# UI Style Guide - Dự án Số Nào Ra (SoNaoRa)

## 1. Nguyên tắc thiết kế tổng quát

### 1.1. Triết lý thiết kế

Dự án Số Nào Ra được xây dựng dựa trên bốn nguyên tắc thiết kế cốt lõi:

- **Dễ tiếp cận**: Thiết kế phải thân thiện với người dùng lớn tuổi không rành công nghệ, dễ nhìn, dễ hiểu và dễ sử dụng.
- **Tin cậy**: Truyền tải cảm giác chính xác, an toàn và chuyên nghiệp trong từng chi tiết.
- **Hiệu quả**: Giúp người dùng hoàn thành mục tiêu nhanh chóng với số lượng thao tác tối thiểu.
- **Nhất quán**: Duy trì sự nhất quán về trực quan và tương tác trên toàn ứng dụng.

### 1.2. Ngôn ngữ thiết kế

Ngôn ngữ thiết kế của Số Nào Ra kết hợp giữa sự đơn giản của Material Design với những điều chỉnh phù hợp với người dùng Việt Nam, đặc biệt là đối tượng người chơi xổ số:

- **Rõ ràng**: Sử dụng khoảng trắng hợp lý, phân cấp thông tin rõ ràng
- **Trực quan**: Ưu tiên biểu tượng và hình ảnh quen thuộc với người Việt Nam
- **Tương tác trực tiếp**: Các thành phần có thể tương tác phải rõ ràng và có phản hồi tức thì
- **Hỗ trợ**: Cung cấp gợi ý và hướng dẫn khi cần thiết

## 2. Hệ thống màu sắc

### 2.1. Bảng màu chính

Bảng màu của Số Nào Ra được thiết kế để truyền tải cảm giác may mắn, đáng tin cậy và dễ đọc:

| Màu | Mã HEX | Mã RGB | Mục đích sử dụng |
| --- | --- | --- | --- |
| Đỏ Cát Tường | #E63946 | rgb(230, 57, 70) | Màu chủ đạo, nút CTA chính, đánh dấu trúng thưởng |
| Vàng May Mắn | #FFD700 | rgb(255, 215, 0) | Đánh dấu kết quả, giải thưởng, jackpot |
| Xanh Tin Cậy | #457B9D | rgb(69, 123, 157) | Thông tin, liên kết, thanh điều hướng |
| Xanh Nhạt | #A8DADC | rgb(168, 218, 220) | Nền phụ, phân tách nội dung |
| Kem Nhẹ | #F1FAEE | rgb(241, 250, 238) | Nền chính (chế độ sáng) |
| Đen Mềm | #1D3557 | rgb(29, 53, 87) | Văn bản chính, tiêu đề |
| Xám Trung Tính | #8D99AE | rgb(141, 153, 174) | Văn bản phụ, biểu tượng không kích hoạt |
| Trắng | #FFFFFF | rgb(255, 255, 255) | Nền thành phần, văn bản trên nền tối |

### 2.2. Bảng màu chế độ tối (Dark Mode)

| Màu | Mã HEX | Mã RGB | Mục đích sử dụng |
| --- | --- | --- | --- |
| Đỏ Cát Tường Tối | #FF6B6B | rgb(255, 107, 107) | Màu chủ đạo trong chế độ tối |
| Vàng May Mắn Tối | #FFD166 | rgb(255, 209, 102) | Đánh dấu kết quả trong chế độ tối |
| Nền Đen | #121212 | rgb(18, 18, 18) | Nền chính (chế độ tối) |
| Đen Cấp 1 | #1E1E1E | rgb(30, 30, 30) | Nền thành phần cấp 1 |
| Đen Cấp 2 | #2C2C2C | rgb(44, 44, 44) | Nền thành phần cấp 2 |
| Xám Sáng | #BBBBBB | rgb(187, 187, 187) | Văn bản phụ trong chế độ tối |
| Trắng Mềm | #E0E0E0 | rgb(224, 224, 224) | Văn bản chính trong chế độ tối |

### 2.3. Màu chức năng

| Màu | Mã HEX | Mã RGB | Mục đích sử dụng |
| --- | --- | --- | --- |
| Thành Công | #4CAF50 | rgb(76, 175, 80) | Thông báo thành công, trúng thưởng |
| Cảnh Báo | #FF9800 | rgb(255, 152, 0) | Cảnh báo, thông tin cần chú ý |
| Lỗi | #F44336 | rgb(244, 67, 54) | Thông báo lỗi, vấn đề |
| Thông Tin | #2196F3 | rgb(33, 150, 243) | Gợi ý, thông tin bổ sung |

