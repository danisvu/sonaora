## PHẦN 1: KẾ HOẠCH TRIỂN KHAI THEO SPRINT CHO GIAI ĐOẠN MVP

### SPRINT 0: KHỞI ĐỘNG DỰ ÁN (2 tuần)

**Mục tiêu**: Thiết lập nền tảng và chuẩn bị cho việc phát triển

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Phân tích yêu cầu chi tiết | PM | 3 ngày | Product Requirements Document |
| Thiết kế hệ thống tổng thể | Developer & PM | 3 ngày | System Architecture Document |
| Thiết kế UI Style Guide | UX/UI | 4 ngày | UI Style Guide, Component Library |
| Thiết lập môi trường phát triển | Developer | 2 ngày | Dev/Staging/Prod environment |
| Thiết lập quy trình làm việc | PM | 2 ngày | Development Workflow Document |

**Buổi họp chính**:

- Kickoff Meeting: Owner trình bày tầm nhìn, PM và team thảo luận
- Technical Planning: Developer và PM thảo luận về kiến trúc
- Design Workshop: UX/UI trình bày style guide và nhận feedback
- Sprint Planning: Lên kế hoạch cho Sprint 1

### SPRINT 1: XEM KẾT QUẢ XỔ SỐ MIỀN NAM & ĐĂNG KÝ/ĐĂNG NHẬP (2 tuần)

**Mục tiêu**: Xây dựng tính năng cốt lõi đầu tiên - xem kết quả xổ số miền Nam và hệ thống xác thực

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Thiết kế màn hình xem kết quả xổ số | UX/UI | 3 ngày | UI Design (Figma) |
| Phát triển API lấy kết quả xổ số | Developer | 4 ngày | API Endpoints |
| Phát triển UI xem kết quả | Developer | 3 ngày | UI Components |
| Thiết kế màn hình đăng ký/đăng nhập | UX/UI | 2 ngày | UI Design (Figma) |
| Phát triển hệ thống xác thực | Developer | 4 ngày | Authentication System |
| Kiểm thử và sửa lỗi | PM & Developer | 2 ngày | Test Reports |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Design Review: UX/UI trình bày thiết kế và nhận feedback
- Mid-sprint Review: Kiểm tra tiến độ giữa sprint
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm

### SPRINT 2: XEM KẾT QUẢ VIETLOTT & LỊCH QUAY THƯỞNG (2 tuần)

**Mục tiêu**: Mở rộng tính năng xem kết quả với Vietlott và lịch quay thưởng

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Thiết kế màn hình kết quả Vietlott | UX/UI | 3 ngày | UI Design (Figma) |
| Phát triển API kết quả Vietlott | Developer | 3 ngày | API Endpoints |
| Phát triển UI kết quả Vietlott | Developer | 3 ngày | UI Components |
| Thiết kế màn hình lịch quay thưởng | UX/UI | 2 ngày | UI Design (Figma) |
| Phát triển tính năng lịch quay thưởng | Developer | 3 ngày | Calendar Feature |
| Kiểm thử và sửa lỗi | PM & Developer | 2 ngày | Test Reports |
| Triển khai phiên bản Alpha | Developer | 1 ngày | Alpha Release |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm
- Alpha Testing Session: Team thử nghiệm phiên bản Alpha

### SPRINT 3: NHẬP VÉ THỦ CÔNG & THÔNG BÁO KẾT QUẢ (2 tuần)

**Mục tiêu**: Phát triển tính năng nhập vé và hệ thống thông báo

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Thiết kế màn hình nhập vé thủ công | UX/UI | 3 ngày | UI Design (Figma) |
| Phát triển tính năng nhập vé thủ công | Developer | 4 ngày | Ticket Entry Feature |
| Thiết kế hệ thống thông báo | UX/UI | 2 ngày | Notification Design |
| Phát triển hệ thống thông báo | Developer | 5 ngày | Notification System |
| Kiểm thử và sửa lỗi | PM & Developer | 2 ngày | Test Reports |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- UX Workshop: Thảo luận về trải nghiệm nhập vé số
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm

### SPRINT 4-5: CHỤP VÀ NHẬN DẠNG VÉ SỐ BẰNG AI (4 tuần)

**Mục tiêu**: Phát triển tính năng nhận dạng vé số bằng AI - đây là tính năng phức tạp nhất trong MVP

**Công việc chi tiết Sprint 4**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Nghiên cứu và lựa chọn phương pháp OCR | Developer & PM | 3 ngày | Technical Research Document |
| Thiết kế UI chụp và nhận dạng vé | UX/UI | 3 ngày | UI Design (Figma) |
| Phát triển tính năng chụp ảnh vé số | Developer | 4 ngày | Camera Integration |
| Phát triển tiền xử lý hình ảnh | Developer | 4 ngày | Image Processing Module |
| Kiểm thử và thu thập dữ liệu | PM & Developer | 2 ngày | Test Image Dataset |

**Công việc chi tiết Sprint 5**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Tích hợp API nhận dạng (LLM) | Developer | 5 ngày | OCR Integration |
| Phát triển UI xác nhận kết quả nhận dạng | Developer | 3 ngày | Confirmation UI |
| Tối ưu hóa độ chính xác nhận dạng | Developer | 4 ngày | Improved Accuracy |
| Kiểm thử và sửa lỗi | PM & Developer | 4 ngày | Comprehensive Testing |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Technical Deep Dive: Thảo luận chi tiết về phương pháp OCR
- Mid-feature Review: Đánh giá giữa chừng tính năng OCR
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm

### SPRINT 6: DÒ VÉ TỰ ĐỘNG & QUẢN LÝ VÉ ĐÃ MUA (2 tuần)

**Mục tiêu**: Hoàn thiện tính năng dò vé và quản lý vé

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Thiết kế UI dò vé và quản lý vé | UX/UI | 3 ngày | UI Design (Figma) |
| Phát triển tính năng dò vé tự động | Developer | 4 ngày | Auto-checking Feature |
| Phát triển tính năng quản lý vé đã mua | Developer | 4 ngày | Ticket Management |
| Tích hợp với thông báo kết quả | Developer | 3 ngày | Notification Integration |
| Kiểm thử và sửa lỗi | PM & Developer | 2 ngày | Test Reports |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm
- Feature Integration Review: Đánh giá việc tích hợp các tính năng

### SPRINT 7: THỐNG KÊ VÀ PHÂN TÍCH CƠ BẢN (2 tuần)

**Mục tiêu**: Phát triển tính năng thống kê số nóng/lạnh và biểu đồ trực quan

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Thiết kế màn hình thống kê | UX/UI | 3 ngày | UI Design (Figma) |
| Phát triển thuật toán phân tích | Developer | 4 ngày | Analysis Algorithms |
| Phát triển biểu đồ trực quan | Developer | 4 ngày | Chart Components |
| Phát triển lịch sử kết quả | Developer | 3 ngày | Historical Data Feature |
| Kiểm thử và sửa lỗi | PM & Developer | 2 ngày | Test Reports |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Data Visualization Workshop: Thảo luận về cách hiển thị dữ liệu
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm

### SPRINT 8: HOÀN THIỆN UX & BETA TESTING (2 tuần)

**Mục tiêu**: Hoàn thiện trải nghiệm người dùng và chuẩn bị cho Beta Testing

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Tối ưu hóa UI/UX tổng thể | UX/UI | 4 ngày | UI Refinements |
| Phát triển tùy chỉnh thông báo | Developer | 3 ngày | Notification Settings |
| Phát triển hồ sơ người dùng | Developer | 3 ngày | User Profile |
| Chuẩn bị Beta Testing | PM | 2 ngày | Beta Test Plan |
| Kiểm thử và sửa lỗi | PM & Developer | 4 ngày | Test Reports |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- UX Review: Đánh giá toàn diện trải nghiệm người dùng
- Beta Test Planning: Lên kế hoạch cho Beta Testing
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm

### SPRINT 9: BETA TESTING & SỬA LỖI (2 tuần)

**Mục tiêu**: Tiến hành Beta Testing, thu thập phản hồi và sửa lỗi

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Tổ chức Beta Testing | PM | 5 ngày | Beta Test Results |
| Phân tích phản hồi người dùng | PM & UX/UI | 2 ngày | User Feedback Analysis |
| Ưu tiên và sửa lỗi quan trọng | Developer | 5 ngày | Bug Fixes |
| Cập nhật tài liệu | PM | 2 ngày | Updated Documentation |
| Kiểm thử lại | PM & Developer | 2 ngày | Validation Testing |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Beta Feedback Review: Đánh giá phản hồi từ người dùng thử nghiệm
- Bug Triage: Phân loại và ưu tiên sửa lỗi
- Sprint Demo & Retrospective: Demo kết quả và rút kinh nghiệm

### SPRINT 10: PHÁT HÀNH MVP (2 tuần)

**Mục tiêu**: Hoàn thiện cuối cùng và phát hành MVP

**Công việc chi tiết**:

| Công việc | Người phụ trách | Thời gian | Kết quả đầu ra |
| --- | --- | --- | --- |
| Hoàn thiện cuối cùng | Developer | 4 ngày | Final Polishing |
| Chuẩn bị tài liệu người dùng | PM | 2 ngày | User Documentation |
| Tối ưu hóa hiệu suất | Developer | 3 ngày | Performance Optimization |
| Chuẩn bị ASO (App Store Optimization) | PM & UX/UI | 2 ngày | ASO Materials |
| Phát hành MVP | Developer & PM | 2 ngày | MVP Release |
| Lên kế hoạch cho giai đoạn tiếp theo | PM & Owner | 3 ngày | Phase 2 Roadmap |

**Buổi họp chính**:

- Daily Check-in (15 phút mỗi ngày)
- Release Readiness Review: Đánh giá sẵn sàng phát hành
- MVP Launch Meeting: Thảo luận về chiến lược phát hành
- Project Retrospective: Đánh giá toàn bộ giai đoạn MVP
- Phase 2 Planning: Lên kế hoạch cho giai đoạn tiếp theo

## PHẦN 2: MÔ TẢ CÁC CÔNG CỤ VÀ MẪU TÀI LIỆU THỰC TẾ

### 1. Công cụ chính cho dự án

### A. Quản lý dự án và tài liệu

- **Notion**: Trung tâm tài liệu, wiki và quản lý kiến thức
- **Trello**: Bảng Kanban quản lý công việc hàng ngày
- **Google Drive**: Lưu trữ tài liệu và chia sẻ file

### B. Thiết kế và phát triển

- **Figma**: Công cụ thiết kế UI/UX và prototyping
- **GitHub**: Quản lý mã nguồn và version control
- **Firebase**: Backend as a Service (Authentication, Database, Storage)
- **VS Code**: IDE cho phát triển

