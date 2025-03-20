## THÔNG TIN CƠ BẢN

- **Tên dự án:** Số Nào Ra (SoNaoRa)
- **Người sở hữu:** Ban quản lý dự án
- **Ngày tạo:** 19/03/2025
- **Ngày cập nhật:** 19/03/2025

## 1. TẦM NHÌN VÀ MỤC TIÊU

### 1.1. Tầm nhìn tổng thể

Số Nào Ra sẽ trở thành ứng dụng hàng đầu tại Việt Nam dành cho người chơi xổ số, nơi người dùng có thể dễ dàng theo dõi kết quả, quản lý vé số thông minh và tiếp cận các phân tích dữ liệu giúp tăng cơ hội trúng thưởng. Ứng dụng hướng tới việc tạo ra một cộng đồng sôi động, nơi người chơi xổ số có thể kết nối và chia sẻ kinh nghiệm.

### 1.2. Mục tiêu cụ thể

1. Phát hành MVP đúng hạn vào ngày 15/05/2025 với các tính năng cốt lõi hoạt động ổn định.
2. Đạt 20.000 người dùng trong tháng đầu tiên sau khi ra mắt MVP, với tỷ lệ giữ chân người dùng (retention rate) trên 35% sau 30 ngày.
3. Hoàn thiện tính năng xem kết quả xổ số miền Nam và Vietlott với thời gian cập nhật dưới 2 phút sau khi có kết quả chính thức.
4. Phát triển tính năng nhập vé thủ công và dò vé tự động với tỷ lệ chính xác 100%.
5. Tạo nền tảng kỹ thuật vững chắc để bổ sung tính năng OCR nhận dạng vé số trong bản cập nhật tiếp theo.

### 1.3. Vấn đề cần giải quyết

Người chơi xổ số tại Việt Nam hiện đang gặp phải nhiều khó khăn như: quản lý vé số mua thủ công không hiệu quả, mất thời gian kiểm tra kết quả, thiếu thông tin phân tích để lựa chọn số, và không có không gian cộng đồng uy tín để chia sẻ kinh nghiệm. Số Nào Ra giải quyết các vấn đề này thông qua nền tảng số hóa toàn diện, giúp người chơi tối ưu hóa trải nghiệm chơi xổ số, tiết kiệm thời gian và tăng cơ hội trúng thưởng.

## 2. THÔNG TIN SẢN PHẨM

### 2.1. Loại sản phẩm

- [x]  Ứng dụng cross-platform (Flutter)

### 2.2. Phạm vi dự án (MVP - 15/05/2025)

**Trong phạm vi MVP:**

- Xem kết quả xổ số miền Nam và Vietlott theo thời gian thực
- Lịch quay thưởng và thông báo kết quả cơ bản
- Nhập và quản lý vé số thủ công
- Dò vé tự động và hiển thị kết quả trúng thưởng
- Hệ thống đăng ký/đăng nhập cơ bản
- Giao diện người dùng thân thiện, dễ sử dụng

**Trong phạm vi giai đoạn tiếp theo (sau MVP):**

- Chụp và nhận dạng vé số bằng AI/OCR
- Thống kê số "nóng"/"lạnh" và biểu đồ trực quan
- Tính năng cộng đồng cơ bản
- Hồ sơ người dùng chi tiết và tùy chỉnh giao diện

**Ngoài phạm vi:**

- Hỗ trợ xổ số miền Trung và miền Bắc
- Tính năng cộng đồng nâng cao
- Thanh toán và giao dịch tài chính
- Phát trực tiếp sự kiện quay thưởng

### 2.3. Đối tượng người dùng

- **Người chơi xổ số truyền thống:**
    - Đặc điểm nhân khẩu học: 35-60 tuổi, thu nhập trung bình, thường xuyên mua vé số truyền thống, ít thành thạo công nghệ
    - Nhu cầu/vấn đề: Muốn dễ dàng theo dõi kết quả xổ số, quản lý vé đã mua, và không bỏ lỡ cơ hội trúng thưởng
    - Kỳ vọng: Giao diện đơn giản, dễ sử dụng, thông báo kết quả nhanh chóng, chính xác
- **Người chơi xổ số điện toán Vietlott:**
    - Đặc điểm nhân khẩu học: 25-45 tuổi, thu nhập khá, sống tại thành thị, thành thạo công nghệ
    - Nhu cầu/vấn đề: Theo dõi jackpot lớn, quản lý nhiều vé Vietlott
    - Kỳ vọng: Thông tin chính xác, cập nhật nhanh, công cụ quản lý vé dễ sử dụng
- **Người chơi mới:**
    - Đặc điểm nhân khẩu học: 18-30 tuổi, sinh viên hoặc người đi làm trẻ, hiếu kỳ về xổ số nhưng chưa thường xuyên chơi
    - Nhu cầu/vấn đề: Tìm hiểu cách chơi xổ số, muốn trải nghiệm thử cơ hội
    - Kỳ vọng: Giao diện hiện đại, hướng dẫn dễ hiểu, thông tin đầy đủ về các loại hình xổ số