### 2.4. Nguyên tắc sử dụng màu sắc

- Đảm bảo tỷ lệ tương phản tối thiểu 4.5:1 giữa văn bản và nền để đảm bảo khả năng đọc
- Không sử dụng màu làm phương tiện truyền đạt thông tin duy nhất (cân nhắc người dùng mù màu)
- Sử dụng màu đỏ và vàng một cách chiến lược để tạo cảm giác may mắn nhưng không gây rối mắt
- Áp dụng màu nhất quán trên toàn ứng dụng để tăng cường khả năng học và sử dụng

## 3. Typography (Hệ thống phông chữ)

### 3.1. Phông chữ chính

- **Phông chữ chính**: SF Pro Text / Roboto (cho Android)
- **Phông chữ dự phòng**: Hệ thống phông sans-serif

Lựa chọn phông chữ dựa trên tính dễ đọc cao, đặc biệt trên màn hình nhỏ và cho người dùng lớn tuổi.

### 3.2. Hệ thống cấp độ phông chữ

| Cấp độ | Kích thước | Độ đậm | Line Height | Mục đích sử dụng |
| --- | --- | --- | --- | --- |
| H1 | 28px | Bold (700) | 34px | Tiêu đề màn hình chính |
| H2 | 24px | Bold (700) | 30px | Tiêu đề phần |
| H3 | 20px | Semibold (600) | 26px | Tiêu đề nhóm, thẻ |
| H4 | 18px | Semibold (600) | 24px | Tiêu đề thành phần |
| Body 1 | 16px | Regular (400) | 22px | Văn bản chính |
| Body 2 | 14px | Regular (400) | 20px | Văn bản phụ |
| Caption | 12px | Regular (400) | 16px | Chú thích, ghi chú |
| Button | 16px | Medium (500) | 20px | Văn bản nút bấm |
| Number | 20px | Medium (500) | 26px | Hiển thị số xổ số |
| Number Large | 32px | Bold (700) | 38px | Hiển thị số trúng thưởng |

### 3.3. Quy tắc typography

- **Kích thước tối thiểu**: Không sử dụng font chữ nhỏ hơn 12px
- **Tùy chỉnh kích thước**: Cho phép người dùng điều chỉnh kích thước font trong cài đặt (Nhỏ/Vừa/Lớn/Rất lớn)
- **Căn chỉnh**: Căn trái cho văn bản dài, căn giữa cho tiêu đề và nội dung ngắn
- **Khoảng cách dòng**: Đảm bảo khoảng cách dòng tối thiểu 1.5 lần kích thước font
- **Trọng lượng**: Sử dụng độ đậm khác nhau để tạo phân cấp thông tin, không chỉ dựa vào kích thước

## 4. Iconography (Hệ thống biểu tượng)

### 4.1. Kiểu dáng biểu tượng

- **Phong cách**: Outline với đường viền 2px, góc bo tròn nhẹ
- **Kích thước cơ bản**: 24x24px
- **Padding**: 2px xung quanh biểu tượng

### 4.2. Biểu tượng chức năng chính

| Biểu tượng | Tên | Mục đích sử dụng |
| --- | --- | --- |
| 🏠 | Home | Màn hình chính |
| 🎲 | Results | Kết quả xổ số |
| 🎫 | Tickets | Quản lý vé số |
| 📊 | Statistics | Thống kê, phân tích |
| 📅 | Calendar | Lịch quay thưởng |
| 📷 | Camera | Chụp vé số |
| 🔔 | Notifications | Thông báo |
| ⚙️ | Settings | Cài đặt |

### 4.3. Kích thước biểu tượng

| Mục đích sử dụng | Kích thước |
| --- | --- |
| Thanh điều hướng | 28x28px |
| Biểu tượng thao tác | 24x24px |
| Biểu tượng chỉ báo | 20x20px |
| Biểu tượng microinteraction | 16x16px |

### 4.4. Nguyên tắc sử dụng biểu tượng

- Biểu tượng phải đi kèm với nhãn văn bản khi xuất hiện lần đầu
- Sử dụng biểu tượng quen thuộc, dễ hiểu với người dùng Việt Nam
- Duy trì nhất quán về kiểu dáng biểu tượng trên toàn ứng dụng
- Tránh sử dụng biểu tượng quá trừu tượng hoặc khó hiểu

## 5. Spacing và Layout

### 5.1. Đơn vị khoảng cách