### C. Giao tiếp và cộng tác

- **Slack**: Giao tiếp nhanh hàng ngày
- **Google Meet**: Họp trực tuyến
- **Loom**: Tạo video hướng dẫn ngắn

### D. Kiểm thử và phân tích

- **TestFlight/Firebase App Distribution**: Phân phối bản beta
- **Firebase Analytics**: Theo dõi hành vi người dùng
- **Sentry**: Tracking lỗi ứng dụng

### 2. Mẫu tài liệu thực tế

### A. Product Requirements Document (PRD)

```markdown
# YÊU CẦU SẢN PHẨM: ỨNG DỤNG SỐ NÀO RA

## 1. Tổng quan
- **Tên sản phẩm**: Số Nào Ra (SoNaoRa)
- **Mô tả**: Ứng dụng hỗ trợ người chơi xổ số tại Việt Nam
- **Tầm nhìn**: Trở thành ứng dụng số 1 cho người chơi xổ số Việt Nam, nơi người dùng có thể dễ dàng theo dõi kết quả, quản lý vé số và nhận gợi ý thông minh

## 2. Đối tượng người dùng
- **Persona chính**: Nguyễn Văn A, 45 tuổi, chơi xổ số truyền thống hàng tuần, không rành công nghệ
- **Persona phụ**: Trần Thị B, 28 tuổi, thỉnh thoảng chơi Vietlott, quen sử dụng smartphone
- **Persona phụ**: Lê Văn C, 35 tuổi, người chơi nghiêm túc, phân tích số liệu trước khi đặt cược

## 3. Mục tiêu kinh doanh
- Đạt 50,000 người dùng trong 3 tháng đầu tiên
- Tỷ lệ giữ chân người dùng >40% sau 30 ngày
- Xây dựng cơ sở người dùng trung thành cho các tính năng trả phí trong tương lai

## 4. Mục tiêu người dùng
- Xem kết quả xổ số nhanh chóng, chính xác
- Quản lý vé số hiệu quả và dễ dàng hơn
- Nhận thông báo kịp thời về kết quả trúng thưởng
- Tiếp cận thông tin phân tích để tăng cơ hội trúng thưởng

## 5. Phạm vi MVP
### 5.1. Trong phạm vi (In-scope)
- Xem kết quả xổ số miền Nam và Vietlott
- Nhập và quản lý vé số
- Chụp và nhận dạng vé số bằng AI
- Dò vé tự động và thông báo kết quả
- Thống kê cơ bản về số nóng/lạnh
- Hệ thống đăng ký/đăng nhập

### 5.2. Ngoài phạm vi (Out-of-scope)
- Mua vé số trực tuyến
- Tính năng cộng đồng và mạng xã hội
- Phân tích nâng cao và dự đoán AI
- Hỗ trợ xổ số miền Trung và miền Bắc
- Tính năng trả phí

## 6. Yêu cầu tính năng
[Chi tiết theo danh sách tính năng đã cung cấp]
...

## 7. Yêu cầu phi chức năng
- **Hiệu suất**: Thời gian phản hồi API < 1 giây, thời gian khởi động ứng dụng < 2 giây
- **Độ tin cậy**: Uptime >99.5%, độ chính xác kết quả xổ số 100%
- **Bảo mật**: Tuân thủ GDPR/PDPA, mã hóa dữ liệu người dùng
- **Khả năng sử dụng**: UI thân thiện với người dùng lớn tuổi, hỗ trợ font chữ lớn

## 8. Rủi ro và Giả định
- **Rủi ro**: Độ chính xác của OCR có thể không đạt yêu cầu
- **Giải pháp**: Kết hợp nhập thủ công và xác nhận kết quả OCR

## 9. Lộ trình phát triển
- **MVP**: Tháng 1-4
- **Giai đoạn 2**: Tháng 5-10
- **Giai đoạn 3**: Tháng 11-22

## 10. Chỉ số thành công (KPIs)
- Số lượng người dùng đăng ký
- Tần suất sử dụng trung bình
- Tỷ lệ chuyển đổi từ chụp vé sang dò vé
- Độ chính xác của OCR
- Điểm hài lòng người dùng (App Rating)

```

### B. User Story Template

```markdown
# USER STORY

## Tiêu đề: Chụp và nhận dạng vé số bằng AI

**ID**: US-2.2
**Mức độ ưu tiên**: Cao
**Độ phức tạp ước tính**: Cao (8 story points)
**Thời gian dự kiến**: 4-5 ngày

### Mô tả
**Là** người chơi xổ số
**Tôi muốn** chụp ảnh vé số và có hệ thống tự động nhận dạng thông tin
**Để** không phải nhập thủ công và tiết kiệm thời gian

### Tiêu chí chấp nhận
- [ ] Ứng dụng cho phép chụp ảnh vé số bằng camera của thiết bị
- [ ] Hệ thống nhận dạng được các loại vé xổ số miền Nam và Vietlott
- [ ] Độ chính xác nhận dạng >85% với vé số rõ nét
- [ ] Người dùng có thể xác nhận hoặc chỉnh sửa thông tin được nhận dạng
- [ ] Thời gian nhận dạng không quá 3 giây
- [ ] Hoạt động được khi không có kết nối internet (lưu ảnh và xử lý sau)

### Luồng người dùng
1. Người dùng chọn "Thêm vé mới" -> "Chụp ảnh"
2. Camera mở và người dùng chụp ảnh vé số
3. Hệ thống xử lý và hiển thị ảnh đã chụp với khung bao quanh vé
4. Người dùng xác nhận khung hoặc điều chỉnh nếu cần
5. Hệ thống nhận dạng và hiển thị thông tin được trích xuất
6. Người dùng xác nhận hoặc sửa thông tin nếu cần
7. Thông tin được lưu vào danh sách vé đã mua

### Mockup/Design
[Link Figma: https://figma.com/file/xxxx]

### Ghi chú kỹ thuật
- Sử dụng API của LLM (OpenAI Vision/Gemini Pro Vision) cho OCR
- Cần tiền xử lý hình ảnh: cắt, xoay, tăng độ tương phản
- Lưu ảnh tạm thời trong Firebase Storage
- Cache kết quả OCR để tránh xử lý lại các vé đã quét trước đó

### Liên quan đến
- US-2.1: Nhập vé thủ công
- US-2.3: Dò vé tự động

```

