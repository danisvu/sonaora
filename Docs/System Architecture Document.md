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
│                     │      │  • Authentication        │      │                    │
│                     │      │  • Storage               │      │                    │
│                     │      │  • FCM                   │      │                    │
└─────────────────────┘      └──────────────────────────┘      └────────────────────┘

```

### 2.2. Nguyên tắc thiết kế chính

- **Serverless First**: Ưu tiên sử dụng dịch vụ serverless để giảm chi phí vận hành
- **Offline-First**: Cho phép sử dụng cơ bản khi không có kết nối internet
- **Progressive Enhancement**: Tính năng phức tạp (như OCR) sẽ có phương án dự phòng
- **Responsive & Adaptive**: Tối ưu trải nghiệm trên nhiều kích thước và nền tảng
- **Design for Scale**: Thiết kế đảm bảo khả năng mở rộng với chi phí hợp lý

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
└─────────────────────────────────────────────────────────┘

```

### 3.2. Quản lý trạng thái (State Management)

- Sử dụng Provider/Riverpod cho quản lý trạng thái
- Chia nhỏ trạng thái ứng dụng theo tính năng để dễ quản lý và mở rộng
- Kết hợp Dependency Injection để tăng tính testability
- Sử dụng Reactive Programming cho các luồng dữ liệu phức tạp

### 3.3. Module chính

1. **Authentication Module**: Xử lý đăng ký, đăng nhập, quản lý phiên
2. **Lottery Results Module**: Xem kết quả xổ số, lịch quay thưởng
3. **Ticket Management Module**: Quản lý vé số, nhận diện vé bằng OCR
4. **Ticket Checking Module**: Dò vé tự động, tính toán giải thưởng
5. **Analytics Module**: Thống kê, phân tích, dự đoán
6. **Notification Module**: Quản lý thông báo và nhắc nhở
7. **User Profile Module**: Quản lý thông tin cá nhân và cài đặt
8. **Community Module** (Giai đoạn 2+): Tính năng cộng đồng

### 3.4. Navigation và Routing

- Sử dụng Navigator 2.0 của Flutter
- Định nghĩa rõ các route và deep links
- Quản lý navigation history cho trải nghiệm người dùng mượt mà

## 4. Kiến trúc Backend

### 4.1. Dịch vụ Firebase

### 4.1.1. Firebase Authentication

- Hỗ trợ đăng nhập bằng email/mật khẩu
- Đăng nhập qua số điện thoại (OTP)
- Đăng nhập qua tài khoản Google, Facebook
- Quản lý phiên người dùng và bảo mật

### 4.1.2. Cloud Firestore

- Database NoSQL cho dữ liệu ứng dụng
- Cấu trúc dữ liệu được thiết kế optimize cho truy vấn thường xuyên
- Security rules nghiêm ngặt để bảo vệ dữ liệu người dùng
- Offline persistence để hoạt động khi mất kết nối

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

```

### 4.1.3. Cloud Functions

- Xử lý OCR vé số thông qua API của LLM
- Cập nhật kết quả xổ số tự động
- Dò vé số và gửi thông báo kết quả
- Tính toán thống kê và phân tích theo lịch trình

### 4.1.4. Firebase Storage

- Lưu trữ hình ảnh vé số người dùng tải lên
- Cache kết quả OCR để tái sử dụng
- Lưu trữ tài nguyên tĩnh của ứng dụng

### 4.1.5. Firebase Cloud Messaging (FCM)

- Gửi thông báo kết quả xổ số
- Thông báo khi có vé trúng thưởng
- Nhắc nhở các sự kiện xổ số
- Thông báo cộng đồng và cập nhật ứng dụng

### 4.2. Các dịch vụ bên ngoài

### 4.2.1. OCR API (LLM)

- Sử dụng OpenAI Vision API hoặc Gemini Pro Vision
- Prompt được tối ưu cho việc nhận dạng vé số Việt Nam
- Fallback strategy khi API không khả dụng hoặc kết quả không chính xác

### 4.2.2. Xổ số API

- Tích hợp với nguồn API hoặc web scraping để lấy kết quả xổ số
- Xây dựng hệ thống caching kết quả để giảm chi phí API
- Chiến lược backup data khi nguồn chính không khả dụng

### 4.3. Bảo mật

### 4.3.1. Xác thực và phân quyền

- JWT (JSON Web Tokens) cho xác thực API
- Firebase Authentication cho xác thực người dùng
- Role-based access control cho các tính năng nâng cao

### 4.3.2. Bảo vệ dữ liệu

- Mã hóa dữ liệu nhạy cảm
- Firestore Security Rules chi tiết
- Giới hạn quyền truy cập theo nguyên tắc principle of least privilege

### 4.3.3. Tuân thủ quy định

- Tuân thủ PDPA Việt Nam
- Xin phép người dùng trước khi truy cập camera, thư viện ảnh
- Chính sách quyền riêng tư rõ ràng và dễ hiểu

## 5. Luồng dữ liệu

### 5.1. Luồng dữ liệu chính

### 5.1.1. Xem kết quả xổ số

```
[Ứng dụng di động] → [Request kết quả] → [Cloud Functions/Firestore]
                                               ↓
