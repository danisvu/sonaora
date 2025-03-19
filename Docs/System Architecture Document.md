# Tài liệu kiến trúc hệ thống - Dự án Số Nào Ra (SoNaoRa)

## 1. Giới thiệu

### 1.1. Mục đích tài liệu

Tài liệu này mô tả chi tiết kiến trúc hệ thống của ứng dụng Số Nào Ra (SoNaoRa) - nền tảng hỗ trợ người chơi xổ số tại Việt Nam. Tài liệu cung cấp cái nhìn tổng quan về các thành phần kiến trúc, mối quan hệ giữa chúng, và các quyết định thiết kế chính.

### 1.2. Phạm vi dự án

Số Nào Ra là ứng dụng di động giúp người chơi xổ số có thể xem kết quả xổ số nhanh chóng, quản lý vé số hiệu quả thông qua công nghệ nhận dạng hình ảnh AI, dò vé tự động, nhận thông báo kết quả, và tiếp cận các phân tích thống kê để tăng cơ hội trúng thưởng.

### 1.3. Các bên liên quan

- Người dùng cuối: Người chơi xổ số tại Việt Nam
- Đội ngũ phát triển: PM, Developer, UX/UI Designer, QA
- Đối tác tiềm năng: Công ty xổ số kiến thiết các tỉnh, Vietlott

## 2. Tổng quan kiến trúc

### 2.1. Mô hình kiến trúc tổng thể

Ứng dụng Số Nào Ra sử dụng kiến trúc client-serverless với các thành phần chính:

```
┌─────────────────────┐      ┌──────────────────────────┐      ┌────────────────────┐
│                     │      │                          │      │                    │
│  MOBILE APP         │      │  FIREBASE SERVICES       │      │  EXTERNAL SERVICES │
│  (Flutter)          │ ───► │  • Firestore             │ ───► │  • OCR API (LLM)   │
│                     │      │  • Firebase Functions    │      │  • Xổ số API       │
│                     │      │  • Authentication        │      │  • Edge Computing  │
│                     │      │  • Storage               │      │                    │
│                     │      │  • FCM                   │      │                    │
└─────────────────────┘      └──────────────────────────┘      └────────────────────┘
          │                              │                              │
          ▼                              ▼                              ▼
┌─────────────────────┐      ┌──────────────────────────┐      ┌────────────────────┐
│                     │      │                          │      │                    │
│  MONITORING &       │      │  DEVOPS &                │      │  ANALYTICS &       │
│  OBSERVABILITY      │      │  CI/CD PIPELINE          │      │  DATA PIPELINE     │
│                     │      │                          │      │                    │
└─────────────────────┘      └──────────────────────────┘      └────────────────────┘
```

### 2.2. Nguyên tắc thiết kế chính

- **Serverless First**: Ưu tiên sử dụng dịch vụ serverless để giảm chi phí vận hành
- **Offline-First**: Cho phép sử dụng cơ bản khi không có kết nối internet
- **Progressive Enhancement**: Tính năng phức tạp (như OCR) sẽ có phương án dự phòng
- **Responsive & Adaptive**: Tối ưu trải nghiệm trên nhiều kích thước và nền tảng
- **Design for Scale**: Thiết kế đảm bảo khả năng mở rộng với chi phí hợp lý
- **Security by Design**: Tích hợp bảo mật vào mọi giai đoạn phát triển
- **AI-First Approach**: Tận dụng công nghệ AI để tối ưu trải nghiệm người dùng
- **Data-Driven Development**: Sử dụng dữ liệu để định hướng quyết định thiết kế và phát triển

## 3. Kiến trúc ứng dụng di động

### 3.1. Kiến trúc tổng thể

Ứng dụng di động Số Nào Ra được phát triển bằng Flutter theo mô hình kiến trúc phân lớp:

