# Phân tích yêu cầu chi tiết: ỨNG DỤNG SỐ NÀO RA (SONAORA)

## 1. Tổng quan

- **Tên sản phẩm**: Số Nào Ra (SoNaoRa)
- **Mô tả**: Ứng dụng hỗ trợ toàn diện cho người chơi xổ số tại Việt Nam, tập trung vào việc xem kết quả, dò vé thông minh và phân tích số liệu
- **Tầm nhìn**: Trở thành ứng dụng số 1 cho người chơi xổ số Việt Nam, nơi người dùng có thể dễ dàng theo dõi kết quả, quản lý vé số, nhận gợi ý thông minh và kết nối với cộng đồng

## 2. Đối tượng người dùng

- **Persona chính**: Nguyễn Văn A, 45 tuổi, chơi xổ số truyền thống miền Nam hàng tuần, không rành công nghệ, mua vé số từ người bán dạo, cần một cách dễ dàng để dò vé và xem kết quả
- **Persona phụ**: Trần Thị B, 28 tuổi, thỉnh thoảng chơi Vietlott, quen sử dụng smartphone, ưa thích trải nghiệm số và muốn có công cụ phân tích trước khi chọn số
- **Persona phụ**: Lê Văn C, 35 tuổi, người chơi nghiêm túc, phân tích số liệu trước khi đặt cược, chơi cả xổ số truyền thống và Vietlott, cần công cụ thống kê chuyên sâu

## 3. Mục tiêu kinh doanh

- Đạt 50.000 người dùng trong 3 tháng đầu tiên
- Tỷ lệ giữ chân người dùng >40% sau 30 ngày
- Xây dựng cơ sở người dùng trung thành cho các tính năng trả phí trong tương lai
- Tạo dựng thương hiệu uy tín trong lĩnh vực ứng dụng xổ số
- Thiết lập nền tảng để mở rộng sang các mô hình kinh doanh khác trong tương lai

## 4. Mục tiêu người dùng

- Xem kết quả xổ số nhanh chóng, chính xác
- Quản lý vé số hiệu quả và dễ dàng hơn
- Nhận thông báo kịp thời về kết quả trúng thưởng
- Tiếp cận thông tin phân tích để tăng cơ hội trúng thưởng
- Tiết kiệm thời gian so với cách dò vé thủ công truyền thống

## 5. Phạm vi MVP

### 5.1. Trong phạm vi (In-scope)

- Xem kết quả xổ số miền Nam và Vietlott
- Nhập và quản lý vé số
- Chụp và nhận dạng vé số bằng AI
- Dò vé tự động và thông báo kết quả
- Thống kê cơ bản về số nóng/lạnh
- Hệ thống đăng ký/đăng nhập
- Lịch quay thưởng chi tiết
- Giao diện người dùng đơn giản, phù hợp với người lớn tuổi

### 5.2. Ngoài phạm vi (Out-of-scope)

- Mua vé số trực tuyến
- Tính năng cộng đồng và mạng xã hội
- Phân tích nâng cao và dự đoán AI
- Hỗ trợ xổ số miền Trung và miền Bắc
- Tính năng trả phí
- Thanh toán trong ứng dụng
- Tích hợp với đại lý xổ số

## 6. Yêu cầu tính năng

### 6.1. Xem kết quả xổ số

- **Kết quả xổ số miền Nam**:
    - Hiển thị kết quả đầy đủ của 21 tỉnh miền Nam
    - Hiển thị tất cả các giải từ Đặc biệt đến giải Tám
    - Hiển thị giải phụ đặc biệt và giải khuyến khích
    - Cập nhật kết quả theo thời gian thực sau khi có kết quả quay số (16h10 hàng ngày)
    - Lưu trữ lịch sử kết quả tối thiểu 6 tháng
    - Tìm kiếm kết quả theo ngày và tỉnh thành
- **Kết quả Vietlott**:
    - Hiển thị kết quả Mega 6/45, Power 6/55, Max 3D, Max 3D Pro, Max 4D, Keno
    - Hiển thị thông tin giá trị Jackpot hiện tại và lịch sử
    - Hiển thị cơ cấu giải thưởng chi tiết
    - Cập nhật theo lịch quay thưởng của từng loại hình
- **Lịch quay thưởng**:
    - Hiển thị lịch quay thưởng chi tiết theo ngày, giờ cho cả xổ số truyền thống và Vietlott
    - Lọc lịch theo khu vực/loại hình xổ số
    - Nhắc nhở tự động trước khi quay thưởng