Hệ thống khoảng cách 8px:
- **4px**: Khoảng cách tối thiểu
- **8px**: Khoảng cách cơ bản
- **16px**: Khoảng cách tiêu chuẩn
- **24px**: Khoảng cách trung bình
- **32px**: Khoảng cách lớn
- **48px**: Khoảng cách rất lớn
- **64px**: Khoảng cách tối đa

### 5.2. Lưới (Grid System)

- **Lưới cơ bản**: 4 cột cho điện thoại, 8 cột cho máy tính bảng
- **Khoảng cách cột**: 16px
- **Padding viền**: 16px (điện thoại), 24px (máy tính bảng)

### 5.3. Nguyên tắc layout

- **Thứ tự đọc**: Tổ chức nội dung theo thứ tự đọc từ trên xuống dưới, từ trái sang phải
- **Phân cấp thông tin**: Sử dụng kích thước, độ đậm và khoảng cách để tạo phân cấp rõ ràng
- **Khoảng trắng**: Sử dụng khoảng trắng rộng rãi để tăng khả năng đọc và làm nổi bật nội dung quan trọng
- **Vùng an toàn**: Đảm bảo nội dung nằm trong vùng an toàn, tránh các cạnh màn hình
- **Tỷ lệ chạm**: Vùng bấm tối thiểu 44x44px cho các thành phần tương tác

## 6. Component Library (Thư viện thành phần)

### 6.1. Nút (Buttons)

#### 6.1.1. Phân loại nút

| Loại | Mô tả | Sử dụng |
| --- | --- | --- |
| Nút chính | Màu đỏ cát tường, font trắng, đệm 16px | Hành động chính trên màn hình |
| Nút thứ cấp | Viền đỏ cát tường, nền trong suốt | Hành động phụ |
| Nút mặc định | Nền xám nhạt, font đen | Hành động thông thường |
| Nút biểu tượng | Chỉ chứa biểu tượng | Hành động phổ biến, tiết kiệm không gian |
| Nút văn bản | Không có nền hoặc viền | Hành động ít quan trọng |

#### 6.1.2. Kích thước nút

| Kích thước | Chiều cao | Padding ngang | Font | Sử dụng |
| --- | --- | --- | --- |--- |
| Lớn | 56px | 24px | 18px | Hành động chính, toàn màn hình |
| Trung bình | 48px | 16px | 16px | Hành động thông thường |
| Nhỏ | 36px | 12px | 14px | Hành động trong thành phần nhỏ |

#### 6.1.3. Trạng thái nút

- **Mặc định**: Trạng thái ban đầu
- **Hover**: Khi di chuột qua (web)
- **Nhấn**: Khi đang nhấn
- **Focus**: Khi được chọn bằng bàn phím
- **Vô hiệu hóa**: Khi không khả dụng
- **Đang tải**: Khi đang xử lý

### 6.2. Trường nhập liệu (Input Fields)

#### 6.2.1. Phân loại trường nhập liệu

| Loại | Mô tả | Sử dụng |
| --- | --- | --- |
| Văn bản một dòng | Trường nhập văn bản cơ bản | Nhập thông tin ngắn |
| Văn bản nhiều dòng | Cho phép nhập nhiều dòng | Nhập nội dung dài |
| Số | Chỉ cho phép nhập số | Nhập số vé số |
| Mã PIN | Hiển thị dưới dạng dấu chấm | Nhập mật khẩu, PIN |
| Chọn ngày | Hiển thị bộ chọn ngày | Chọn ngày quay thưởng |

#### 6.2.2. Trạng thái trường nhập liệu

- **Mặc định**: Trạng thái ban đầu
- **Focus**: Khi đang nhập
- **Điền**: Đã có dữ liệu
- **Lỗi**: Khi dữ liệu không hợp lệ
- **Thành công**: Khi dữ liệu hợp lệ
- **Vô hiệu hóa**: Khi không khả dụng

#### 6.2.3. Kích thước và padding

- **Chiều cao**: 56px (để dễ nhấn cho người dùng lớn tuổi)
- **Padding ngang**: 16px
- **Khoảng cách nhãn**: 8px
- **Kích thước font**: 16px
- **Border radius**: 8px

### 6.3. Thẻ (Cards)

#### 6.3.1. Phân loại thẻ

| Loại | Mô tả | Sử dụng |
| --- | --- | --- |
| Thẻ tiêu chuẩn | Nền trắng, bóng đổ nhẹ | Hiển thị nội dung độc lập |
| Thẻ kết quả | Nền trắng, viền màu | Hiển thị kết quả xổ số |
| Thẻ vé số | Thiết kế giống vé số thật | Hiển thị vé đã nhập |
| Thẻ thông báo | Có biểu tượng trạng thái | Hiển thị thông báo, cảnh báo |

