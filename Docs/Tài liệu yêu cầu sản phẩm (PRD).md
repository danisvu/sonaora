## THÔNG TIN TÀI LIỆU

**Phiên bản:** 1.0

**Ngày tạo:** 20/03/2025

**Người tạo:** [PM Name]

**Trạng thái:** Bản thảo

**Đối tượng:** Ban quản lý dự án, Team phát triển, Các bên liên quan

## 1. GIỚI THIỆU

### 1.1. Mục đích tài liệu

Tài liệu này mô tả chi tiết các yêu cầu chức năng và phi chức năng của ứng dụng Số Nào Ra (SoNaoRa), các đặc điểm kỹ thuật và lộ trình phát triển. Đây là tài liệu tham chiếu chính cho team phát triển, làm cơ sở cho việc thiết kế, phát triển và kiểm thử sản phẩm.

### 1.2. Phạm vi tài liệu

Tài liệu này bao gồm các yêu cầu cho phiên bản MVP (Minimum Viable Product) của ứng dụng Số Nào Ra, dự kiến phát hành vào ngày 15/05/2025. Các tính năng và yêu cầu cho các phiên bản sau MVP sẽ được mô tả sơ lược để cung cấp tầm nhìn dài hạn.

### 1.3. Tài liệu tham khảo

- Tài liệu Tầm nhìn Dự án Số Nào Ra (19/03/2025)
- Báo cáo Phân tích Thị trường Xổ số Việt Nam 2023-2025
- Phân tích Đối tượng Người dùng Xổ số Việt Nam
- Kế hoạch Kỹ thuật và Kiến trúc Hệ thống

## 2. TỔNG QUAN SẢN PHẨM

### 2.1. Tầm nhìn sản phẩm

Số Nào Ra hướng tới việc trở thành ứng dụng hàng đầu tại Việt Nam dành cho người chơi xổ số, nơi người dùng có thể dễ dàng theo dõi kết quả, quản lý vé số thông minh và tiếp cận các phân tích dữ liệu để tăng cơ hội trúng thưởng. Đồng thời, ứng dụng sẽ xây dựng một cộng đồng sôi động để người chơi xổ số có thể kết nối và chia sẻ kinh nghiệm.

### 2.2. Mô tả sản phẩm

Số Nào Ra là ứng dụng di động đa nền tảng (iOS và Android) phát triển bằng Flutter, hỗ trợ người chơi xổ số tại Việt Nam quản lý hoạt động chơi xổ số hiệu quả hơn. Ứng dụng cung cấp tính năng xem kết quả xổ số miền Nam và Vietlott theo thời gian thực, lịch quay thưởng, nhập và quản lý vé số, cùng với công cụ dò vé tự động. Ngoài ra, ứng dụng sẽ hỗ trợ cá nhân hóa trải nghiệm thông qua tùy chỉnh giao diện theo phong thủy và tùy biến menu yêu thích theo sở thích của người dùng.

### 2.3. Định vị sản phẩm

Trong thị trường các ứng dụng xổ số tại Việt Nam, Số Nào Ra định vị là ứng dụng toàn diện duy nhất phục vụ cả người chơi xổ số truyền thống và Vietlott, với điểm khác biệt là giao diện thân thiện với mọi độ tuổi và khả năng quản lý vé số thông minh. Đặc biệt, ứng dụng sẽ là nền tảng tích hợp nhiều loại hình xổ số, khác với các ứng dụng hiện tại thường chỉ tập trung vào một loại hình. Khả năng cá nhân hóa theo phong thủy cũng là một điểm độc đáo giúp Số Nào Ra khác biệt hoàn toàn trên thị trường.

### 2.4. Mục tiêu kinh doanh

1. Xây dựng cơ sở người dùng ban đầu đạt 20.000 người trong tháng đầu tiên sau khi ra mắt
2. Đạt tỷ lệ giữ chân người dùng (retention rate) trên 35% sau 30 ngày
3. Tạo nền tảng vững chắc cho việc phát triển các tính năng nâng cao và mô hình doanh thu trong tương lai
4. Trở thành một trong 3 ứng dụng xổ số hàng đầu tại Việt Nam trong vòng 12 tháng sau khi ra mắt

## 3. PHÂN TÍCH THỊ TRƯỜNG VÀ ĐỐI THỦ

### 3.1. Phân tích thị trường

- Thị trường xổ số Việt Nam đạt doanh thu 153.037 tỷ đồng năm 2023, tăng 11% so với năm 2022
- Xổ số miền Nam chiếm 93,3% thị phần toàn quốc, là thị trường mục tiêu chính của Số Nào Ra
- Khoảng 60-70 triệu người trưởng thành tại Việt Nam là đối tượng tiềm năng của thị trường xổ số
- Tỷ lệ sở hữu smartphone tại Việt Nam đạt trên 70%, tạo điều kiện thuận lợi cho ứng dụng di động
- Các yếu tố tâm linh và phong thủy có ảnh hưởng lớn đến việc lựa chọn số của người chơi xổ số tại Việt Nam

### 3.2. Phân tích đối thủ

1. **Vietlott SMS (Ứng dụng chính thức của Vietlott)**
    - Điểm mạnh: Hỗ trợ mua vé Vietlott trực tuyến, độ tin cậy cao
    - Điểm yếu: Chỉ hỗ trợ xổ số Vietlott, giao diện chưa thân thiện với người dùng lớn tuổi, không có tính năng cá nhân hóa theo phong thủy
    - Điểm khác biệt với SoNaoRa: Chúng ta hỗ trợ cả xổ số truyền thống và Vietlott, tùy chỉnh giao diện theo phong thủy