- **Thông báo kết quả**:
    - Gửi thông báo ngay sau khi có kết quả
    - Cho phép tùy chỉnh loại thông báo theo sở thích
    - Hỗ trợ tùy chỉnh thời gian nhận thông báo

### 6.2. Công cụ dò vé số

- **Nhập vé thủ công**:
    - Giao diện nhập vé trực quan, dễ sử dụng
    - Hỗ trợ nhiều loại vé số (truyền thống miền Nam, các loại Vietlott)
    - Kiểm tra tính hợp lệ của số vé
    - Cho phép lưu vé vào danh sách theo dõi
- **Chụp và nhận dạng vé số**:
    - Sử dụng camera để chụp ảnh vé số
    - Ứng dụng OCR qua API của LLM để nhận dạng thông tin trên vé
    - Hỗ trợ chỉnh sửa kết quả nhận dạng nếu không chính xác
    - Tự động lưu vé đã nhận dạng vào danh sách theo dõi
    - Độ chính xác nhận dạng >85% với vé số rõ nét
- **Dò vé tự động**:
    - Tự động so khớp vé đã lưu với kết quả mới nhất
    - Tính toán giá trị giải thưởng nếu trúng
    - Thông báo ngay lập tức khi có vé trúng thưởng
    - Hỗ trợ dò vé theo lô, theo cặp, hoặc theo dạng bảo đảm
- **Quản lý vé đã mua**:
    - Lưu trữ và phân loại vé số theo loại, ngày mua, ngày quay
    - Hiển thị trạng thái dò (đã dò/chưa dò) và kết quả trúng thưởng
    - Cho phép xóa, chỉnh sửa thông tin vé
    - Tìm kiếm nhanh trong danh sách vé đã lưu

### 6.3. Thống kê cơ bản

- **Thống kê số "nóng"/"lạnh"**:
    - Phân tích tần suất xuất hiện của các con số
    - Phân loại số nóng/lạnh dựa trên tần suất xuất hiện
    - Hiển thị xu hướng biến động qua các kỳ quay số
- **Biểu đồ trực quan**:
    - Hiển thị dữ liệu thống kê dưới dạng biểu đồ
    - Cho phép tương tác (zoom, filter) với biểu đồ
    - Hỗ trợ xuất dữ liệu biểu đồ
- **Lịch sử kết quả**:
    - Dữ liệu kết quả xổ số 6-12 tháng gần nhất
    - Hỗ trợ tìm kiếm và lọc theo nhiều tiêu chí
    - Hiển thị thống kê tổng hợp theo thời gian

### 6.4. Trải nghiệm người dùng

- **Đăng ký/đăng nhập**:
    - Xác thực qua email hoặc số điện thoại
    - Hỗ trợ đăng nhập qua tài khoản mạng xã hội
    - Quy trình đăng ký đơn giản, ít bước
- **Giao diện người dùng**:
    - UI/UX thân thiện với mọi lứa tuổi
    - Hỗ trợ chế độ tối (dark mode)
    - Font chữ rõ ràng, kích thước có thể điều chỉnh
    - Bố cục hợp lý, dễ điều hướng
- **Tùy chỉnh thông báo**:
    - Cấu hình loại thông báo (kết quả, trúng thưởng, lịch quay)
    - Thiết lập thời gian và tần suất nhận thông báo
    - Tắt/bật thông báo cho từng loại xổ số
- **Hồ sơ người dùng**:
    - Quản lý thông tin cá nhân cơ bản
    - Theo dõi lịch sử hoạt động
    - Đồng bộ dữ liệu giữa các thiết bị

## 7. Yêu cầu phi chức năng

- **Hiệu suất**:
    - Thời gian phản hồi API < 1 giây
    - Thời gian khởi động ứng dụng < 2 giây
    - Xử lý OCR vé số < 3 giây/vé
    - Dung lượng ứng dụng < 30MB
    - Sử dụng tài nguyên hệ thống tối thiểu
- **Độ tin cậy**:
    - Uptime >99.5%
    - Độ chính xác kết quả xổ số 100%
    - Độ chính xác OCR >85% với vé số rõ nét
    - Tự động khôi phục sau lỗi
    - Sao lưu dữ liệu người dùng định kỳ
- **Bảo mật**:
    - Tuân thủ quy định về bảo vệ dữ liệu cá nhân (PDPA)
    - Mã hóa dữ liệu người dùng
    - Xác thực an toàn, mạnh mẽ
    - Bảo vệ thông tin cá nhân và tài chính