## 3. YÊU CẦU BAN ĐẦU

### 3.1. Tính năng chính (MVP)

1. **Xem kết quả xổ số:** Hiển thị kết quả đầy đủ của xổ số miền Nam (21 tỉnh) và Vietlott (Mega 6/45, Power 6/55, Max 3D, Max 4D), cập nhật theo thời gian thực
2. **Lịch quay thưởng:** Hiển thị lịch quay thưởng chi tiết theo ngày, giờ và đài quay thưởng
3. **Thông báo kết quả cơ bản:** Gửi thông báo sau khi có kết quả xổ số
4. **Nhập vé thủ công:** Giao diện nhập vé trực quan, dễ sử dụng, hỗ trợ nhiều loại vé số
5. **Dò vé tự động:** Tự động so khớp với kết quả mới nhất, tính toán giải thưởng nếu trúng
6. **Quản lý vé đã mua:** Lưu trữ và phân loại vé số, hiển thị trạng thái dò và kết quả trúng thưởng
7. **Đăng ký/đăng nhập cơ bản:** Xác thực qua email hoặc số điện thoại

### 3.2. Yêu cầu phi chức năng

- **Hiệu suất:** Thời gian phản hồi API < 2 giây, thời gian khởi động ứng dụng < 3 giây
- **Bảo mật:** Bảo vệ thông tin người dùng, tuân thủ quy định về bảo vệ dữ liệu cá nhân của Việt Nam
- **Trải nghiệm người dùng:** Giao diện thân thiện với mọi lứa tuổi, hỗ trợ font chữ lớn cho người dùng lớn tuổi
- **Độ tin cậy:** Ứng dụng ổn định, ít lỗi, kết quả xổ số chính xác 100%
- **Khả năng mở rộng:** Kiến trúc cho phép dễ dàng bổ sung tính năng mới trong các phiên bản sau

### 3.3. Ràng buộc

- **Thời gian:** Phát triển MVP trong vòng 8 tuần, phát hành vào 15/05/2025
- **Công nghệ:** Sử dụng Flutter cho phát triển cross-platform, Firebase cho backend
- **Nhân sự:** Team 4 người gồm PM, Developer, UX/UI Designer, và QA
- **Ưu tiên hóa:** Tập trung vào tính năng cốt lõi, đảm bảo ổn định và trải nghiệm người dùng tốt thay vì nhiều tính năng
- **Quy định pháp lý:** Tuân thủ quy định về hoạt động xổ số của Việt Nam

## 4. THÔNG TIN TRIỂN KHAI

### 4.1. Thời gian dự kiến

- **Ngày bắt đầu:** 20/03/2025
- **Ngày phát hành MVP:** 15/05/2025
- **Tổng thời gian:** 8 tuần

### 4.2. Các cột mốc chính

1. **Hoàn thành thiết kế UI/UX và kiến trúc hệ thống:** 27/03/2025 - Kết thúc tuần 1
2. **Hoàn thành tính năng xem kết quả xổ số và lịch quay thưởng:** 10/04/2025 - Kết thúc tuần 3
3. **Hoàn thành tính năng đăng ký/đăng nhập và nhập vé thủ công:** 24/04/2025 - Kết thúc tuần 5
4. **Hoàn thành tính năng dò vé tự động và quản lý vé đã mua:** 01/05/2025 - Kết thúc tuần 6
5. **Hoàn tất testing và sửa lỗi:** 08/05/2025 - Kết thúc tuần 7
6. **Chuẩn bị phát hành và triển khai lên cửa hàng ứng dụng:** 15/05/2025 - Kết thúc tuần 8

### 4.3. Tiêu chí thành công

1. Phát hành đúng hạn vào ngày 15/05/2025 với tất cả tính năng MVP hoạt động ổn định
2. Đạt 20.000 lượt tải ứng dụng trong tháng đầu tiên sau khi ra mắt
3. Tỷ lệ giữ chân người dùng (retention rate) > 35% sau 30 ngày sử dụng
4. Điểm đánh giá ứng dụng trên cửa hàng ứng dụng > 4.3/5 sao
5. Tỷ lệ sự cố và lỗi (crash rate) < 1%
6. 60% người dùng sử dụng ít nhất 3 tính năng chính của ứng dụng

## 5. THÔNG TIN BỔ SUNG

### 5.1. Tài nguyên hiện có

- Stack công nghệ đã được xác định: Flutter, Firebase
- Thiết kế UI Style Guide và Component Library
- Dữ liệu thống kê về kết quả xổ số lịch sử
- Kiến thức chuyên sâu về thị trường xổ số Việt Nam
- Mô hình kiến trúc hệ thống đã được thiết kế
- Phân tích chi tiết về thị trường và đối tượng người dùng

### 5.2. Đối thủ cạnh tranh