```
┌─────────────────────────────────────────────────────────┐
│ PRESENTATION LAYER                                      │
│ • Screens                                               │
│ • Widgets                                               │
│ • State Management (Provider/Riverpod)                  │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│ BUSINESS LOGIC LAYER                                    │
│ • Use Cases                                             │
│ • Services                                              │
│ • State Controllers                                     │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│ DATA LAYER                                              │
│ • Repositories                                          │
│ • Data Sources (Remote & Local)                         │
│ • Models                                                │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│ INFRASTRUCTURE LAYER                                    │
│ • Firebase Services                                     │
│ • Local Storage                                         │
│ • Network                                               │
│ • Edge Computing Components                             │
└─────────────────────────────────────────────────────────┘
```

### 3.2. Quản lý trạng thái (State Management)

- Sử dụng Provider/Riverpod cho quản lý trạng thái
- Chia nhỏ trạng thái ứng dụng theo tính năng để dễ quản lý và mở rộng
- Kết hợp Dependency Injection để tăng tính testability
- Sử dụng Reactive Programming cho các luồng dữ liệu phức tạp
- Áp dụng CQRS (Command Query Responsibility Segregation) pattern cho các tính năng phức tạp

### 3.3. Module chính

1. **Authentication Module**: Xử lý đăng ký, đăng nhập, quản lý phiên
2. **Lottery Results Module**: Xem kết quả xổ số, lịch quay thưởng
3. **Ticket Management Module**: Quản lý vé số, nhận diện vé bằng OCR
4. **Ticket Checking Module**: Dò vé tự động, tính toán giải thưởng
5. **Analytics Module**: Thống kê, phân tích, dự đoán
6. **Notification Module**: Quản lý thông báo và nhắc nhở
7. **User Profile Module**: Quản lý thông tin cá nhân và cài đặt
8. **Community Module** (Giai đoạn 2+): Tính năng cộng đồng
9. **Feature Flag Module**: Quản lý và điều khiển tính năng mới, A/B testing
10. **Performance Monitoring Module**: Thu thập và phân tích hiệu suất ứng dụng

### 3.4. Navigation và Routing

- Sử dụng Navigator 2.0 của Flutter
- Định nghĩa rõ các route và deep links
- Quản lý navigation history cho trải nghiệm người dùng mượt mà
- Tích hợp analytics tracking cho navigation events

### 3.5. Edge Computing Components

- **Image Pre-processing**: Xử lý sơ bộ hình ảnh vé số trên thiết bị
- **Offline OCR Capabilities**: Tính năng OCR cơ bản khi không có internet
- **Local Data Analysis**: Phân tích dữ liệu cơ bản trên thiết bị để giảm tải server
- **Compression Pipeline**: Tối ưu hóa kích thước dữ liệu trước khi truyền lên cloud

## 4. Kiến trúc Backend

### 4.1. Dịch vụ Firebase

#### 4.1.1. Firebase Authentication

- Hỗ trợ đăng nhập bằng email/mật khẩu
- Đăng nhập qua số điện thoại (OTP)
- Đăng nhập qua tài khoản Google, Facebook
- Quản lý phiên người dùng và bảo mật
- MFA (Multi-Factor Authentication) cho tài khoản nhạy cảm

#### 4.1.2. Cloud Firestore

- Database NoSQL cho dữ liệu ứng dụng
- Cấu trúc dữ liệu được thiết kế optimize cho truy vấn thường xuyên
- Security rules nghiêm ngặt để bảo vệ dữ liệu người dùng
- Offline persistence để hoạt động khi mất kết nối
- Shard collection strategy cho việc mở rộng quy mô

```
[Cấu trúc database]
users/
  {userId}/
    profile: {...}
    preferences: {...}
    tickets/
      {ticketId}: {...}
    notifications/
      {notificationId}: {...}
    analytics/
      usage_metrics: {...}

lottery_results/
  traditional/
    {region}/
      {date}/
        results: {...}
  vietlott/
    {type}/
      {date}/
        results: {...}

statistics/
  hot_numbers/
    {region}/
      {timeframe}: [...]
  cold_numbers/
    {region}/
      {timeframe}: [...]

system/
  feature_flags/
    {flagId}: {...}
  performance_metrics/
    {date}: {...}
```

