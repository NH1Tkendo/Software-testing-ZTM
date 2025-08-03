## Mục Tiêu của Kiểm Thử Phần Mềm

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- Kiểm thử phần mềm có nhiều mục tiêu chính, tùy thuộc vào giai đoạn, người thực hiện và môi trường kiểm thử.
- Các mục tiêu bao gồm đánh giá sản phẩm công việc, đảm bảo đáp ứng yêu cầu, giảm rủi ro, cung cấp thông tin cho các bên liên quan và tuân thủ các quy định.

### Các Mục Tiêu Chính của Kiểm Thử Phần Mềm

#### 1. Đánh Giá Sản Phẩm Công Việc (Work-Product Evaluation)

- **Sản phẩm công việc (work-product)**: Các tài liệu hoặc thành phần được tạo ra trong quá trình phát triển phần mềm, khác với sản phẩm cuối (end product) như ứng dụng di động hoặc website.
  - Ví dụ: Mã nguồn (code), tài liệu yêu cầu (requirements), thiết kế (design), trường hợp kiểm thử (test cases).
- **Mục tiêu**: Xem xét và đánh giá các sản phẩm công việc để tìm ra vấn đề hoặc lỗi.
- **Lợi ích**: Phát hiện lỗi sớm trong tài liệu hoặc mã nguồn giúp cải thiện chất lượng sản phẩm cuối.

#### 2. Đáp Ứng Yêu Cầu (Fulfilling Requirements)