[Hiển thị kết quả] ← [Dữ liệu kết quả] ← [Kết quả được lưu cache]

```

### 5.1.2. Chụp và nhận dạng vé số

```
[Chụp ảnh vé] → [Xử lý sơ bộ trên thiết bị] → [Upload lên Storage]
                                                   ↓
                                          [Cloud Function trigger]
                                                   ↓
                                             [Gọi OCR API]
                                                   ↓
[Hiển thị & xác nhận] ← [Kết quả OCR] ← [Lưu vào Firestore]

```

### 5.1.3. Dò vé tự động

```
[Vé đã lưu] → [Kết quả xổ số mới] → [Cloud Function dò vé]
                                            ↓
                                  [Tìm thấy vé trúng thưởng]
                                            ↓
                                   [Gửi FCM thông báo]
                                            ↓
[Hiển thị thông báo] ← [Người dùng mở thông báo] ← [Nhận FCM]

```

### 5.1.4. Phân tích thống kê

```
[Dữ liệu kết quả xổ số] → [Cloud Function phân tích] → [Thống kê trong Firestore]
                                                               ↓
[Hiển thị biểu đồ, thống kê] ← [Request dữ liệu thống kê] ← [Ứng dụng]

```

### 5.2. Trao đổi dữ liệu

- RESTful API cho giao tiếp giữa client và backend
- WebSockets (thông qua Firestore) cho dữ liệu real-time
- JSON là định dạng dữ liệu chính
- Batch processing cho các tác vụ nặng

## 6. Hiệu suất và khả năng mở rộng

### 6.1. Chiến lược caching

- Caching dữ liệu trên thiết bị: SQLite hoặc Hive
- Caching kết quả xổ số trên Firestore
- Firebase Functions caching cho các tính toán phức tạp
- Lazy loading cho dữ liệu lịch sử và thống kê

### 6.2. Chiến lược mở rộng

- Sharding dữ liệu theo vùng miền (Bắc, Trung, Nam)
- Horizontal scaling qua các dịch vụ Firebase
- Tối ưu Chi phí thông qua Firebase Blaze Plan
- Rate limiting cho các tính năng tiêu tốn tài nguyên

### 6.3. Monitoring và Alerting

- Firebase Performance Monitoring
- Firebase Crashlytics cho theo dõi lỗi
- Custom logging cho hành vi người dùng và hiệu suất
- Hệ thống cảnh báo cho các vấn đề quan trọng

## 7. Chiến lược triển khai

### 7.1. Môi trường phát triển

- Development: Môi trường phát triển cục bộ
- Staging: Môi trường kiểm thử tích hợp
- Production: Môi trường người dùng cuối

### 7.2. CI/CD Pipeline

```
[Git Push] → [GitHub Actions trigger] → [Unit Tests + Linting]
                                               ↓
[Firebase Test Lab] ← [Build APK/IPA] ← [Tích hợp thành công]
        ↓
[Firebase App Distribution (Beta)]
        ↓
[Play Store/App Store (Production)]