#### 4.1.3. Cloud Functions

- Xử lý OCR vé số thông qua API của LLM với abstraction layer
- Cập nhật kết quả xổ số tự động
- Dò vé số và gửi thông báo kết quả
- Tính toán thống kê và phân tích theo lịch trình
- Cron jobs cho maintenance và data cleanup
- Rate limiting và usage monitoring
- Circuit breaker pattern cho các API calls bên ngoài

#### 4.1.4. Firebase Storage

- Lưu trữ hình ảnh vé số người dùng tải lên
- Cache kết quả OCR để tái sử dụng
- Lưu trữ tài nguyên tĩnh của ứng dụng
- Tiered storage strategy cho data retention
- Automated lifecycle management (archiving/deletion)

#### 4.1.5. Firebase Cloud Messaging (FCM)

- Gửi thông báo kết quả xổ số
- Thông báo khi có vé trúng thưởng
- Nhắc nhở các sự kiện xổ số
- Thông báo cộng đồng và cập nhật ứng dụng
- Segmented messaging dựa trên hành vi người dùng

### 4.2. Các dịch vụ bên ngoài

#### 4.2.1. OCR API (LLM) với Abstraction Layer

- Sử dụng adapter pattern cho multiple LLM providers (OpenAI Vision API, Gemini Pro Vision, etc.)
- Prompt engineering framework với versioning và A/B testing
- Automatic prompt optimization dựa trên feedback
- Caching và data deduplication strategy
- Fallback mechanism khi API chính không khả dụng
- Cost optimization through batch processing

```
┌─────────────────────┐
│                     │
│  OCR CLIENT API     │
│                     │
└────────┬────────────┘
         │
┌────────▼────────────┐     ┌─────────────────────┐
│                     │     │                     │
│  ADAPTER INTERFACE  │────►│  OPENAI ADAPTER     │
│                     │     │                     │
└────────┬────────────┘     └─────────────────────┘
         │
         │              ┌─────────────────────┐
         └─────────────►│                     │
                        │  GEMINI ADAPTER     │
                        │                     │
                        └─────────────────────┘
```

#### 4.2.2. Xổ số API

- Tích hợp với nguồn API hoặc web scraping để lấy kết quả xổ số
- Xây dựng hệ thống caching kết quả để giảm chi phí API
- Chiến lược backup data khi nguồn chính không khả dụng
- Data validation và consistency checking
- Rate limiting và retry mechanism

### 4.3. Bảo mật

#### 4.3.1. Xác thực và phân quyền

- JWT (JSON Web Tokens) cho xác thực API
- Firebase Authentication cho xác thực người dùng
- Role-based access control cho các tính năng nâng cao
- Tích hợp OAuth 2.0 cho third-party authentication
- Session management với automatic timeout

#### 4.3.2. Bảo vệ dữ liệu

- Mã hóa dữ liệu nhạy cảm (encryption at rest and in transit)
- Firestore Security Rules chi tiết
- Giới hạn quyền truy cập theo nguyên tắc principle of least privilege
- Data anonymization cho phân tích và debugging
- Secure deletion process cho data lifecycle management

#### 4.3.3. Secure SDLC và DevSecOps

- SAST (Static Application Security Testing) trong CI/CD pipeline
- DAST (Dynamic Application Security Testing) cho production environment
- Dependency scanning và vulnerability management
- Regular penetration testing
- Threat modeling cho các tính năng mới
- Security incident response plan

#### 4.3.4. Tuân thủ quy định

- Tuân thủ PDPA Việt Nam
- Xin phép người dùng trước khi truy cập camera, thư viện ảnh
- Chính sách quyền riêng tư rõ ràng và dễ hiểu
- Cơ chế thực hiện quyền "quên" của người dùng (right to be forgotten)
- Data Processing Agreement với third-party services

## 5. Luồng dữ liệu

### 5.1. Luồng dữ liệu chính

#### 5.1.1. Xem kết quả xổ số