### C. Sprint Planning Document

```markdown
# KẾ HOẠCH SPRINT 4: CHỤP VÀ NHẬN DẠNG VÉ SỐ (PHẦN 1)

## Thông tin Sprint
- **Sprint**: #4
- **Thời gian**: 24/02/2025 - 09/03/2025 (2 tuần)
- **Story Points**: 21 points
- **Mục tiêu**: Xây dựng nền tảng cho tính năng nhận dạng vé số

## User Stories được chọn
1. **[US-2.2.1]** Nghiên cứu và lựa chọn phương pháp OCR (5 points) - Developer & PM
2. **[US-2.2.2]** Thiết kế UI chụp và nhận dạng vé (3 points) - UX/UI
3. **[US-2.2.3]** Phát triển tính năng chụp ảnh vé số (5 points) - Developer
4. **[US-2.2.4]** Phát triển tiền xử lý hình ảnh (8 points) - Developer

## Chi tiết công việc hàng ngày

### Tuần 1
- **Thứ 2**:
  - PM & Developer: Bắt đầu nghiên cứu OCR options (US-2.2.1)
  - UX/UI: Bắt đầu thiết kế UI (US-2.2.2)
- **Thứ 3**:
  - PM & Developer: Tiếp tục nghiên cứu, đánh giá API LLM (US-2.2.1)
  - UX/UI: Wireframes cho màn hình chụp và nhận dạng (US-2.2.2)
- **Thứ 4**:
  - PM & Developer: Hoàn thành nghiên cứu, chọn giải pháp (US-2.2.1)
  - UX/UI: Prototype tương tác (US-2.2.2)
  - Daily check-in: 9:00 AM
- **Thứ 5**:
  - Developer: Bắt đầu phát triển tính năng chụp ảnh (US-2.2.3)
  - UX/UI: Hoàn thiện thiết kế, chuyển giao cho Developer (US-2.2.2)
  - PM: Viết tài liệu kỹ thuật cho OCR
- **Thứ 6**:
  - Developer: Tiếp tục phát triển tính năng chụp ảnh (US-2.2.3)
  - PM: Chuẩn bị test cases cho tính năng chụp ảnh
  - Team: Demo cuối tuần, đánh giá tiến độ

### Tuần 2
- **Thứ 2**:
  - Developer: Hoàn thiện tính năng chụp ảnh (US-2.2.3)
  - PM: Kiểm thử tính năng chụp ảnh
- **Thứ 3**:
  - Developer: Bắt đầu phát triển tiền xử lý hình ảnh (US-2.2.4)
  - PM: Chuẩn bị dữ liệu test cho tiền xử lý hình ảnh
- **Thứ 4**:
  - Developer: Tiếp tục phát triển tiền xử lý hình ảnh (US-2.2.4)
  - PM: Phối hợp testing và cập nhật tài liệu
  - Daily check-in: 9:00 AM
- **Thứ 5**:
  - Developer: Tiếp tục phát triển tiền xử lý hình ảnh (US-2.2.4)
  - PM: Hỗ trợ testing và debugging
- **Thứ 6**:
  - Developer: Hoàn thiện tiền xử lý hình ảnh (US-2.2.4)
  - PM: Chuẩn bị cho Sprint Review & Retrospective
  - Team: Sprint Demo & Retrospective

## Rủi ro và biện pháp giảm thiểu
- **Rủi ro**: Tính năng tiền xử lý hình ảnh phức tạp hơn dự kiến
  - **Giảm thiểu**: Ưu tiên làm MVP của tính năng trước, hoàn thiện sau
- **Rủi ro**: Chậm tiến độ do phụ thuộc vào API bên ngoài
  - **Giảm thiểu**: Chuẩn bị mock data và API để phát triển độc lập

## Chỉ số đo lường
- Hoàn thành 100% các User Stories đã cam kết
- Độ chính xác tiền xử lý hình ảnh >80% trên mẫu test
- Demo được flow hoàn chỉnh từ chụp ảnh đến tiền xử lý

```

### D. Design Brief