#### 6.3.2. Giải phẫu thẻ

- **Header**: Tùy chọn, chứa tiêu đề và hành động
- **Media**: Tùy chọn, chứa hình ảnh, biểu đồ
- **Content**: Phần chính, chứa nội dung
- **Actions**: Tùy chọn, chứa các nút hành động

#### 6.3.3. Kích thước và padding

- **Padding nội dung**: 16px
- **Khoảng cách giữa các phần**: 12px
- **Border radius**: 12px
- **Độ sâu bóng đổ**: 2-4px

### 6.4. Danh sách (Lists)

#### 6.4.1. Phân loại danh sách

| Loại | Mô tả | Sử dụng |
| --- | --- | --- |
| Danh sách đơn giản | Chỉ văn bản | Hiển thị danh sách đơn giản |
| Danh sách hai dòng | Tiêu đề và mô tả | Hiển thị thông tin chi tiết hơn |
| Danh sách có biểu tượng | Có biểu tượng bên trái | Tăng tính trực quan |
| Danh sách có hình ảnh | Có hình ảnh bên trái | Hiển thị nội dung hình ảnh |
| Danh sách có hành động | Có nút hành động bên phải | Cho phép tương tác nhanh |

#### 6.4.2. Kích thước và padding

- **Chiều cao mục tiêu chuẩn**: 64px
- **Padding ngang**: 16px
- **Padding dọc**: 12px
- **Khoảng cách giữa các mục**: 1px (đường phân cách)
- **Kích thước biểu tượng**: 24x24px

### 6.5. Thanh điều hướng (Navigation)

#### 6.5.1. Thanh điều hướng dưới

- **Số lượng mục tối đa**: 5
- **Chiều cao**: 56px
- **Padding**: 8px
- **Biểu tượng**: 28x28px
- **Kích thước nhãn**: 12px

#### 6.5.2. Thanh ứng dụng trên (App Bar)

- **Chiều cao**: 56px
- **Tiêu đề**: H2 (24px)
- **Padding ngang**: 16px
- **Khoảng cách giữa các phần tử**: 16px

#### 6.5.3. Điều hướng cử chỉ

- Vuốt trái/phải để điều hướng giữa các tab
- Vuốt từ cạnh trái để mở menu
- Vuốt xuống để làm mới nội dung

### 6.6. Dialogs và Modals

#### 6.6.1. Phân loại Dialog

| Loại | Mô tả | Sử dụng |
| --- | --- | --- |
| Dialog thông báo | Thông báo đơn giản | Hiển thị thông tin quan trọng |
| Dialog xác nhận | Yêu cầu xác nhận | Trước hành động quan trọng |
| Dialog nhập liệu | Chứa form nhập liệu | Thu thập thông tin |
| Dialog toàn màn hình | Chiếm toàn bộ màn hình | Hiển thị nội dung phức tạp |

#### 6.6.2. Kích thước và padding

- **Chiều rộng**: 85% chiều rộng màn hình (tối đa 400px)
- **Padding**: 24px
- **Border radius**: 16px
- **Khoảng cách giữa các phần**: 16px
- **Vùng nút**: Padding 16px, căn phải

### 6.7. Thành phần hiển thị số (Number Displays)

#### 6.7.1. Phân loại hiển thị số

| Loại | Mô tả | Sử dụng |
| --- | --- | --- |
| Hiển thị số cơ bản | Font số rõ ràng | Hiển thị số xổ số thông thường |
| Hiển thị số trúng thưởng | Font số lớn, hiệu ứng nổi bật | Đánh dấu số trúng thưởng |
| Hiển thị số vòng tròn | Số trong vòng tròn | Hiển thị kết quả Vietlott |
| Bảng số | Dạng bảng, nhiều cột | Hiển thị kết quả nhiều giải |

#### 6.7.2. Kích thước và định dạng

- **Font chữ**: San-serif đậm, dễ đọc
- **Kích thước số thông thường**: 20px
- **Kích thước số nổi bật**: 32px
- **Khoảng cách giữa các số**: 8px
- **Padding**: 12px
- **Border radius**: 8px (cho vòng tròn: 50%)

## 7. Hướng dẫn trải nghiệm người dùng (UX Guidelines)

### 7.1. Tính khả dụng