```
[Ứng dụng di động] → [Request kết quả] → [Cloud Functions/Firestore]
                                               ↓
[Hiển thị kết quả] ← [Dữ liệu kết quả] ← [Kết quả được lưu cache]
           ↓
[Analytics event] → [Firebase Analytics] → [Data warehouse]
```

#### 5.1.2. Chụp và nhận dạng vé số

```
[Chụp ảnh vé] → [Xử lý sơ bộ trên thiết bị] → [Pre-classification]
                               ↓
                  [Có kết nối internet?] → [No] → [Lưu vào queue local]
                               ↓ [Yes]                     ↓
                       [Upload lên Storage]         [Sync khi có kết nối]
                               ↓
                    [Cloud Function trigger]
                               ↓
         [OCR Abstraction Layer] → [LLM Provider Selection]
                               ↓
                          [Gọi OCR API]
                               ↓
[Hiển thị & xác nhận] ← [Kết quả OCR] ← [Lưu vào Firestore] → [OCR Analytics]
```

#### 5.1.3. Dò vé tự động

```
[Vé đã lưu] → [Kết quả xổ số mới] → [Cloud Function dò vé]
                                            ↓
                                  [Tìm thấy vé trúng thưởng]
                                            ↓
                                   [Gửi FCM thông báo]
                                            ↓
[Hiển thị thông báo] ← [Người dùng mở thông báo] ← [Nhận FCM]
           ↓
[Log engagement] → [Analytics] → [User engagement metrics]
```

#### 5.1.4. Phân tích thống kê với Hybrid Analytics

```
[Dữ liệu kết quả xổ số] → [Cloud Function phân tích] → [Thống kê trong Firestore]
                                     ↓
        [On-device analytics] ← [Subset data sync] ← [Data optimization]
                  ↓
[Hiển thị biểu đồ, thống kê] ← [Request dữ liệu] ← [Ứng dụng]
                  ↓
[Phân tích local dữ liệu] → [User-specific insights]
```

### 5.2. Event-Driven Architecture

- Event sourcing pattern cho các tính năng real-time
- Publish-subscribe model cho thông báo và cập nhật
- Command-query separation cho việc đọc/ghi dữ liệu
- Event logging cho audit trail và debugging

### 5.3. Trao đổi dữ liệu

- RESTful API cho giao tiếp giữa client và backend
- GraphQL consideration cho tương lai (phase 2)
- WebSockets (thông qua Firestore) cho dữ liệu real-time
- JSON là định dạng dữ liệu chính
- Batch processing cho các tác vụ nặng
- Compression và binary protocols cho thiết bị yếu/mạng chậm

## 6. Hiệu suất và khả năng mở rộng

### 6.1. Performance Engineering

#### 6.1.1. Performance Metrics & KPIs

- **API Response Time**: < 500ms cho P95
- **App Startup Time**: < 2s trên thiết bị trung bình
- **OCR Processing Time**: < 3s end-to-end
- **UI Rendering Performance**: > 60 FPS cho animations
- **Memory Footprint**: < 150MB peak usage
- **Battery Impact**: < 5% per hour of active use
- **Network Bandwidth**: < 50MB daily data usage
- **Storage Utilization**: < 100MB app storage

#### 6.1.2. Performance Testing Strategy

- Automated performance testing trong CI/CD pipeline
- Synthetic monitoring cho production environment
- Real user monitoring (RUM) với Firebase Performance
- Load testing cho Cloud Functions và Firestore
- Benchmarking trên various device tiers

#### 6.1.3. Performance Optimization Techniques

- Lazy loading cho components không cần thiết ngay
- Image optimization pipeline
- Code splitting và tree shaking
- Asset preloading cho critical paths
- Service worker cho caching assets
- Background processing cho tác vụ nặng

### 6.2. Chiến lược caching

- **Client-side Cache**:
  - Caching dữ liệu trên thiết bị: SQLite hoặc Hive
  - LRU (Least Recently Used) eviction policy
  - Time-based invalidation cho dữ liệu quan trọng
  - Persistent cache cho offline support