2. **Các ứng dụng xem kết quả xổ số hiện có**
    - Điểm mạnh: Đã có người dùng, giao diện đơn giản
    - Điểm yếu: Chỉ tập trung vào xem kết quả, thiếu tính năng quản lý vé và dò vé tự động, không có cá nhân hóa
    - Điểm khác biệt với SoNaoRa: Chúng ta cung cấp giải pháp toàn diện để quản lý hoạt động chơi xổ số, có khả năng cá nhân hóa cao
3. **Trang web xem kết quả xổ số**
    - Điểm mạnh: Dễ truy cập, không cần cài đặt ứng dụng
    - Điểm yếu: Trải nghiệm mobile kém, không có tính năng quản lý vé số cá nhân
    - Điểm khác biệt với SoNaoRa: Chúng ta cung cấp trải nghiệm mobile tối ưu và tính năng cá nhân hóa

### 3.3. Lợi thế cạnh tranh

1. Ứng dụng duy nhất tích hợp đầy đủ cả xổ số truyền thống miền Nam và các loại hình Vietlott
2. Giao diện thân thiện với mọi đối tượng, đặc biệt phù hợp với người dùng lớn tuổi
3. Khả năng quản lý vé số thông minh với tính năng nhập thủ công và dò vé tự động
4. Nền tảng kỹ thuật vững chắc cho việc phát triển tính năng OCR nhận dạng vé số trong tương lai
5. Khả năng xuất dữ liệu để phân tích cá nhân hoặc sử dụng với các mô hình AI
6. Tính năng tùy chỉnh giao diện theo phong thủy độc đáo, phù hợp với văn hóa và tâm lý người Việt
7. Khả năng cá nhân hóa cao với menu yêu thích theo sở thích của người dùng

## 4. ĐỐI TƯỢNG NGƯỜI DÙNG

### 4.1. Phân loại người dùng

### 4.1.1. Người chơi xổ số truyền thống

- **Đặc điểm nhân khẩu học:** 35-60 tuổi, thu nhập trung bình, thường xuyên mua vé số truyền thống
- **Đặc điểm công nghệ:** Ít thành thạo công nghệ, ưa thích giao diện đơn giản
- **Nhu cầu/vấn đề:** Muốn dễ dàng theo dõi kết quả xổ số, quản lý vé đã mua, không bỏ lỡ cơ hội trúng thưởng, tin vào yếu tố phong thủy khi chọn số
- **Kỳ vọng:** Giao diện đơn giản, dễ sử dụng, thông báo kết quả nhanh chóng, chính xác, có các yếu tố phong thủy hỗ trợ chọn số

### 4.1.2. Người chơi xổ số điện toán Vietlott

- **Đặc điểm nhân khẩu học:** 25-45 tuổi, thu nhập khá, sống tại thành thị
- **Đặc điểm công nghệ:** Thành thạo công nghệ, sử dụng smartphone thường xuyên
- **Nhu cầu/vấn đề:** Theo dõi jackpot lớn, quản lý nhiều vé Vietlott, muốn trải nghiệm cá nhân hóa
- **Kỳ vọng:** Thông tin chính xác, cập nhật nhanh, công cụ quản lý vé dễ sử dụng, giao diện hiện đại có thể tùy chỉnh

### 4.1.3. Người chơi mới

- **Đặc điểm nhân khẩu học:** 18-30 tuổi, sinh viên hoặc người đi làm trẻ
- **Đặc điểm công nghệ:** Rất thành thạo công nghệ, thích trải nghiệm mới
- **Nhu cầu/vấn đề:** Tìm hiểu cách chơi xổ số, muốn trải nghiệm thử cơ hội, thích ứng dụng có thể cá nhân hóa cao
- **Kỳ vọng:** Giao diện hiện đại, hướng dẫn dễ hiểu, thông tin đầy đủ về các loại hình xổ số, khả năng tùy biến cao

### 4.2. User Personas

### 4.2.1. Persona 1: Ông Tuấn - Người chơi xổ số truyền thống

- **Tuổi:** 55
- **Nghề nghiệp:** Cán bộ hưu trí
- **Địa điểm:** TP.HCM
- **Hành vi chơi xổ số:** Mua 2-3 vé số truyền thống mỗi ngày, dò kết quả qua TV hoặc báo, tin vào số may mắn theo tuổi
- **Thách thức:** Khó quản lý vé đã mua, đôi khi quên dò, bỏ lỡ cơ hội trúng thưởng, muốn biết số nào hợp tuổi
- **Mục tiêu:** Muốn một cách dễ dàng để theo dõi vé đã mua và kết quả xổ số, ứng dụng có màu sắc hợp phong thủy

### 4.2.2. Persona 2: Chị Hương - Người chơi Vietlott

- **Tuổi:** 35
- **Nghề nghiệp:** Nhân viên văn phòng
- **Địa điểm:** Hà Nội
- **Hành vi chơi xổ số:** Mua vé Mega 6/45 và Power 6/55 mỗi tuần khi jackpot lớn
- **Thách thức:** Khó theo dõi nhiều vé cùng lúc, muốn biết jackpot đã lên bao nhiêu, thích giao diện phù hợp cá nhân
- **Mục tiêu:** Cần công cụ quản lý nhiều vé Vietlott, thông báo khi jackpot hấp dẫn, và tùy chỉnh ứng dụng theo sở thích

### 4.2.3. Persona 3: Minh - Người chơi mới