```markdown
# DESIGN BRIEF: TÍNH NĂNG CHỤP VÀ NHẬN DẠNG VÉ SỐ

## 1. Tổng quan
Tính năng này cho phép người dùng chụp ảnh vé số và hệ thống sẽ tự động nhận dạng thông tin trên vé, giúp tiết kiệm thời gian so với nhập thủ công.

## 2. Mục tiêu thiết kế
- Tạo trải nghiệm chụp ảnh đơn giản, trực quan
- Thiết kế giao diện xác nhận thông tin dễ hiểu
- Làm nổi bật thông tin đã nhận dạng để dễ kiểm tra
- Tạo khả năng chỉnh sửa thông tin nhanh chóng
- Đảm bảo người dùng luôn biết đang ở bước nào trong quy trình

## 3. Hành trình người dùng (User Journey)
1. Người dùng chọn "Thêm vé mới" từ màn hình chính
2. Chọn "Chụp ảnh vé" từ menu tùy chọn
3. Chụp ảnh vé số với hướng dẫn căn chỉnh
4. Xác nhận hoặc chụp lại nếu cần
5. Xem kết quả nhận dạng và sửa nếu cần
6. Xác nhận lưu thông tin vé

## 4. Yêu cầu màn hình
### 4.1. Màn hình chụp ảnh
- Khung hướng dẫn vị trí vé số
- Hướng dẫn trực quan về cách chụp tốt nhất
- Nút chụp ảnh lớn, dễ thao tác
- Tùy chọn bật/tắt đèn flash
- Tùy chọn chọn ảnh từ thư viện

### 4.2. Màn hình xác nhận ảnh
- Hiển thị ảnh đã chụp
- Khung bao quanh vé số được nhận diện
- Nút chụp lại và nút tiếp tục
- Thông báo về chất lượng ảnh nếu cần

### 4.3. Màn hình kết quả nhận dạng
- Hiển thị thông tin nhận dạng được: số seri, dãy số, ngày quay
- Trường chỉnh sửa cho mỗi phần thông tin
- Đánh dấu các thông tin chưa chắc chắn
- Nút xác nhận và quay lại

## 5. Nguyên tắc thiết kế
- Sử dụng màu sắc từ style guide chính
- Font chữ lớn, dễ đọc cho người dùng lớn tuổi
- Tối ưu cho thao tác một tay trên điện thoại
- Thời gian phản hồi người dùng không quá 0.1 giây
- Cung cấp phản hồi trực quan (visual feedback) cho mọi thao tác

## 6. Tài nguyên thiết kế
- Link Figma: [https://figma.com/file/xxxx]
- Link Component Library: [https://figma.com/file/yyyy]
- Link Design System: [https://figma.com/file/zzzz]

## 7. Tiêu chí thành công
- Người dùng hoàn thành quá trình chụp và nhận dạng trong <30 giây
- Ít nhất 80% người dùng thử nghiệm có thể hoàn thành tác vụ mà không cần hỗ trợ
- Tỷ lệ lỗi thao tác <5% trong quá trình testing

```

### E. Technical Specification Document

```markdown
# ĐẶC TẢ KỸ THUẬT: TÍNH NĂNG NHẬN DẠNG VÉ SỐ BẰNG OCR

## 1. Tổng quan
Tài liệu này mô tả chi tiết kỹ thuật cho tính năng nhận dạng vé số (OCR) trong ứng dụng Số Nào Ra.

## 2. Kiến trúc hệ thống
### 2.1. Tổng quan

```

┌─────────────┐         ┌─────────────┐         ┌─────────────┐
│  MOBILE APP │         │  FIREBASE   │         │  OCR API    │
│  (Flutter)  │────────►│  SERVICES   │────────►│  (LLM)      │
└─────────────┘         └─────────────┘         └─────────────┘

```

### 2.2. Các thành phần chính
- **Mobile App (Flutter)**:
  - Camera Controller
  - Image Processing Utilities
  - OCR Results Viewer & Editor
- **Firebase Services**:
  - Cloud Storage (lưu trữ hình ảnh tạm thời)
  - Cloud Functions (xử lý OCR)
  - Firestore (lưu kết quả OCR)
- **OCR API (LLM)**:
  - API của OpenAI Vision hoặc Gemini Pro Vision
  - Prompt engineering tối ưu

## 3. Luồng dữ liệu
1. Người dùng chụp ảnh vé số trên mobile app
2. App xử lý ảnh sơ bộ (cropping, enhancement) trên thiết bị
3. Ảnh được tải lên Firebase Storage
4. Cloud Function được trigger để gọi API LLM
5. API LLM phân tích và trả về dữ liệu trích xuất
6. Kết quả được lưu trong Firestore và trả về cho app
7. App hiển thị kết quả để người dùng xác nhận/chỉnh sửa

## 4. Mô tả chi tiết các thành phần

### 4.1. Xử lý ảnh trên thiết bị
- **Thư viện**: image, image_cropper, flutter_image_compress
- **Các bước xử lý**:
  1. Chụp ảnh ở độ phân giải cao (at least 1080p)
  2. Tự động crop vùng chứa vé số
  3. Tăng độ tương phản và khử nhiễu
  4. Nén ảnh trước khi upload (target size <1MB)
- **Code mẫu**:
```dart
Future<File> preprocessImage(File imageFile) async {
  // Crop image
  final croppedFile = await ImageCropper().cropImage(
    sourcePath: imageFile.path,
    aspectRatio: CropAspectRatio(ratioX: 3, ratioY: 1),
    compressQuality: 100,
  );

  // Enhance image
  img.Image? image = img.decodeImage(await croppedFile!.readAsBytes());
  img.Image enhancedImage = img.adjustColor(
    image!,
    contrast: 1.2,
    brightness: 0.05,
  );

  // Compress image
  final compressedData = await FlutterImageCompress.compressWithList(
    img.encodePng(enhancedImage),
    minHeight: 800,
    minWidth: 600,
    quality: 90,
  );

  // Save and return
  final tempDir = await getTemporaryDirectory();
  File processedFile = File('${tempDir.path}/processed_ticket.jpg');
  await processedFile.writeAsBytes(compressedData);
  return processedFile;
}