- **Server-side Cache**:
  - Caching kết quả xổ số trên Firestore
  - Firebase Functions caching cho các tính toán phức tạp
  - Redis consideration cho phase 2
  - CDN cho static assets

- **API Response Caching**:
  - HTTP caching với ETag
  - Cache-Control headers optimization
  - Conditional requests với If-Modified-Since

### 6.3. Chiến lược mở rộng

- **Horizontal Scaling**:
  - Sharding dữ liệu theo vùng miền (Bắc, Trung, Nam)
  - Horizontal scaling qua các dịch vụ Firebase
  - Stateless design cho Cloud Functions

- **Database Scaling**:
  - Collection sharding trong Firestore
  - Indexing strategy optimization
  - Read/write optimization với denormalization
  - Phân chia workload giữa realtime và batch processing

- **Cost Optimization**:
  - Tối ưu Chi phí thông qua Firebase Blaze Plan
  - Reserved instances for predictable workloads
  - Budget alerts và usage monitoring
  - Data lifecycle management

### 6.4. Kiến trúc dữ liệu phân tán

- **Distributed Data Store**:
  - Strong consistency cho dữ liệu quan trọng
  - Eventual consistency cho dữ liệu thống kê
  - Multi-region replication cho high availability

- **Data Partitioning**:
  - Vertical partitioning theo loại dữ liệu
  - Geographic partitioning theo vùng miền
  - Time-based partitioning cho dữ liệu lịch sử

## 7. Observability và Monitoring

### 7.1. Monitoring Infrastructure

- **Metrics Collection**:
  - Firebase Performance Monitoring
  - Custom metrics cho business KPIs
  - System health metrics
  - Application performance index (Apdex)

- **Logging Strategy**:
  - Structured logging (JSON format)
  - Log levels (DEBUG, INFO, WARN, ERROR, FATAL)
  - Context-rich logging với correlation IDs
  - Log aggregation với Firebase/Google Cloud Logging

- **Distributed Tracing**:
  - End-to-end tracing cho user journeys
  - Trace sampling strategy
  - Performance bottleneck identification
  - Integration với OpenTelemetry (future)

### 7.2. Alerting và Incident Response

- **Alert Configuration**:
  - Threshold-based alerts
  - Anomaly detection
  - Composite alerts để giảm noise
  - Escalation policies

- **Incident Management**:
  - Incident classification (P0-P4)
  - Automated incident response cho common issues
  - Postmortem template và process
  - Service Level Objectives (SLOs) tracking

### 7.3. User Experience Monitoring

- **Real User Monitoring**:
  - User journey tracking
  - Rage clicks detection
  - Error tracking
  - Session replay consideration (phase 2)

- **Synthetic Monitoring**:
  - Critical path testing
  - API availability checks
  - Performance regression detection
  - Scheduled monitoring jobs

### 7.4. Business Intelligence và Analytics

- **Data Warehouse**:
  - ETL pipeline từ Firebase vào BigQuery
  - Data mart cho specific business domains
  - Automated reporting
  - ML model training dataset preparation

- **Visualization**:
  - Custom dashboards cho stakeholders
  - Real-time business metrics
  - User growth và retention metrics
  - Feature adoption tracking

## 8. Chiến lược dữ liệu toàn diện

### 8.1. Data Governance

- **Data Classification**:
  - PII (Personal Identifiable Information)
  - Sensitive data
  - Operational data
  - Analytics data

- **Data Lifecycle Management**:
  - Data creation và validation
  - Storage và retention policies
  - Archiving strategy
  - Secure deletion

- **Data Quality**:
  - Validation rules
  - Data consistency checks
  - Automated quality monitoring
  - Data cleansing processes

### 8.2. Data Backup và Disaster Recovery

- **Backup Strategy**:
  - Daily incremental backups
  - Weekly full backups
  - Multi-region backup storage
  - Encryption for backups

- **Recovery Planning**:
  - Recovery Time Objective (RTO): 4 hours
  - Recovery Point Objective (RPO): 1 hour
  - Disaster recovery testing schedule
  - Automated recovery procedures