- **Tuổi:** 22
- **Nghề nghiệp:** Sinh viên
- **Địa điểm:** Đà Nẵng
- **Hành vi chơi xổ số:** Mới bắt đầu quan tâm đến xổ số, thỉnh thoảng mua vé để thử vận may
- **Thách thức:** Chưa hiểu rõ về cách chơi và các loại hình xổ số khác nhau, thích ứng dụng có thể tùy biến theo sở thích
- **Mục tiêu:** Muốn tìm hiểu thêm về xổ số, có hướng dẫn rõ ràng cách chơi hiệu quả, và tùy chỉnh giao diện theo sở thích cá nhân

### 4.3. Hành trình người dùng (User Journey)

### 4.3.1. Hành trình của Ông Tuấn

1. **Khám phá:** Nghe con giới thiệu về ứng dụng Số Nào Ra
2. **Tải và đăng ký:** Con giúp tải ứng dụng và đăng ký tài khoản
3. **Học sử dụng:** Tìm hiểu cách xem kết quả xổ số và nhập vé thủ công
4. **Cá nhân hóa:** Tùy chỉnh giao diện ứng dụng theo màu sắc hợp tuổi và phong thủy
5. **Sử dụng hàng ngày:** Nhập các vé số đã mua, kiểm tra kết quả, và xem thông tin xổ số yêu thích
6. **Chia sẻ:** Giới thiệu ứng dụng cho bạn bè cùng tuổi

### 4.3.2. Hành trình của Chị Hương

1. **Khám phá:** Tìm kiếm ứng dụng quản lý vé số trên App Store
2. **Tải và đăng ký:** Tự tải và đăng ký tài khoản
3. **Khám phá tính năng:** Tập trung vào tính năng xem kết quả Vietlott và quản lý vé
4. **Tùy chỉnh:** Thiết lập Power 6/55 là loại hình mặc định và tùy chỉnh giao diện theo sở thích
5. **Sử dụng hàng tuần:** Nhập các vé Vietlott đã mua và theo dõi jackpot
6. **Phân tích dữ liệu:** Xuất dữ liệu kết quả Vietlott 6 tháng gần nhất kèm prompt về "các số xuất hiện nhiều lần nhất" để phân tích với ChatGPT
7. **Phản hồi:** Đánh giá ứng dụng và đề xuất tính năng mới

### 4.3.3. Hành trình của Minh

1. **Khám phá:** Thấy quảng cáo ứng dụng trên Facebook
2. **Tải và đăng ký:** Tải ứng dụng và đăng ký bằng tài khoản Google
3. **Tìm hiểu:** Đọc hướng dẫn về các loại hình xổ số trong ứng dụng
4. **Tùy biến:** Thử nghiệm các tùy chọn giao diện và thêm Power 6/55 vào menu yêu thích
5. **Thử nghiệm:** Mua vé lần đầu và nhập vào ứng dụng để thử tính năng dò vé
6. **Phân tích:** Sử dụng tính năng xuất dữ liệu để phân tích xu hướng số với công cụ AI
7. **Tương tác:** Tiếp tục sử dụng nếu trải nghiệm tốt, hoặc bỏ nếu không thấy giá trị

## 5. YÊU CẦU TÍNH NĂNG

### 5.1. Tính năng MVP (Phát hành 15/05/2025)

### 5.1.1. Xem kết quả xổ số

- **Mô tả:** Hiển thị kết quả đầy đủ của xổ số miền Nam (21 tỉnh) và Vietlott (Mega 6/45, Power 6/55, Max 3D, Max 4D), cập nhật theo thời gian thực
- **Yêu cầu chi tiết:**
    - Hiển thị kết quả xổ số miền Nam với đầy đủ các giải từ Đặc biệt đến giải Tám
    - Hiển thị kết quả Vietlott với giá trị jackpot và các giải thưởng khác
    - Cập nhật kết quả trong vòng 2 phút sau khi có kết quả chính thức
    - Cho phép xem lại kết quả của các ngày trước (tối thiểu 30 ngày gần nhất)
    - Hỗ trợ tìm kiếm và lọc kết quả theo tỉnh/thành và ngày
- **Tiêu chí chấp nhận:**
    - Kết quả hiển thị chính xác 100% và cập nhật kịp thời
    - Thời gian tải kết quả < 2 giây
    - Giao diện hiển thị rõ ràng, dễ đọc, phù hợp với người dùng lớn tuổi
    - Hoạt động ổn định khi không có kết nối internet (hiển thị kết quả đã cache)

### 5.1.2. Lịch quay thưởng

- **Mô tả:** Hiển thị lịch quay thưởng chi tiết theo ngày, giờ và đài quay thưởng
- **Yêu cầu chi tiết:**
    - Hiển thị lịch quay thưởng của xổ số miền Nam theo từng tỉnh/thành
    - Hiển thị lịch quay thưởng của các loại hình Vietlott
    - Cung cấp thông tin về thời gian và địa điểm quay thưởng
    - Cho phép đặt nhắc nhở cho các kỳ quay thưởng quan tâm
- **Tiêu chí chấp nhận:**
    - Lịch quay thưởng hiển thị chính xác và cập nhật khi có thay đổi
    - Giao diện lịch trực quan, dễ sử dụng
    - Nhắc nhở hoạt động đúng thời điểm đã cài đặt

### 5.1.3. Thông báo kết quả

- **Mô tả:** Gửi thông báo sau khi có kết quả xổ số
- **Yêu cầu chi tiết:**
    - Gửi thông báo khi có kết quả xổ số miền Nam và Vietlott
    - Cho phép người dùng tùy chỉnh loại thông báo muốn nhận
    - Hỗ trợ thông báo cho vé đã trúng thưởng
- **Tiêu chí chấp nhận:**
    - Thông báo gửi đúng thời điểm (không trễ quá 5 phút sau khi có kết quả)
    - Nội dung thông báo rõ ràng, đầy đủ thông tin
    - Người dùng có thể dễ dàng bật/tắt và tùy chỉnh thông báo