- **Vietlott SMS:** Ứng dụng chính thức của Vietlott - SoNaoRa khác biệt với khả năng tích hợp cả xổ số truyền thống và Vietlott
- **Các ứng dụng xem kết quả xổ số hiện có:** SoNaoRa khác biệt với tính năng quản lý vé và dò vé tự động
- **Trang web xem kết quả xổ số:** SoNaoRa khác biệt với trải nghiệm mobile tối ưu và khả năng quản lý vé số cá nhân

### 5.3. Ghi chú bổ sung

Thị trường xổ số Việt Nam đang tăng trưởng mạnh với doanh thu năm 2023 đạt 153.037 tỷ đồng, tăng 11% so với năm 2022. Đặc biệt, xổ số miền Nam chiếm đến 93,3% thị phần toàn quốc, là thị trường mục tiêu chính của Số Nào Ra trong giai đoạn MVP.

Với thời gian phát triển ngắn (8 tuần), chúng ta sẽ tập trung vào các tính năng cốt lõi mang lại giá trị nhanh nhất cho người dùng. Tính năng OCR nhận dạng vé số - điểm khác biệt quan trọng của Số Nào Ra - sẽ được phát triển ngay trong bản cập nhật đầu tiên sau MVP, dự kiến trong tháng 6/2025.

Chiến lược phát triển "thin slice" sẽ được áp dụng, đảm bảo mỗi tính năng đều được hoàn thiện đầy đủ từ UI đến backend, thay vì triển khai nhiều tính năng nhưng chưa hoàn chỉnh.

---

## PHẦN DÀNH CHO PM AGENT

### Câu hỏi làm rõ:

1. Liệu tiến độ 8 tuần có quá gấp rút cho việc phát triển cả phần xem kết quả xổ số và quản lý vé không? Có nên ưu tiên ra mắt chỉ với tính năng xem kết quả trước không?
2. Có cần chuẩn bị kế hoạch dự phòng nếu không kịp phát triển tất cả tính năng MVP vào ngày 15/05?
3. Kế hoạch marketing và user acquisition cụ thể để đạt mục tiêu 20.000 lượt tải trong tháng đầu là gì?
4. Kế hoạch cập nhật và lộ trình phát triển chi tiết sau MVP đã được xác định chưa?
5. Chiến lược thu thập phản hồi người dùng trong giai đoạn beta testing (1 tuần cuối) là gì?

### Các rủi ro tiềm ẩn:

1. **Rủi ro tiến độ:** Lịch trình 8 tuần khá gấp rút cho việc phát triển toàn bộ tính năng MVP và có thể dẫn đến nợ kỹ thuật.
2. **Rủi ro chất lượng:** Áp lực thời gian có thể ảnh hưởng đến chất lượng code và trải nghiệm người dùng.
3. **Rủi ro kỹ thuật:** Tích hợp API lấy kết quả xổ số có thể phức tạp hơn dự kiến, đặc biệt khi cần đảm bảo dữ liệu chính xác 100%.
4. **Rủi ro UX:** Giao diện đơn giản có thể không đủ hấp dẫn để cạnh tranh với các ứng dụng hiện có.
5. **Rủi ro thị trường:** Thời gian marketing và chuẩn bị ra mắt ngắn có thể ảnh hưởng đến lượng người dùng ban đầu.

### Đề xuất:

1. **Áp dụng phương pháp phát triển MVP hai giai đoạn:**
    - **MVP Phase 1 (15/05):** Tập trung vào tính năng xem kết quả xổ số, lịch quay thưởng và thông báo
    - **MVP Phase 2 (01/06):** Bổ sung tính năng nhập và quản lý vé số, dò vé tự động
2. **Tối ưu hóa quy trình phát triển:**
    - Sử dụng các thư viện và template có sẵn để tăng tốc quá trình phát triển UI
    - Ưu tiên sử dụng Firebase Functions để giảm thời gian phát triển backend
    - Triển khai CI/CD từ sớm để tự động hóa quy trình testing và deployment
3. **Chuẩn bị chiến lược marketing trước khi phát hành:**
    - Xây dựng landing page và tài khoản mạng xã hội từ tuần 3-4
    - Tiếp cận các nhóm cộng đồng người chơi xổ số từ tuần 5-6
    - Chuẩn bị chiến dịch quảng cáo Facebook/Google trước khi ra mắt 2 tuần
4. **Xây dựng kế hoạch phản hồi nhanh sau khi phát hành:**
    - Thiết lập hệ thống thu thập phản hồi trong ứng dụng
    - Chuẩn bị sẵn sàng đội ngũ để xử lý và phản hồi đánh giá người dùng
    - Lên kế hoạch phát hành bản cập nhật đầu tiên trong vòng 2 tuần sau MVP
5. **Tập trung vào trải nghiệm người dùng đơn giản nhưng hiệu quả:**
    - Ưu tiên tính dễ sử dụng và tốc độ hơn là thiết kế phức tạp
    - Đảm bảo thông tin kết quả xổ số luôn chính xác và cập nhật nhanh
    - Thiết kế giao diện người dùng thân thiện với người lớn tuổi từ đầu