- **Business Continuity**:
  - Fallback services for critical functions
  - Degraded mode operation capabilities
  - Communication plan during outages
  - Regular drills và testing

### 8.3. Data Migration Strategy

- **Phased Migration Approach**:
  - Data model compatibility layer
  - Dual-write period
  - Verification và validation
  - Cutover planning

- **Firebase to Custom Backend**:
  - Data export procedures
  - Schema transformation
  - Historical data handling
  - Service transition without downtime

### 8.4. Data Privacy Engineering

- **Privacy by Design**:
  - Data minimization principle
  - Purpose limitation
  - Storage limitation
  - Data subject rights implementation

- **Anonymization Techniques**:
  - Pseudonymization for operational data
  - k-anonymity for analytics
  - Differential privacy consideration
  - Data masking for debugging

## 9. Chiến lược AI và Advanced Analytics

### 9.1. AI-Driven Modular Architecture (AIDMA)

- **Modular AI Components**:
  - OCR module với version control
  - Prediction engine cho "hot numbers"
  - User behavior analysis
  - Anomaly detection

- **Continuous Learning Pipeline**:
  - Feedback collection
  - Model retraining triggers
  - A/B testing framework
  - Performance evaluation metrics

- **Responsible AI Practices**:
  - Fairness evaluation
  - Transparency in AI decisions
  - Human oversight
  - Ethical considerations

### 9.2. OCR Enhancement Strategy

- **Multi-tiered OCR Approach**:
  - Local OCR cho simple cases
  - Cloud OCR cho complex cases
  - Hybrid approach cho balanced performance/cost

- **Prompt Engineering Framework**:
  - Systematic prompt development
  - Version control for prompts
  - Effectiveness measurement
  - Context optimization

- **Image Processing Pipeline**:
  - Preprocessing techniques catalog
  - Adaptive processing based on image quality
  - Post-processing for verification
  - Quality scoring để determine confidence

### 9.3. Predictive Analytics

- **Statistical Models**:
  - Time series analysis
  - Pattern recognition
  - Correlation analysis
  - Seasonality detection

- **User Personalization**:
  - Preference learning
  - Habit recognition
  - Personalized recommendations
  - Engagement optimization

## 10. Feature Flagging và Experimentation

### 10.1. Feature Flag System

- **Flag Types**:
  - Release flags (on/off)
  - Operational flags (configuration)
  - Experimentation flags (A/B testing)
  - Permission flags (user-based)

- **Implementation Strategy**:
  - Centralized flag management
  - Real-time updates
  - Default values for offline
  - Audit logging

- **Targeting Rules**:
  - User segment targeting
  - Device capability targeting
  - Geography-based rules
  - Progressive rollout percentages

### 10.2. A/B Testing Framework

- **Experiment Design**:
  - Hypothesis formulation
  - Sample size calculation
  - Duration planning
  - Success metrics definition

- **Experimentation Pipeline**:
  - Variant assignment
  - User tracking
  - Results collection
  - Statistical analysis

- **Optimization Loop**:
  - Continuous experimentation
  - Automated winner selection
  - Learning documentation
  - Knowledge sharing

## 11. Chiến lược triển khai

### 11.1. Môi trường phát triển

- Development: Môi trường phát triển cục bộ
- Staging: Môi trường kiểm thử tích hợp
- UAT: User Acceptance Testing environment
- Production: Môi trường người dùng cuối

### 11.2. CI/CD Pipeline với DevSecOps

```
[Git Push] → [GitHub Actions trigger]
               ↓
[Static Analysis] → [SAST Security Scan] → [Dependency Scan]
               ↓
[Unit & Integration Tests] → [Coverage Analysis]
               ↓
[Build APK/IPA] → [Automated UI Tests]
               ↓
[Deploy to Firebase Test Lab] → [Performance Benchmark]
               ↓
[Security Dynamic Analysis] → [Compliance Checks]
               ↓
[Firebase App Distribution (Beta)] → [Beta Tester Feedback]
               ↓
[Production Deployment] → [Canary Release] → [Full Rollout]
               ↓
[Post-Deployment Verification] → [Synthetic Monitoring]
```