### 5.1.4. Nhập vé thủ công

- **Mô tả:** Giao diện nhập vé trực quan, dễ sử dụng, hỗ trợ nhiều loại vé số
- **Yêu cầu chi tiết:**
    - Hỗ trợ nhập vé xổ số truyền thống miền Nam
    - Hỗ trợ nhập vé Vietlott (Mega 6/45, Power 6/55, Max 3D, Max 4D)
    - Giao diện nhập liệu tối ưu cho từng loại vé (bàn phím số, chọn nhanh)
    - Kiểm tra tính hợp lệ của vé khi nhập
- **Tiêu chí chấp nhận:**
    - Giao diện nhập vé đơn giản, trực quan
    - Thời gian nhập một vé số < 30 giây
    - Kiểm tra và phản hồi lỗi nhập liệu ngay lập tức
    - Hỗ trợ chỉnh sửa thông tin vé đã nhập

### 5.1.5. Dò vé tự động

- **Mô tả:** Tự động so khớp với kết quả mới nhất, tính toán giải thưởng nếu trúng
- **Yêu cầu chi tiết:**
    - Dò vé tự động khi có kết quả mới
    - Tính toán chính xác giải thưởng cho mỗi loại vé
    - Hiển thị thông tin rõ ràng về kết quả dò vé
    - Thông báo cho người dùng khi có vé trúng thưởng
- **Tiêu chí chấp nhận:**
    - Độ chính xác 100% trong việc dò vé và tính giải thưởng
    - Thời gian dò vé < 1 giây/vé
    - Hiển thị kết quả dò vé trực quan, dễ hiểu

### 5.1.6. Quản lý vé đã mua

- **Mô tả:** Lưu trữ và phân loại vé số, hiển thị trạng thái dò và kết quả trúng thưởng
- **Yêu cầu chi tiết:**
    - Lưu trữ thông tin vé số đã mua theo ngày, loại vé
    - Phân loại vé theo trạng thái (chưa dò, không trúng, đã trúng)
    - Hiển thị lịch sử vé số đã mua và kết quả
    - Hỗ trợ tìm kiếm và lọc vé số
- **Tiêu chí chấp nhận:**
    - Giao diện quản lý vé số trực quan, dễ sử dụng
    - Thời gian tải danh sách vé < 2 giây
    - Hỗ trợ lưu trữ tối thiểu 100 vé số/người dùng

### 5.1.7. Đăng ký/đăng nhập

- **Mô tả:** Xác thực qua email hoặc số điện thoại, hỗ trợ đăng nhập qua mạng xã hội
- **Yêu cầu chi tiết:**
    - Đăng ký tài khoản bằng email hoặc số điện thoại
    - Hỗ trợ đăng nhập qua Google, Facebook
    - Xác thực số điện thoại qua OTP
    - Quản lý phiên đăng nhập và bảo mật
- **Tiêu chí chấp nhận:**
    - Quá trình đăng ký đơn giản, < 1 phút
    - Đăng nhập nhanh chóng, < 5 giây
    - Tuân thủ các tiêu chuẩn bảo mật trong xác thực

### 5.2. Tính năng dự kiến sau MVP

### 5.2.1. Chụp và nhận dạng vé số bằng AI/OCR

- **Mô tả:** Sử dụng camera để chụp vé số và tự động nhận dạng thông tin
- **Ưu tiên:** Cao (dự kiến phát triển ngay sau MVP)
- **Thời gian dự kiến:** Tháng 6/2025

### 5.2.2. Thống kê số "nóng"/"lạnh" và biểu đồ trực quan

- **Mô tả:** Phân tích dữ liệu lịch sử để hiển thị xu hướng số xuất hiện
- **Ưu tiên:** Trung bình
- **Thời gian dự kiến:** Quý 3/2025

### 5.2.3. Tính năng cộng đồng cơ bản

- **Mô tả:** Diễn đàn chia sẻ kinh nghiệm và dự đoán giữa người chơi
- **Ưu tiên:** Trung bình
- **Thời gian dự kiến:** Quý 3/2025

### 5.2.4. Hỗ trợ xổ số miền Trung và miền Bắc

- **Mô tả:** Mở rộng hỗ trợ xem kết quả và dò vé cho các khu vực khác
- **Ưu tiên:** Cao
- **Thời gian dự kiến:** Quý 4/2025

### 5.2.5. Xuất dữ liệu và tích hợp với công cụ phân tích

- **Mô tả:** Cho phép người dùng xuất/copy dữ liệu kết quả xổ số kèm theo các prompt được định nghĩa sẵn để sử dụng với các công cụ phân tích bên ngoài và mô hình LLM
- **Yêu cầu chi tiết:**
    - Cho phép xuất dữ liệu kết quả xổ số theo nhiều định dạng (CSV, JSON, văn bản thuần)
    - Hỗ trợ lọc dữ liệu theo khoảng thời gian (ngày, tuần, tháng, năm)
    - Cung cấp tùy chọn giới hạn dung lượng dữ liệu xuất ra (để phù hợp với giới hạn của các công cụ phân tích)
    - Tích hợp các prompt mẫu được tối ưu hóa cho phân tích xổ số với các mô hình LLM phổ biến (ChatGPT, Claude, v.v.)
    - Cho phép người dùng tùy chỉnh và lưu các prompt của riêng họ
    - Hỗ trợ chia sẻ trực tiếp dữ liệu đến các ứng dụng phân tích phổ biến