```

### 4.2. Cloud Function cho OCR

- **Runtime**: Node.js 16
- **Dependencies**: @google-cloud/storage, axios, uuid
- **Flow**:
    1. Trigger khi có file mới trong thư mục tickets/temp
    2. Download image từ Storage
    3. Tạo payload cho API LLM
    4. Gọi API và xử lý response
    5. Lưu kết quả vào Firestore
    6. Trả kết quả về client qua Cloud Messaging
- **Code mẫu**:

```jsx
const functions = require('firebase-functions');
const {Storage} = require('@google-cloud/storage');
const axios = require('axios');
const admin = require('firebase-admin');
const uuid = require('uuid');

admin.initializeApp();
const storage = new Storage();
const db = admin.firestore();

exports.processTicketImage = functions.storage.object().onFinalize(async (object) => {
  // Check if this is a ticket image
  if (!object.name.startsWith('tickets/temp/')) {
    return null;
  }

  // Download image
  const bucketName = object.bucket;
  const filePath = object.name;
  const tempFilePath = `/tmp/${uuid.v4()}`;

  await storage.bucket(bucketName).file(filePath).download({
    destination: tempFilePath
  });

  // Encode image to base64
  const imageBuffer = fs.readFileSync(tempFilePath);
  const base64Image = imageBuffer.toString('base64');

  // Call LLM API
  const response = await axios.post(
    'https://api.openai.com/v1/chat/completions',
    {
      model: "gpt-4-vision-preview",
      messages: [
        {
          role: "user",
          content: [
            {
              type: "text",
              text: "This is a Vietnamese lottery ticket. Please extract the following information: 1) The ticket series number, 2) The lottery numbers, 3) The draw date. Return the extracted information in JSON format with fields: seriesNumber, lotteryNumbers, drawDate"
            },
            {
              type: "image_url",
              image_url: {
                url: `data:image/jpeg;base64,${base64Image}`
              }
            }
          ]
        }
      ],
      max_tokens: 300
    },
    {
      headers: {
        'Authorization': `Bearer ${process.env.OPENAI_API_KEY}`,
        'Content-Type': 'application/json'
      }
    }
  );

  // Parse result
  const content = response.data.choices[0].message.content;
  let ticketData;
  try {
    ticketData = JSON.parse(content);
  } catch (e) {
    // Handle parsing error
    ticketData = {
      error: true,
      message: "Failed to parse result",
      rawContent: content
    };
  }

  // Save result to Firestore
  const userId = object.metadata.userId;
  const ticketId = uuid.v4();
  await db.collection('users').doc(userId).collection('tickets').doc(ticketId).set({
    id: ticketId,
    createdAt: admin.firestore.FieldValue.serverTimestamp(),
    imageUrl: `gs://${bucketName}/${filePath}`,
    ocrResult: ticketData,
    status: 'pending_confirmation'
  });

  // Notify client
  await admin.messaging().send({
    token: object.metadata.fcmToken,
    data: {
      type: 'ocr_completed',
      ticketId: ticketId
    }
  });

  // Delete temp file
  fs.unlinkSync(tempFilePath);

  return null;
});

```

### 4.3. OCR Prompt Engineering

- **Prompt cơ bản**:

```
This is a Vietnamese lottery ticket. Please extract the following information:
1) The ticket series number
2) The lottery numbers
3) The draw date

Return the extracted information in JSON format with fields: seriesNumber, lotteryNumbers, drawDate

```

- **Cải tiến prompt**:

```
This is a Vietnamese lottery ticket image. Please carefully analyze the image and extract the following information:

1) The ticket series number: This is usually a 6-digit number at the top of the ticket, often starting with letters like "AB" or "CD" followed by 4-6 digits.

2) The lottery numbers: These are the main numbers on the ticket, usually 6 digits printed in large font in the center of the ticket.

3) The draw date: This is the date when the lottery will be drawn, usually in format DD/MM/YYYY.

For "Vietlott" tickets (modern computerized tickets):
- Look for 6 numbers between 01-45 (for Mega 6/45) or 6 numbers between 01-55 (for Power 6/55)
- The numbers will be separated and clearly marked

Return the extracted information in this exact JSON format:
{
  "seriesNumber": "string",
  "lotteryNumbers": "string",
  "drawDate": "string",
  "ticketType": "traditional | vietlott",
  "confidence": {
    "seriesNumber": number between 0-1,
    "lotteryNumbers": number between 0-1,
    "drawDate": number between 0-1
  }
}

If you can't clearly read any field, include it as null and set its confidence to 0.