- **Khả năng sử dụng**:
    - UI thân thiện với người dùng lớn tuổi
    - Hỗ trợ font chữ lớn và điều chỉnh độ tương phản
    - Hướng dẫn sử dụng trong ứng dụng
    - Thời gian học sử dụng ứng dụng < 5 phút
- **Khả năng mở rộng**:
    - Kiến trúc cho phép dễ dàng thêm tính năng mới
    - Hỗ trợ tăng số lượng người dùng mà không làm giảm hiệu suất
    - Chuẩn bị sẵn sàng cho việc mở rộng khu vực (miền Trung, miền Bắc)

## 8. Rủi ro và Giả định

- **Rủi ro**: Độ chính xác của OCR có thể không đạt yêu cầu với vé số nhàu nát, mờ hoặc chụp không rõ
    - **Giải pháp**: Kết hợp nhập thủ công và xác nhận kết quả OCR, hướng dẫn người dùng cách chụp vé số để đạt kết quả tốt nhất
- **Rủi ro**: Chi phí API của LLM có thể tăng cao khi số lượng người dùng tăng
    - **Giải pháp**: Thiết lập hạn ngạch sử dụng, tối ưu hóa prompt, chuẩn bị phương án chuyển đổi sang giải pháp OCR khác
- **Rủi ro**: Cạnh tranh từ các ứng dụng tương tự trên thị trường
    - **Giải pháp**: Tập trung vào trải nghiệm người dùng vượt trội, độ chính xác cao và các tính năng độc đáo
- **Rủi ro**: Quy định pháp luật về xổ số có thể thay đổi
    - **Giải pháp**: Theo dõi chặt chẽ các thay đổi pháp lý, thiết kế ứng dụng linh hoạt để dễ dàng điều chỉnh
- **Giả định**: Người dùng lớn tuổi sẽ sử dụng ứng dụng nếu giao diện đủ đơn giản và trực quan
- **Giả định**: Người chơi xổ số quan tâm đến thống kê và phân tích số liệu
- **Giả định**: API của LLM có thể xử lý OCR vé số với độ chính xác đủ cao
- **Giả định**: Thị trường ứng dụng xổ số có tiềm năng tăng trưởng trong 3-5 năm tới

## 9. Lộ trình phát triển

- **MVP (Giai đoạn 1)**: Tháng 1-4
    - Phát triển và ra mắt các tính năng cốt lõi
    - Tập trung vào trải nghiệm người dùng đơn giản, hiệu quả
    - Thiết lập cơ sở hạ tầng kỹ thuật
- **Giai đoạn 2**: Tháng 5-10
    - Bổ sung phân tích nâng cao và dự đoán AI
    - Mở rộng hỗ trợ cho xổ số miền Trung và miền Bắc
    - Phát triển tính năng cộng đồng cơ bản
    - Cải thiện độ chính xác OCR
- **Giai đoạn 3**: Tháng 11-22
    - Triển khai mô hình doanh thu (premium, quảng cáo)
    - Tích hợp mua vé số trực tuyến (nếu pháp luật cho phép)
    - Phát triển tính năng cộng đồng nâng cao
    - Mở rộng sang nền tảng web

## 10. Chỉ số thành công (KPIs)

- **Người dùng**:
    - Số lượng người dùng đăng ký: 50.000 sau 3 tháng
    - Tỷ lệ giữ chân người dùng: >40% sau 30 ngày
    - Người dùng hoạt động hàng ngày (DAU): >10.000 sau 3 tháng
- **Tương tác**:
    - Tần suất sử dụng trung bình: >3 lần/tuần
    - Thời gian trung bình trong ứng dụng: >5 phút/phiên
    - Số lượng vé số quản lý: >5 vé/người dùng/tháng
- **Hiệu suất**:
    - Tỷ lệ chuyển đổi từ chụp vé sang dò vé: >80%
    - Độ chính xác của OCR: >85% trong điều kiện tiêu chuẩn
    - Thời gian xử lý dò vé: <2 giây/vé
- **Hài lòng người dùng**:
    - Điểm đánh giá ứng dụng: >4.5/5 trên cửa hàng ứng dụng
    - Tỷ lệ báo lỗi: <0.5% người dùng
    - Net Promoter Score (NPS): >40

Tài liệu này mô tả chi tiết các yêu cầu sản phẩm cho ứng dụng Số Nào Ra (SoNaoRa) trong giai đoạn MVP. Mục tiêu chính là tạo ra một ứng dụng toàn diện, dễ sử dụng, giúp người chơi xổ số Việt Nam dễ dàng theo dõi kết quả, quản lý vé số và tận dụng các công cụ phân tích để tăng cơ hội trúng thưởng.