- **Tiêu chí chấp nhận:**
    - Xuất dữ liệu hoàn thành trong <3 giây cho bộ dữ liệu lên đến 1 năm
    - Định dạng xuất dữ liệu phải tương thích với các công cụ phân tích phổ biến
    - Prompt mẫu phải được tối ưu và kiểm thử để đảm bảo hiệu quả với các mô hình LLM
    - Giao diện xuất dữ liệu phải trực quan, dễ sử dụng
    - Các tùy chọn lọc dữ liệu phải hoạt động chính xác
- **Ưu tiên:** Cao
- **Thời gian dự kiến:** Quý 3/2025 (có thể đẩy lên sớm hơn sau khi đánh giá phản hồi từ MVP)

### 5.2.6. Tùy chỉnh giao diện theo phong thủy

- **Mô tả:** Cho phép người dùng tùy chỉnh giao diện ứng dụng theo phong thủy, hợp tuổi
- **Yêu cầu chi tiết:**
    - Hỗ trợ thay đổi màu sắc giao diện theo phong thủy và mệnh của người dùng (Kim, Mộc, Thủy, Hỏa, Thổ)
    - Cung cấp bộ sưu tập các theme phong thủy được thiết kế sẵn (ít nhất 5 theme)
    - Cho phép người dùng thêm hình ảnh linh vật phong thủy vào các vị trí trong ứng dụng
    - Cung cấp gợi ý màu sắc, phong cách và linh vật phù hợp dựa trên năm sinh của người dùng
    - Lưu và đồng bộ tùy chỉnh giao diện giữa các thiết bị
- **Tiêu chí chấp nhận:**
    - Các theme phong thủy phải được thiết kế chuyên nghiệp và hài hòa
    - Thay đổi giao diện phải mượt mà, không ảnh hưởng đến hiệu suất ứng dụng
    - Khả năng quay lại giao diện mặc định một cách dễ dàng
    - Các tùy chỉnh phong thủy không làm giảm khả năng sử dụng của ứng dụng
    - Giao diện vẫn đảm bảo đồng nhất khi thay đổi theme
- **Ưu tiên:** Cao
- **Thời gian dự kiến:** Quý 3/2025

### 5.2.7. Menu yêu thích và tùy chỉnh loại hình xổ số

- **Mô tả:** Cho phép người dùng tùy chỉnh menu với các loại hình xổ số ưa thích và thiết lập loại hình mặc định
- **Yêu cầu chi tiết:**
    - Cho phép người dùng đánh dấu các loại hình xổ số yêu thích (Vietlott, xổ số miền Nam theo tỉnh, v.v.)
    - Tạo menu yêu thích với các loại hình xổ số người dùng thường xuyên truy cập
    - Cho phép người dùng thiết lập loại hình xổ số mặc định khi mở ứng dụng
    - Hỗ trợ sắp xếp lại thứ tự các mục trong menu yêu thích
    - Đồng bộ hóa tùy chỉnh giữa các thiết bị của người dùng
- **Tiêu chí chấp nhận:**
    - Giao diện menu yêu thích trực quan, dễ sử dụng
    - Thời gian tải màn hình mặc định < 2 giây
    - Tùy chỉnh menu yêu thích phải được lưu chính xác
    - Hoạt động mượt mà trên tất cả các thiết bị được hỗ trợ
- **Ưu tiên:** Cao
- **Thời gian dự kiến:** Quý 3/2025

## 6. YÊU CẦU PHI CHỨC NĂNG

### 6.1. Hiệu suất

- Thời gian phản hồi API < 2 giây
- Thời gian khởi động ứng dụng < 3 giây
- Thời gian tải trang kết quả xổ số < 2 giây
- Thời gian dò vé < 1 giây/vé
- Ứng dụng phải hoạt động mượt mà trên các thiết bị có cấu hình trung bình
- Thời gian áp dụng thay đổi giao diện phong thủy < 2 giây

### 6.2. Bảo mật

- Bảo vệ thông tin người dùng tuân thủ quy định PDPA Việt Nam
- Mã hóa dữ liệu nhạy cảm trong quá trình truyền và lưu trữ
- Quản lý phiên đăng nhập an toàn
- Chính sách quyền riêng tư rõ ràng, dễ hiểu
- Không lưu trữ thông tin thẻ tín dụng hoặc tài khoản ngân hàng

### 6.3. Độ tin cậy

- Uptime tối thiểu 99,5%
- Kết quả xổ số chính xác 100%
- Dữ liệu người dùng được sao lưu định kỳ
- Hệ thống phục hồi sau sự cố < 10 phút
- Khả năng hoạt động offline với các tính năng cơ bản
- Lưu trữ tùy chỉnh giao diện và menu yêu thích của người dùng không bị mất khi cập nhật ứng dụng

### 6.4. Khả năng sử dụng

- Giao diện thân thiện với mọi lứa tuổi
- Hỗ trợ font chữ lớn và chế độ tối (dark mode)
- Thiết kế responsive, tương thích với nhiều kích thước màn hình
- Tuân thủ các nguyên tắc thiết kế Material Design
- Thiết kế tối ưu cho thao tác một tay
- Các theme phong thủy đảm bảo độ tương phản và khả năng đọc dễ dàng

### 6.5. Khả năng mở rộng

- Kiến trúc cho phép dễ dàng bổ sung tính năng mới
- Cấu trúc database linh hoạt, dễ mở rộng
- Hỗ trợ tối thiểu 100.000 người dùng đồng thời
- Khả năng xử lý tăng trưởng dữ liệu 300% trong năm đầu tiên
- Hỗ trợ đa ngôn ngữ (dự kiến bổ sung tiếng Anh trong tương lai)
- Khả năng thêm mới các theme phong thủy và phong cách giao diện