```

## 5. Xử lý kết quả OCR tại Client

- **State Management**: Provider/Bloc
- **UI Validation**:
    - Hiển thị mức độ tin cậy của từng trường
    - Highlight các trường có độ tin cậy thấp
    - Auto-correction cho định dạng số và ngày tháng
- **Error Handling**:
    - Retry logic cho API calls
    - Fallback về nhập thủ công khi OCR thất bại
    - Caching kết quả OCR để tránh xử lý lại cùng một vé

## 6. Yêu cầu hiệu suất

- Thời gian xử lý hình ảnh trên thiết bị: <2 giây
- Thời gian upload và xử lý OCR: <5 giây
- Độ chính xác OCR: >85% cho vé rõ nét, >70% cho vé chất lượng trung bình
- Kích thước hình ảnh tải lên: <1MB

## 7. Kế hoạch kiểm thử

- **Unit Tests**: Kiểm thử các hàm xử lý ảnh, parsing kết quả OCR
- **Integration Tests**: Kiểm thử flow từ chụp ảnh đến hiển thị kết quả
- **Dataset Testing**: Kiểm thử với 100+ mẫu vé số khác nhau
- **User Testing**: Theo dõi tỷ lệ thành công và thời gian hoàn thành

## 8. Cân nhắc phát triển trong tương lai

- Caching và offline support cho OCR
- Tối ưu hóa model dựa trên dữ liệu người dùng
- Hỗ trợ scan nhiều vé cùng lúc
- Tùy chỉnh OCR theo từng loại vé cụ thể

```

#### F. Sprint Retrospective

```markdown
# SPRINT RETROSPECTIVE - SPRINT 5

## Thông tin chung
- **Sprint**: #5 - Chụp và nhận dạng vé số (Phần 2)
- **Thời gian**: 10/03/2025 - 23/03/2025
- **Tham dự**: Owner, PM, UX/UI, Developer

## Thành tựu Sprint
- Hoàn thành tích hợp API LLM cho OCR
- Phát triển UI xác nhận kết quả nhận dạng
- Đạt độ chính xác OCR 83% trong testing nội bộ
- Giải quyết được 4 bugs từ sprint trước

## Điều đã làm tốt
- **Developer**: Tối ưu hóa prompt OCR đã cải thiện độ chính xác từ 65% lên 83%
- **UX/UI**: Thiết kế màn hình xác nhận OCR trực quan và dễ hiểu
- **PM**: Cung cấp test dataset đa dạng giúp kiểm thử toàn diện
- **Team**: Giao tiếp tốt và giải quyết nhanh các vấn đề kỹ thuật

## Điều cần cải thiện
- **Ước tính thời gian**: Tích hợp API OCR mất nhiều thời gian hơn dự kiến (5 ngày thay vì 3 ngày)
- **Hiệu suất API**: Thời gian phản hồi OCR đôi khi chậm (>8 giây)
- **Quản lý dependencies**: Một số cập nhật thư viện gây ra conflicts
- **Phạm vi công việc**: Feature creep khi thêm tính năng highlight từng số trên ảnh

## Hành động cụ thể cho Sprint tiếp theo
- [ ] **PM**: Thêm buffer 30% cho ước tính thời gian các tính năng phức tạp - *Sprint 6*
- [ ] **Developer**: Thêm caching cho kết quả OCR để cải thiện hiệu suất - *Sprint 6*
- [ ] **Developer**: Thiết lập quy trình kiểm tra dependencies trước khi cập nhật - *Ngay lập tức*
- [ ] **PM & UX/UI**: Tạo backlog tính năng cải tiến OCR thay vì thêm vào sprint hiện tại - *Sprint Planning*
- [ ] **Team**: Tổ chức "Tech Talk" 30 phút về prompt engineering để chia sẻ kiến thức - *Tuần tới*

## Chỉ số Sprint
- **Cam kết**: 21 story points
- **Hoàn thành**: 19 story points (90%)
- **Bugs phát hiện**: 7
- **Bugs đã sửa**: 6 (1 được đưa sang Sprint tiếp theo)
- **Tốc độ trung bình (velocity)**: 18.5 points (trung bình 2 sprint gần nhất)

## Bài học chính
- Prompt engineering là yếu tố quyết định cho độ chính xác OCR với API LLM
- Nên tách tính năng OCR thành nhiều phần nhỏ để dễ quản lý và cải tiến
- Team hoạt động hiệu quả hơn khi focus vào một tính năng phức tạp thay vì nhiều tính năng đơn giản

## Kế hoạch cải tiến quy trình
- Cập nhật template User Story để thêm phần "Technical Dependencies"
- Tạo thư viện các prompt OCR cho nhiều loại vé số khác nhau
- Thiết lập monitoring cho API calls để theo dõi hiệu suất

```

### G. Product Backlog