- **Mục tiêu**: Người dùng hoàn thành tác vụ trong <30 giây
- **Số lượng thao tác**: Tối đa 3 bước để hoàn thành tác vụ chính
- **Vùng tương tác**: Tối thiểu 44x44px cho tất cả các thành phần có thể nhấn
- **Feedback**: Cung cấp phản hồi trực quan cho mọi thao tác
- **Khả năng phục hồi**: Cho phép hoàn tác hành động quan trọng

### 7.2. Accessibility (Khả năng tiếp cận)

- **Tương phản màu sắc**: Đảm bảo tỷ lệ tương phản WCAG AA (4.5:1)
- **Kích thước text**: Cho phép điều chỉnh từ 12px đến 24px
- **Thay thế hình ảnh**: Cung cấp text thay thế cho tất cả hình ảnh
- **Tương thích screen reader**: Đảm bảo tất cả thành phần có nhãn phù hợp
- **Điều hướng bàn phím**: Hỗ trợ điều hướng không cần chuột/chạm (cho web)

### 7.3. Micro-interactions

- **Hiệu ứng nhấn**: Phản hồi trực quan khi nhấn nút
- **Hiệu ứng chuyển tiếp**: Chuyển đổi mượt mà giữa các màn hình
- **Hiệu ứng loading**: Hiển thị trạng thái đang tải rõ ràng
- **Hiệu ứng thành công**: Đánh dấu rõ ràng khi hoàn thành tác vụ
- **Thông báo**: Hiển thị thông báo không gây gián đoạn

### 7.4. Empty States (Trạng thái trống)

- **Danh sách trống**: Hiển thị hình ảnh và hướng dẫn thân thiện
- **Không có kết quả**: Đề xuất thay đổi tìm kiếm hoặc bộ lọc
- **Không có vé**: Gợi ý thêm vé mới
- **Không có kết nối**: Hiển thị thông tin hữu ích offline

### 7.5. Quy trình chính

#### 7.5.1. Quy trình xem kết quả xổ số

1. Chọn loại xổ số (Miền Nam/Vietlott)
2. Chọn ngày/kỳ quay số
3. Xem kết quả chi tiết
4. Tùy chọn: Dò vé, chia sẻ kết quả

#### 7.5.2. Quy trình nhập vé thủ công

1. Chọn "Thêm vé mới"
2. Chọn loại vé
3. Nhập thông tin vé (số seri, ngày quay, dãy số)
4. Xác nhận và lưu

#### 7.5.3. Quy trình chụp vé

1. Chọn "Thêm vé mới" > "Chụp ảnh"
2. Căn chỉnh vé trong khung hướng dẫn
3. Chụp ảnh
4. Xác nhận hoặc chụp lại
5. Xác nhận kết quả OCR hoặc sửa nếu cần
6. Lưu vé

#### 7.5.4. Quy trình dò vé

1. Chọn vé từ danh sách
2. Hệ thống tự động dò với kết quả mới nhất
3. Hiển thị kết quả trúng/không trúng
4. Tùy chọn: Xem chi tiết giải thưởng

## 8. Áp dụng Style Guide trong thiết kế

### 8.1. Quy trình làm việc thiết kế

1. Sử dụng thư viện Figma Component để đảm bảo nhất quán
2. Tuân thủ grid system và spacing đã định nghĩa
3. Kiểm tra accessibility trước khi hoàn thiện thiết kế
4. Áp dụng Responsive Design cho mọi màn hình

### 8.2. Handoff cho developers

1. Xuất các thành phần UI với tên rõ ràng
2. Cung cấp tất cả trạng thái và biến thể
3. Đảm bảo các giá trị (màu sắc, font, spacing) được mã hóa như biến
4. Bao gồm hướng dẫn animation và micro-interactions

### 8.3. Các nền tảng cụ thể

- **iOS**: Tuân thủ Human Interface Guidelines khi có thể
- **Android**: Tương thích với Material Design
- **Tương lai - Web**: Responsive design cho tất cả breakpoints

---

## 9. Tổng kết

Style Guide này cung cấp nền tảng vững chắc cho sự phát triển giao diện người dùng nhất quán, dễ tiếp cận và hiệu quả cho ứng dụng Số Nào Ra. Các nguyên tắc và thành phần được định nghĩa nhằm tạo ra trải nghiệm trực quan, thân thiện và đáng tin cậy cho người dùng, đặc biệt là đối tượng người chơi xổ số lớn tuổi tại Việt Nam.

Tài liệu này sẽ được cập nhật liên tục trong quá trình phát triển để phản ánh những thay đổi và cải tiến dựa trên phản hồi từ người dùng và các bên liên quan.

Các tệp thiết kế Figma liên quan, bao gồm Component Library và Design System, được lưu trữ tại [đường dẫn Figma].