### 6.6. Tương thích

- Hỗ trợ iOS 13+ và Android 8.0+
- Tối ưu cho các thiết bị phổ biến tại Việt Nam
- Hoạt động tốt trên kết nối mạng không ổn định
- Tương thích với các dịch vụ đám mây phổ biến
- Đảm bảo các theme phong thủy hoạt động tốt trên mọi thiết bị được hỗ trợ

## 7. KIẾN TRÚC VÀ CÔNG NGHỆ

### 7.1. Kiến trúc tổng thể

- Ứng dụng di động: Flutter 3.x
- Backend: Firebase (Firestore, Functions, Authentication, Storage, FCM)
- API: RESTful API, WebSockets cho dữ liệu real-time
- Database: Cloud Firestore (NoSQL)

### 7.2. Mô hình dữ liệu

### 7.2.1. Dữ liệu người dùng

```
users/
  {userId}/
    profile: {name, email, phone, birthYear, settings}
    tickets/
      {ticketId}: {type, numbers, date, status, result}
    notifications/
      {notificationId}: {type, message, date, read}
    saved_prompts/
      {promptId}: {name, text, description, created_at}
    ui_preferences/
      theme: {type, color, feng_shui_element}
      mascots: [{id, position, visibility}]
      favorites: {
        menu_items: [{type, id, position}],
        default_lottery_type: {type, id}
      }

```

### 7.2.2. Dữ liệu kết quả xổ số

```
lottery_results/
  traditional/
    {region}/
      {date}/
        results: {...}
  vietlott/
    {type}/
      {date}/
        results: {...}

```

### 7.2.3. Dữ liệu phân tích và cấu hình

```
analytics/
  hot_numbers/
    {region}/{timeframe}: [...]
  cold_numbers/
    {region}/{timeframe}: [...]
  templates/
    prompt_templates/
      {templateId}: {name, description, prompt_text, model_type}
ui_configs/
  themes/
    {themeId}: {name, colors, assets, feng_shui_element}
  mascots/
    {mascotId}: {name, description, image_url, feng_shui_element}
  lottery_types/
    {typeId}: {name, description, region, icon_url}

```

### 7.3. Tích hợp bên thứ ba

- Firebase: Backend as a Service
- Google Analytics: Phân tích hành vi người dùng
- FCM (Firebase Cloud Messaging): Gửi thông báo
- Crashlytics: Theo dõi lỗi ứng dụng
- Open AI API (tương lai): Tích hợp với tính năng phân tích AI

### 7.4. Offline Strategy

- Caching kết quả xổ số gần đây
- Lưu trữ vé số đã nhập trên thiết bị
- Đồng bộ hóa dữ liệu khi có kết nối internet
- Thông báo rõ ràng về trạng thái offline
- Lưu trữ cục bộ các tùy chỉnh giao diện và menu yêu thích

## 8. GIAO DIỆN NGƯỜI DÙNG

### 8.1. Nguyên tắc thiết kế

- Đơn giản, trực quan, dễ sử dụng cho mọi lứa tuổi
- Ưu tiên khả năng sử dụng hơn là thiết kế phức tạp
- Tương thích với chế độ tối (dark mode) và các theme phong thủy
- Phông chữ rõ ràng, dễ đọc
- Bố cục nhất quán giữa các màn hình
- Các theme phong thủy đảm bảo thẩm mỹ và tính nhất quán

### 8.2. Sitemap và luồng người dùng

### 8.2.1. Sitemap

1. Màn hình đăng nhập/đăng ký
2. Màn hình chính (Dashboard)
3. Xem kết quả xổ số
    - Xổ số miền Nam
    - Vietlott
4. Lịch quay thưởng
5. Quản lý vé số
    - Nhập vé mới
    - Danh sách vé đã nhập
    - Chi tiết vé
6. Công cụ dữ liệu (sau MVP)
    - Xuất dữ liệu
    - Quản lý prompt
    - Chia sẻ phân tích
7. Menu yêu thích (sau MVP)
    - Danh sách loại hình xổ số yêu thích
    - Thiết lập loại hình mặc định
8. Tùy chỉnh giao diện (sau MVP)
    - Theme phong thủy
    - Linh vật phong thủy
    - Màu sắc và phong cách
9. Cài đặt
    - Thông báo
    - Hồ sơ người dùng
    - Cài đặt ứng dụng

### 8.2.2. Luồng người dùng chính

1. **Xem kết quả xổ số:**
    - Mở ứng dụng
    - Chọn loại xổ số (miền Nam/Vietlott) hoặc mở loại hình mặc định
    - Xem kết quả
2. **Nhập và dò vé:**
    - Mở ứng dụng
    - Chọn "Nhập vé mới"
    - Chọn loại vé
    - Nhập thông tin vé
    - Lưu vé
    - Hệ thống tự động dò khi có kết quả
3. **Tùy chỉnh giao diện phong thủy:**
    - Mở cài đặt
    - Chọn "Tùy chỉnh giao diện"
    - Nhập năm sinh hoặc chọn mệnh
    - Chọn theme phong thủy phù hợp
    - Tùy chọn thêm linh vật
    - Áp dụng thay đổi
4. **Thiết lập menu yêu thích:**
    - Mở cài đặt
    - Chọn "Menu yêu thích"
    - Đánh dấu loại hình xổ số ưa thích
    - Sắp xếp thứ tự hiển thị
    - Chọn loại hình mặc định
    - Lưu thay đổi
5. **Xuất dữ liệu để phân tích:**
    - Mở màn hình kết quả xổ số
    - Mở menu Công cụ dữ liệu
    - Chọn khoảng thời gian
    - Chọn định dạng xuất
    - Tùy chọn: chọn prompt mẫu
    - Xuất và chia sẻ dữ liệu