### 11.3. Chiến lược phát hành

- Beta testing trước mỗi phát hành
- Phát hành theo từng giai đoạn (phased rollout)
- A/B testing cho tính năng mới
- Feedback loop từ người dùng thông qua Firebase Analytics
- Automated rollback capability if anomalies detected
- Feature flag control for emergency disabling

### 11.4. Versioning Strategy

- Semantic versioning (MAJOR.MINOR.PATCH)
- API versioning for backward compatibility
- Database schema versioning
- Migration paths between versions
- Support policy for older versions

## 12. Công nghệ và thư viện

### 12.1. Stack công nghệ chính

- **Frontend**: Flutter 3.x, Dart 3.x
- **Backend**: Firebase (Firestore, Functions, Auth, Storage, FCM)
- **AI/ML**: OpenAI Vision API, Google Cloud Vision AI, On-device ML models
- **Analytics**: Firebase Analytics, Google Analytics, BigQuery
- **CI/CD**: GitHub Actions, Firebase App Distribution, Fastlane
- **Monitoring**: Firebase Performance, Crashlytics, Custom monitoring

### 12.2. Thư viện phía client

- **State Management**: provider/riverpod, bloc
- **Networking**: dio, http, graphql_flutter (future)
- **Local Storage**: shared_preferences, hive, sqflite
- **UI Components**: flutter_svg, fl_chart, cached_network_image
- **Utilities**: image_picker, camera, intl, url_launcher
- **Testing**: flutter_test, mockito, integration_test
- **Performance**: performance_overlay, memory_profiler
- **Feature Flags**: firebase_remote_config, feature_flags

### 12.3. Thư viện phía server

- **Firebase Admin SDK**: firebase-admin
- **OCR Processing**: axios, sharp, tensorflow.js
- **Data Processing**: lodash, moment
- **Security**: jsonwebtoken, crypto
- **Monitoring**: prometheus-client, opentelemetry

## 13. Rủi ro và giảm thiểu

### 13.1. Rủi ro kỹ thuật

| Rủi ro | Mức độ | Tác động | Giải pháp giảm thiểu |
| --- | --- | --- | --- |
| Độ chính xác OCR không đạt yêu cầu | Cao | Trải nghiệm người dùng kém | 1. Kết hợp với nhập thủ công<br>2. Cải thiện tiền xử lý hình ảnh<br>3. Multi-provider OCR strategy<br>4. Progressive prompting technique |
| Chi phí Firebase vượt dự kiến | Trung bình | Tăng chi phí vận hành | 1. Monitoring chặt chẽ<br>2. Tối ưu truy vấn<br>3. Caching hiệu quả<br>4. Usage quotas và alerting<br>5. Hybrid processing strategy |
| Thay đổi API/chính sách của LLM | Cao | Ảnh hưởng tính năng OCR | 1. Thiết kế adapter pattern<br>2. Dự phòng nhiều nhà cung cấp OCR<br>3. Capability testing framework<br>4. Version pinning with upgrade testing |
| Hiệu suất trên thiết bị thấp | Trung bình | Người dùng không hài lòng | 1. Tối ưu code<br>2. Lazy loading<br>3. Nén hình ảnh<br>4. Performance profiling<br>5. Device-specific optimizations |
| Security vulnerabilities | Cao | Data breach | 1. Regular security audits<br>2. SAST/DAST in pipeline<br>3. Penetration testing<br>4. Security response plan<br>5. Employee security training |

### 13.2. Rủi ro kinh doanh