- Kiểm thử [[Verification-validation#Xác Minh (Verification)|xác minh (verification)]] đảm bảo ứng dụng đáp ứng các yêu cầu được ghi trong:
  - Tài liệu yêu cầu hệ thống (SRS - System Requirements Specification).
  - Tài liệu yêu cầu sản phẩm (PRD - Product Requirements Document).
  - Câu chuyện người dùng (user stories).
- **Ví dụ**: Kiểm tra xem ứng dụng có hỗ trợ đăng nhập bằng Facebook, Instagram, hoặc Google như yêu cầu hay không.

#### 3. Xây Dựng Niềm Tin (Building Confidence)

- Đảm bảo ứng dụng sẵn sàng để triển khai (launch) với ít lỗi nghiêm trọng nhất có thể.
- Mặc dù không có phần mềm nào hoàn toàn không có lỗi (bug-free), kiểm thử giúp giảm thiểu số lượng lỗi (defects) và đảm bảo ứng dụng hoạt động ổn định.

#### 4. Tìm Kiếm Lỗi và Thất Bại (Finding Defects and Failures)

- **Lỗi (defect)**: Vấn đề trong mã nguồn hoặc thiết kế.
- **Thất bại (failure)**: Hậu quả của lỗi, ví dụ ứng dụng bị sập (crash).
- **Mục tiêu**:
  - Phát hiện lỗi và thất bại trong quá trình phát triển.
  - Ngăn ngừa lỗi ngay từ đầu bằng cách xem xét yêu cầu, thiết kế, hoặc mã nguồn.
- **Cách ngăn ngừa lỗi**:
  - Xem xét tài liệu yêu cầu và thiết kế để đảm bảo chúng tuân thủ chuẩn (standards).
  - Đảm bảo sản phẩm công việc được xây dựng đúng cách từ đầu, giảm nguy cơ lỗi trong [[Dynamic-Static-Testing#Kiểm Thử Động (Dynamic Testing)|kiểm thử động (dynamic testing)]].

> **Liên quan**: Xem [[Testing-Debugging|Kiểm Thử vs Gỡ Lỗi]] để hiểu vai trò của tester trong việc tìm lỗi và developer trong việc sửa lỗi.

#### 5. Cung Cấp Thông Tin cho Các Bên Liên Quan (Providing Information to Stakeholders)

- **Các bên liên quan nội bộ (internal stakeholders)**: Trưởng nhóm, quản lý cấp cao (CEO, CTO).
- **Các bên liên quan bên ngoài (external stakeholders)**: Khách hàng hoặc công ty đối tác.
- **Mục tiêu**: Cung cấp thông tin chính xác về chất lượng ứng dụng để hỗ trợ quyết định triển khai (release decision).
- **Vai trò của người kiểm thử**: Là nguồn thông tin đáng tin cậy nhất về tình trạng ứng dụng, thay vì dựa vào đánh giá chủ quan của nhà phát triển.

#### 6. Giảm Rủi Ro (Reducing Risks)

- Phát hiện lỗi sớm trong các giai đoạn phát triển giúp:
  - Ngăn lỗi xuất hiện ở các giai đoạn sau (ví dụ: từ yêu cầu đến thiết kế, từ thiết kế đến mã nguồn, từ mã nguồn đến kiểm thử tích hợp).
  - Giảm rủi ro lỗi nghiêm trọng (high-impact defects) xuất hiện khi người dùng cuối sử dụng ứng dụng.
- **Ví dụ**:
  - Phát hiện lỗi trong yêu cầu giúp giảm rủi ro lỗi trong thiết kế.
  - Phát hiện lỗi trong [[Testing-level#Kiểm Thử Đơn Vị (Unit Testing/Component Testing/Module Testing)|kiểm thử đơn vị (unit testing)]] ngăn lỗi lan sang [[Testing-level#Kiểm Thử Tích Hợp (Integration Testing)|kiểm thử tích hợp (integration testing)]].

#### 7. Tuân Thủ Luật Pháp và Quy Định (Compliance with Laws and Regulations)

- Đảm bảo ứng dụng tuân thủ các quy định pháp luật hoặc tiêu chuẩn ngành của quốc gia hoặc khu vực triển khai (ví dụ: Ấn Độ, Ai Cập, Mỹ).
- **Ví dụ**:
  - Tuân thủ tiêu chuẩn tiếp cận (accessibility standards).
  - Tuân thủ các tiêu chuẩn ngành cụ thể như hàng không (avionics) hoặc ô tô (automotive).
- **Tầm quan trọng**: Tránh các vấn đề pháp lý hoặc rủi ro cho công ty.

### Tính Linh Hoạt của Mục Tiêu Kiểm Thử

- Các mục tiêu kiểm thử thay đổi tùy thuộc vào:
  - **Người thực hiện kiểm thử**: Nhà phát triển, người kiểm thử, nhà phân tích kinh doanh, hoặc người dùng.
  - **Thời điểm kiểm thử**: Giai đoạn đầu (yêu cầu, thiết kế), giữa (mã nguồn), hay cuối (triển khai) của vòng đời phát triển phần mềm.
  - **Môi trường kiểm thử (test environment)**: Môi trường phát triển (development), môi trường thử nghiệm (staging), hoặc môi trường thực tế (production).
- **Ví dụ**:
  - Ở giai đoạn đầu: Đánh giá sản phẩm công việc và giảm rủi ro là ưu tiên.
  - Ở giai đoạn cuối (kiểm thử chấp nhận): Cung cấp thông tin cho quyết định triển khai và xác thực tính hữu ích cho người dùng là quan trọng hơn.

### Ghi Chú Thêm

- Các mục tiêu này được tham khảo từ **Chứng chỉ ISTQB Foundation Level**, sẽ được thảo luận chi tiết sau.
- Để tối ưu hóa kiểm thử, người kiểm thử cần hiểu rõ mục tiêu phù hợp với từng giai đoạn và môi trường.

---

## Liên kết liên quan

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Verification-validation|Xác Minh và Xác Thực]] - Chi tiết về verification và validation
- [[Testing-level|Các Mức Độ Kiểm Thử]] - Các giai đoạn thực hiện mục tiêu kiểm thử
- [[Testing-Debugging|Kiểm Thử vs Gỡ Lỗi]] - Vai trò trong việc tìm và sửa lỗi
- [[Testing-process|Quy Trình Kiểm Thử]] - Quy trình 7 bước để đạt các mục tiêu