### 8.3. Wireframes chính

*Các wireframes chi tiết sẽ được phát triển bởi đội thiết kế UX/UI và đính kèm dưới dạng phụ lục*

## 9. KẾ HOẠCH TRIỂN KHAI

### 9.1. Lộ trình phát triển MVP

1. **Thiết kế UI/UX và kiến trúc hệ thống:** 20/03 - 27/03/2025 (1 tuần)
2. **Xây dựng tính năng xem kết quả và lịch quay thưởng:** 28/03 - 10/04/2025 (2 tuần)
3. **Phát triển tính năng đăng ký/đăng nhập và nhập vé thủ công:** 11/04 - 24/04/2025 (2 tuần)
4. **Hoàn thiện tính năng dò vé và quản lý vé:** 25/04 - 01/05/2025 (1 tuần)
5. **Testing và sửa lỗi:** 02/05 - 08/05/2025 (1 tuần)
6. **Chuẩn bị phát hành:** 09/05 - 15/05/2025 (1 tuần)
7. **Phát hành MVP:** 15/05/2025

### 9.2. Kế hoạch sau MVP

1. **Phát triển tính năng OCR:** 16/05 - 15/06/2025 (1 tháng)
2. **Phát triển tính năng tùy chỉnh giao diện phong thủy và menu yêu thích:** 16/06 - 15/07/2025 (1 tháng)
3. **Phát triển tính năng xuất dữ liệu và tích hợp với công cụ phân tích:** 16/07 - 15/08/2025 (1 tháng)
4. **Phát triển thống kê và biểu đồ trực quan:** 16/08 - 15/09/2025 (1 tháng)
5. **Phát triển tính năng cộng đồng cơ bản:** 16/09 - 15/10/2025 (1 tháng)
6. **Mở rộng hỗ trợ xổ số miền Trung và miền Bắc:** 16/10 - 15/11/2025 (1 tháng)

### 9.3. Kế hoạch testing

- **Alpha Testing:** 25/04 - 01/05/2025 (nội bộ)
- **Beta Testing:** 02/05 - 08/05/2025 (nhóm người dùng được chọn)
- **UAT (User Acceptance Testing):** 09/05 - 12/05/2025
- **Testing tự động:** Unit tests, Integration tests, UI tests
- **Testing theme và UI tùy chỉnh:** Kiểm tra độ tương thích trên các thiết bị khác nhau

### 9.4. Kế hoạch phát hành

- **Pre-launch Marketing:** 01/05 - 15/05/2025
- **Phát hành:** 15/05/2025
- **Theo dõi và phản hồi nhanh:** 15/05 - 31/05/2025
- **Bản cập nhật đầu tiên (OCR):** 01/06/2025
- **Bản cập nhật thứ hai (UI phong thủy và menu yêu thích):** 15/07/2025

### 9.5. Chiến lược backup và chuyển đổi

- Kiểm tra tự động trước mỗi lần triển khai
- Khả năng rollback nhanh chóng khi có sự cố
- Theo dõi chặt chẽ các chỉ số hiệu suất sau khi triển khai
- Phát hành A/B testing cho tính năng giao diện phong thủy

## 10. RỦI RO VÀ GIẢI PHÁP GIẢM THIỂU

### 10.1. Rủi ro kỹ thuật

| Rủi ro | Mức độ | Giải pháp giảm thiểu |
| --- | --- | --- |
| Độ chính xác và kịp thời của dữ liệu kết quả xổ số | Cao | - Sử dụng nhiều nguồn dữ liệu<br>- Kiểm tra chéo tự động<br>- Cơ chế cập nhật thủ công khi cần |
| Hiệu suất ứng dụng trên thiết bị cấu hình thấp | Trung bình | - Tối ưu hóa code và tài nguyên<br>- Testing trên nhiều loại thiết bị<br>- Lazy loading cho dữ liệu lớn |
| Ổn định của hệ thống khi có nhiều người dùng | Trung bình | - Stress testing với lượng người dùng mô phỏng<br>- Thiết kế hệ thống có khả năng mở rộng<br>- Monitoring liên tục |
| Bảo mật dữ liệu người dùng | Cao | - Tuân thủ các practices bảo mật tốt nhất<br>- Mã hóa dữ liệu<br>- Review code định kỳ |
| Tích hợp với các API bên ngoài cho tính năng xuất dữ liệu | Trung bình | - Xây dựng adapter layer để dễ dàng chuyển đổi API<br>- Caching và retry mechanism<br>- Monitoring và alerting |
| Hiệu suất khi thay đổi theme phong thủy | Trung bình | - Tối ưu assets và tài nguyên<br>- Pre-loading theme<br>- Compression hiệu quả |

### 10.2. Rủi ro kinh doanh

| Rủi ro | Mức độ | Giải pháp giảm thiểu |
| --- | --- | --- |
| Cạnh tranh từ ứng dụng tương tự | Trung bình | - Tập trung vào lợi thế cạnh tranh<br>- Ra mắt tính năng độc đáo sớm<br>- Trải nghiệm người dùng vượt trội |
| Thay đổi quy định pháp luật về xổ số | Cao | - Theo dõi chặt chẽ các quy định<br>- Thiết kế hệ thống linh hoạt<br>- Tuân thủ tất cả quy định hiện hành |
| Khó tiếp cận người dùng lớn tuổi | Cao | - Thiết kế giao diện đơn giản<br>- Tài liệu hướng dẫn chi tiết<br>- Hỗ trợ khách hàng chuyên nghiệp |
| Người dùng không thấy giá trị của ứng dụng | Trung bình | - Truyền thông rõ giá trị cốt lõi<br>- Thu thập và phản hồi feedback sớm<br>- Cải thiện liên tục dựa trên dữ liệu thực tế |
| Tính năng xuất dữ liệu không được sử dụng rộng rãi | Trung bình | - Giáo dục người dùng về lợi ích của phân tích dữ liệu<br>- Cung cấp ví dụ và hướng dẫn sử dụng<br>- Đơn giản hóa quy trình xuất và phân tích |
| Tính năng phong thủy không được đánh giá cao | Trung bình | - Đảm bảo tính xác thực của thông tin phong thủy<br>- Thiết kế theme hấp dẫn và chuyên nghiệp<br>- Kết hợp các yếu tố truyền thống và hiện đại |