```markdown
# PRODUCT BACKLOG - SỐ NÀO RA

## MVP (Giai đoạn 1)

### THEME: Xem kết quả xổ số
| ID | User Story | Độ ưu tiên | Độ phức tạp | Sprint |
|----|------------|------------|-------------|--------|
| US-1.1 | Xem kết quả xổ số miền Nam | Cao | Thấp | 1 |
| US-1.2 | Xem kết quả Vietlott | Cao | Thấp | 2 |
| US-1.3 | Xem lịch quay thưởng | Cao | Thấp | 2 |
| US-1.4 | Nhận thông báo kết quả | Cao | Trung bình | 3 |

### THEME: Công cụ dò vé số
| ID | User Story | Độ ưu tiên | Độ phức tạp | Sprint |
|----|------------|------------|-------------|--------|
| US-2.1 | Nhập vé thủ công | Cao | Thấp | 3 |
| US-2.2 | Chụp và nhận dạng vé số | Cao | Cao | 4-5 |
| US-2.3 | Dò vé tự động | Cao | Trung bình | 6 |
| US-2.4 | Quản lý vé đã mua | Cao | Trung bình | 6 |

### THEME: Thống kê và phân tích
| ID | User Story | Độ ưu tiên | Độ phức tạp | Sprint |
|----|------------|------------|-------------|--------|
| US-3.1 | Xem thống kê số nóng/lạnh | Trung bình | Trung bình | 7 |
| US-3.2 | Xem biểu đồ trực quan | Trung bình | Trung bình | 7 |
| US-3.3 | Xem lịch sử kết quả | Trung bình | Thấp | 7 |

### THEME: Trải nghiệm người dùng
| ID | User Story | Độ ưu tiên | Độ phức tạp | Sprint |
|----|------------|------------|-------------|--------|
| US-4.1 | Đăng ký/đăng nhập | Cao | Trung bình | 1 |
| US-4.2 | Giao diện người dùng cơ bản | Cao | Trung bình | 1-2 |
| US-4.3 | Tùy chỉnh thông báo | Trung bình | Trung bình | 8 |
| US-4.4 | Quản lý hồ sơ người dùng | Trung bình | Thấp | 8 |

## Giai đoạn 2 (4-6 tháng sau MVP)

### THEME: Phân tích nâng cao
| ID | User Story | Độ ưu tiên | Độ phức tạp | Sprint |
|----|------------|------------|-------------|--------|
| US-5.1 | AI gợi ý số | Cao | Cao | TBD |
| US-5.2 | Phân tích mẫu số | Trung bình | Cao | TBD |
| US-5.3 | Thống kê chi tiết | Trung bình | Trung bình | TBD |
| US-5.4 | Xuất dữ liệu kèm prompt | Trung bình | Thấp | TBD |

(Các phần còn lại của backlog được phát triển tương tự...)

## Mức độ ưu tiên
- **Cao**: Tính năng thiết yếu, ảnh hưởng lớn đến trải nghiệm người dùng
- **Trung bình**: Tính năng quan trọng nhưng có thể triển khai sau
- **Thấp**: Tính năng bổ sung, cải thiện trải nghiệm nhưng không thiết yếu

## Độ phức tạp
- **Cao**: 8+ story points, thường mất >1 sprint
- **Trung bình**: 3-7 story points
- **Thấp**: 1-2 story points, tính năng đơn giản

```

### H. Definition of Done

```markdown
# DEFINITION OF DONE - DỰ ÁN SỐ NÀO RA

## Tính năng được coi là "DONE" khi đáp ứng TẤT CẢ các tiêu chí sau:

### Tiêu chí phát triển
- [ ] Code đã được viết theo yêu cầu từ User Story
- [ ] Code tuân thủ coding standards đã thống nhất
- [ ] Unit tests đã được viết và pass (coverage >80%)
- [ ] Code đã được review bởi ít nhất 1 thành viên khác
- [ ] Tất cả comments trong PR đã được giải quyết
- [ ] Code đã được merge vào nhánh develop

### Tiêu chí thiết kế
- [ ] UI triển khai đúng theo design từ Figma
- [ ] Responsive trên cả mobile (cả iPhone và Android)
- [ ] Đảm bảo tính nhất quán với Design System
- [ ] Đáp ứng các tiêu chí về accessibility cơ bản
- [ ] Được UX/UI Designer xác nhận

### Tiêu chí kiểm thử
- [ ] Tất cả tiêu chí chấp nhận (acceptance criteria) đều pass
- [ ] Tích hợp tốt với các tính năng hiện có
- [ ] Không có bugs nghiêm trọng (P0, P1)
- [ ] Hiệu suất đạt yêu cầu (load time, memory usage)
- [ ] Được test trên ít nhất 3 thiết bị khác nhau

### Tiêu chí tài liệu
- [ ] Tài liệu kỹ thuật đã được cập nhật
- [ ] User Story đã được đánh dấu là "Complete" trong Trello
- [ ] Release notes đã được cập nhật (nếu cần)
- [ ] Hướng dẫn sử dụng đã được cập nhật (nếu cần)

### Tiêu chí triển khai
- [ ] Tính năng đã được triển khai lên môi trường staging
- [ ] Smoke test trên staging đã pass
- [ ] PM đã verify và sign-off
- [ ] Không có regression trên các tính năng khác

## Checklist bổ sung cho các loại tính năng đặc biệt

### Tính năng AI/OCR
- [ ] Đạt độ chính xác theo yêu cầu (>85% cho vé rõ nét)
- [ ] Có cơ chế backup khi AI/OCR thất bại
- [ ] Đã test với nhiều loại vé số khác nhau

### Tính năng thống kê/phân tích
- [ ] Thuật toán phân tích đã được verify về tính chính xác
- [ ] Biểu đồ hiển thị tốt trên các kích thước màn hình
- [ ] Hiệu suất tốt với dữ liệu lớn

### Tính năng đăng ký/đăng nhập
- [ ] Tuân thủ các tiêu chuẩn bảo mật
- [ ] Có cơ chế khôi phục mật khẩu
- [ ] Validation đúng cho các trường dữ liệu

```

Trên đây là kế hoạch triển khai chi tiết và các mẫu tài liệu thực tế cho dự án Số Nào Ra. Các tài liệu này đã được thiết kế phù hợp với quy mô team 4 người và tập trung vào tính hiệu quả, dễ triển khai, đồng thời đảm bảo chất lượng sản phẩm cuối cùng.