| Rủi ro | Mức độ | Tác động | Giải pháp giảm thiểu |
| --- | --- | --- | --- |
| Thay đổi quy định pháp luật về xổ số | Cao | Thay đổi mô hình kinh doanh | 1. Theo dõi chặt chẽ quy định<br>2. Thiết kế linh hoạt<br>3. Legal advisory team<br>4. Compliance monitoring |
| Cạnh tranh từ ứng dụng tương tự | Trung bình | Mất thị phần | 1. Tập trung vào UX và tính năng độc đáo<br>2. Faster innovation cycle<br>3. User loyalty program<br>4. Market differentiation strategy |
| Khó khăn trong tiếp cận người dùng lớn tuổi | Cao | Hạn chế tăng trưởng | 1. UI thân thiện<br>2. Hỗ trợ font lớn<br>3. Hướng dẫn chi tiết<br>4. User education program<br>5. Simplified mode for elderly users |
| Poor App Store ratings | Trung bình | Reduced organic acquisition | 1. Pre-release quality gates<br>2. Proactive support<br>3. Quick bug fix cycles<br>4. Rating request optimization |

## 14. Roadmap kiến trúc

### 14.1. Phase 1: MVP Foundation (Months 1-4)

- Triển khai kiến trúc serverless với Firebase
- Xây dựng core features với Flutter
- Thiết lập OCR abstraction layer
- Implement basic monitoring và alerting
- Thiết lập CI/CD pipeline

### 14.2. Phase 2: Optimization & Scale (Months 5-10)

- Edge computing integration
- Feature flag system implementation
- Enhanced observability và monitoring
- Advanced analytics integration
- Performance optimization
- Database sharding implementation

### 14.3. Phase 3: Advanced AI & Cloud Migration (Months 11-22)

- AI-Driven Modular Architecture (AIDMA) implementation
- Hybrid analytics pipeline
- Advanced feature experimentation
- Preparation for potential custom backend
- Microservices decomposition planning
- Data warehouse maturity

## 15. Kết luận

Kiến trúc hệ thống của ứng dụng Số Nào Ra được thiết kế với mục tiêu tạo ra trải nghiệm người dùng tốt nhất trong khi tối ưu chi phí vận hành. Bằng cách sử dụng Flutter kết hợp với các dịch vụ Firebase và AI/ML hiện đại, ứng dụng có thể đáp ứng nhu cầu của người chơi xổ số Việt Nam một cách hiệu quả và mở rộng dễ dàng trong tương lai.

Thiết kế này tích hợp các nguyên tắc modern software architecture như serverless computing, AI-first approach, edge computing, và observability, đồng thời vẫn đảm bảo tính bền vững và khả năng mở rộng khi ứng dụng phát triển.

## 16. Phụ lục

### 16.1. Từ điển thuật ngữ

- **OCR**: Optical Character Recognition - Nhận dạng ký tự quang học
- **LLM**: Large Language Model - Mô hình ngôn ngữ lớn
- **FCM**: Firebase Cloud Messaging - Dịch vụ gửi thông báo của Firebase
- **JWT**: JSON Web Token - Chuẩn mở để truyền thông tin an toàn
- **AIDMA**: AI-Driven Modular Architecture - Kiến trúc module được điều khiển bởi AI
- **SAST**: Static Application Security Testing - Kiểm thử bảo mật ứng dụng tĩnh
- **DAST**: Dynamic Application Security Testing - Kiểm thử bảo mật ứng dụng động
- **KPI**: Key Performance Indicator - Chỉ số hiệu suất chính
- **SLO**: Service Level Objective - Mục tiêu mức dịch vụ

### 16.2. Tài liệu tham khảo

- Flutter Architecture Blueprint
- Firebase Serverless Architecture Guidelines
- Material Design 3 Guidelines
- Google Cloud Vision AI Documentation
- Ứng dụng Offline-First Architecture
- NIST Cybersecurity Framework
- The Twelve-Factor App Methodology
- Domain-Driven Design Principles
- Site Reliability Engineering (SRE) Workbook

### 16.3. Diagram và hình ảnh

- Sơ đồ kiến trúc tổng thể
- Sơ đồ cơ sở dữ liệu
- Mô hình luồng dữ liệu
- Diagram CI/CD
- OCR Process Flow
- Feature Flag Decision Tree
- Monitoring Dashboard Layout

---

*Tài liệu này được phát triển bởi đội ngũ Số Nào Ra và được cập nhật lần cuối vào 19/03/2025.*