## 11. CHỈ SỐ THÀNH CÔNG (KPIs)

### 11.1. KPI Người dùng

- Đạt 20.000 người dùng trong tháng đầu tiên
- Tỷ lệ giữ chân người dùng (retention rate) > 35% sau 30 ngày
- Thời gian sử dụng trung bình > 5 phút/phiên
- Tần suất sử dụng > 3 lần/tuần

### 11.2. KPI Sản phẩm

- Điểm đánh giá ứng dụng > 4.3/5 sao
- Tỷ lệ sự cố (crash rate) < 1%
- Thời gian tải trang < 2 giây
- 60% người dùng sử dụng ít nhất 3 tính năng chính
- 30% người dùng thử nghiệm tính năng xuất dữ liệu sau 3 tháng ra mắt
- Tỷ lệ người dùng hài lòng với tính năng xuất dữ liệu > 75%
- Tỷ lệ sử dụng tính năng tùy chỉnh giao diện phong thủy > 40% sau khi ra mắt
- Tỷ lệ người dùng thiết lập menu yêu thích > 50% trong số người dùng thường xuyên

### 11.3. KPI Marketing

- Chi phí thu hút khách hàng (CAC) < 15.000 VNĐ/người dùng
- Tỷ lệ chuyển đổi từ lượt xem quảng cáo > 3%
- Tỷ lệ giới thiệu người dùng mới > 20%
- Đánh giá tích cực về tính năng phong thủy trong các đánh giá ứng dụng > 30%

### 11.4. KPI Kinh doanh

- Đạt top 10 ứng dụng xổ số trên App Store và Google Play trong vòng 3 tháng
- Chuẩn bị tiền đề cho mô hình doanh thu trong tương lai
- Tăng thời gian sử dụng ứng dụng thêm 20% sau khi ra mắt tính năng tùy chỉnh giao diện và menu yêu thích

## 12. LƯU Ý ĐẶC BIỆT VÀ RÀNG BUỘC

### 12.1. Ràng buộc pháp lý

- **Loại bỏ tính năng mua vé trực tuyến:** Tính năng này sẽ KHÔNG được triển khai do yêu cầu sự cho phép từ cơ quan quản lý nhà nước, hiện tại chưa phù hợp để triển khai. Tính năng này được đưa vào danh sách "ngoài phạm vi" và sẽ chỉ được xem xét khi có sự cho phép rõ ràng từ cơ quan có thẩm quyền.
- Tuân thủ các quy định về hoạt động xổ số tại Việt Nam
- Chỉ cung cấp thông tin kết quả xổ số chính thức
- Tuân thủ quy định về quảng cáo và khuyến mãi
- Đảm bảo rằng tính năng xuất dữ liệu không vi phạm bản quyền hay quy định về chia sẻ thông tin
- Nội dung phong thủy cần được chuẩn bị cẩn thận, tránh các yếu tố mê tín dị đoan quá mức

### 12.2. Ràng buộc dự án

- Team 4 người: PM, Developer, UX/UI Designer, QA
- Thời gian phát triển MVP: 8 tuần
- Stack công nghệ: Flutter, Firebase
- Ngân sách giới hạn cho marketing và phát triển ban đầu
- Cần tham khảo ý kiến chuyên gia phong thủy cho tính năng tùy chỉnh giao diện theo phong thủy

### 12.3. Giả định

- Người dùng có thiết bị smartphone với hệ điều hành iOS 13+ hoặc Android 8.0+
- Người dùng có kết nối internet cơ bản
- API kết quả xổ số sẽ hoạt động ổn định và cung cấp dữ liệu chính xác
- Các mô hình AI/LLM sẽ tiếp tục hỗ trợ phân tích dữ liệu xổ số thông qua prompt
- Người dùng Việt Nam quan tâm đến yếu tố phong thủy và tính cá nhân hóa trong ứng dụng

## 13. PHỤ LỤC

### 13.1. Dữ liệu nghiên cứu người dùng

*Sẽ được bổ sung sau khi hoàn thành nghiên cứu*

### 13.2. Wireframes chi tiết

*Sẽ được bổ sung sau khi hoàn thành thiết kế*

### 13.3. Quy trình dịch vụ

*Sẽ được bổ sung sau khi hoàn thành thiết kế quy trình*

### 13.4. Tài liệu kỹ thuật bổ sung

*Sẽ được bổ sung sau khi hoàn thành kiến trúc kỹ thuật chi tiết*

### 13.5. Mẫu prompt cho tính năng xuất dữ liệu

*Sẽ được bổ sung trong quá trình phát triển tính năng*

### 13.6. Bảng tham chiếu phong thủy

*Sẽ được bổ sung sau khi tham khảo ý kiến chuyên gia phong thủy*

---

**Phê duyệt bởi:**

Người lập: [PM Name]

Ngày: 20/03/2025

Người phê duyệt: [Owner Name]

Ngày: ***/***/2025