```

### 7.3. Chiến lược phát hành

- Beta testing trước mỗi phát hành
- Phát hành theo từng giai đoạn (phased rollout)
- A/B testing cho tính năng mới
- Feedback loop từ người dùng thông qua Firebase Analytics

## 8. Công nghệ và thư viện

### 8.1. Stack công nghệ chính

- **Frontend**: Flutter 3.x, Dart 3.x
- **Backend**: Firebase (Firestore, Functions, Auth, Storage, FCM)
- **AI/ML**: OpenAI Vision API hoặc Google Cloud Vision AI
- **Analytics**: Firebase Analytics, Google Analytics
- **CI/CD**: GitHub Actions, Firebase App Distribution

### 8.2. Thư viện phía client

- **State Management**: provider/riverpod
- **Networking**: dio, http
- **Local Storage**: shared_preferences, hive, sqflite
- **UI Components**: flutter_svg, fl_chart, cached_network_image
- **Utilities**: image_picker, camera, intl, url_launcher

### 8.3. Thư viện phía server

- **Firebase Admin SDK**: firebase-admin
- **OCR Processing**: axios, sharp
- **Data Processing**: lodash, moment
- **Security**: jsonwebtoken, crypto

## 9. Cân nhắc bổ sung

### 9.1. Khả năng offline

- Lưu cache kết quả xổ số gần đây
- Dò vé offline sơ bộ
- Đồng bộ hóa khi có kết nối internet

### 9.2. Đa nền tảng

- iOS và Android thông qua Flutter
- Web app (giai đoạn sau) thông qua Flutter Web
- Tối ưu giao diện cho từng nền tảng

### 9.3. Khả năng tương tác

- Deep linking cho chia sẻ kết quả, dự đoán
- Share extensions cho chia sẻ vé số
- Widget trên màn hình chính (Home screen)

### 9.4. Khả năng mở rộng tính năng

- Phân tách modules cho việc mở rộng dễ dàng
- API versioning cho khả năng tương thích ngược
- Feature flags để kiểm soát tính năng mới

## 10. Rủi ro và giảm thiểu

### 10.1. Rủi ro kỹ thuật

| Rủi ro | Mức độ | Tác động | Giải pháp giảm thiểu |
| --- | --- | --- | --- |
| Độ chính xác OCR không đạt yêu cầu | Cao | Trải nghiệm người dùng kém | Kết hợp với nhập thủ công, cải thiện tiền xử lý hình ảnh |
| Chi phí Firebase vượt dự kiến | Trung bình | Tăng chi phí vận hành | Monitoring chặt chẽ, tối ưu truy vấn, caching hiệu quả |
| Thay đổi API/chính sách của LLM | Cao | Ảnh hưởng tính năng OCR | Thiết kế adapter pattern, dự phòng nhiều nhà cung cấp OCR |
| Hiệu suất trên thiết bị thấp | Trung bình | Người dùng không hài lòng | Tối ưu code, lazy loading, nén hình ảnh |

### 10.2. Rủi ro kinh doanh

| Rủi ro | Mức độ | Tác động | Giải pháp giảm thiểu |
| --- | --- | --- | --- |
| Thay đổi quy định pháp luật về xổ số | Cao | Thay đổi mô hình kinh doanh | Theo dõi chặt chẽ quy định, thiết kế linh hoạt |
| Cạnh tranh từ ứng dụng tương tự | Trung bình | Mất thị phần | Tập trung vào UX và tính năng độc đáo |
| Khó khăn trong tiếp cận người dùng lớn tuổi | Cao | Hạn chế tăng trưởng | UI thân thiện, hỗ trợ font lớn, hướng dẫn chi tiết |

## 11. Kết luận

Kiến trúc hệ thống của ứng dụng Số Nào Ra được thiết kế với mục tiêu tạo ra trải nghiệm người dùng tốt nhất trong khi tối ưu chi phí vận hành. Bằng cách sử dụng Flutter kết hợp với các dịch vụ Firebase và AI/ML hiện đại, ứng dụng có thể đáp ứng nhu cầu của người chơi xổ số Việt Nam một cách hiệu quả và mở rộng dễ dàng trong tương lai.

## 12. Phụ lục

### 12.1. Từ điển thuật ngữ

- **OCR**: Optical Character Recognition - Nhận dạng ký tự quang học
- **LLM**: Large Language Model - Mô hình ngôn ngữ lớn
- **FCM**: Firebase Cloud Messaging - Dịch vụ gửi thông báo của Firebase
- **JWT**: JSON Web Token - Chuẩn mở để truyền thông tin an toàn

### 12.2. Tài liệu tham khảo

- Flutter Architecture Blueprint
- Firebase Serverless Architecture Guidelines
- Material Design 3 Guidelines
- Google Cloud Vision AI Documentation
- Ứng dụng Offline-First Architecture

### 12.3. Diagram và hình ảnh

- Sơ đồ kiến trúc tổng thể
- Sơ đồ cơ sở dữ liệu
- Mô hình luồng dữ liệu
- Diagram CI/CD

---

*Tài liệu này được phát triển bởi đội ngũ Số Nào Ra và được cập nhật lần cuối vào 19/03/2025.*
