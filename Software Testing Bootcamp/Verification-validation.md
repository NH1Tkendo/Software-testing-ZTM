## Kiểm Thử Phần Mềm: Phân B#### Đặc điểm

- Tập trung vào **góc nhìn của nhà phát triển (developer's point of view)**.
- Thường liên quan đến các hoạt động như:
  - [[Testing-type#Kiểm Thử Hộp Trắng (White-Box Testing)|Kiểm thử hộp trắng (white box testing)]]: Xem xét mã nguồn để đảm bảo tuân thủ chuẩn mã hóa.
  - Kiểm tra mã nguồn ([[Testing-level#Kiểm Thử Đơn Vị (Unit Testing/Component Testing/Module Testing)|unit testing]]) để xác minh tính đúng đắn của từng thành phần.
- Kiểm tra xem sản phẩm có tuân thủ các tiêu chuẩn và yêu cầu đã đặt ra hay không.c Minh (Verification) và Xác Thực (Validation)

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- Kiểm thử phần mềm được chia thành hai danh mục chính: **xác minh (verification)** và **xác thực (validation)**.
- Cả hai đều là trách nhiệm của người kiểm thử phần mềm.
- Xác minh và xác thực có mục tiêu khác nhau nhưng có thể giao thoa trong một số hoạt động kiểm thử.

### Xác Minh (Verification)

#### Khái niệm

- Xác minh tập trung vào việc đảm bảo sản phẩm được xây dựng **đúng (building the product right)** theo các yêu cầu đã được định nghĩa.
- Kiểm tra xem ứng dụng có đáp ứng các yêu cầu được ghi trong tài liệu như:
  - Tài liệu yêu cầu hệ thống (SRS - System Requirements Specification).
  - Tài liệu yêu cầu sản phẩm (PRD - Product Requirements Document).
  - Câu chuyện người dùng (user stories).
- Không quan tâm liệu yêu cầu có thực sự hữu ích cho người dùng hay không.

#### Ví dụ

- Kiểm tra các yêu cầu cụ thể của sản phẩm, như:
  - Ứng dụng có cho phép đăng nhập bằng Facebook, Instagram hoặc Google không?
  - Người dùng có thể thêm số điện thoại và nhận mã OTP (One-Time Password) không?
  - Một chiếc áo (shirt) có đáp ứng các yêu cầu:
    - Có hai tay áo (sleeves)?
    - Kích cỡ là lớn (large)?
    - Màu sắc là xanh (blue)?
    - Có thiếu nút (buttons) nào không?

#### Đặc điểm

- Tập trung vào **góc nhìn của nhà phát triển (developer’s point of view)**.
- Thường liên quan đến các hoạt động như:
  - Kiểm thử hộp trắng (white box testing): Xem xét mã nguồn để đảm bảo tuân thủ chuẩn mã hóa.
  - Kiểm tra mã nguồn (unit testing) để xác minh tính đúng đắn của từng thành phần.
- Kiểm tra xem sản phẩm có tuân thủ các tiêu chuẩn và yêu cầu đã đặt ra hay không.

### Xác Thực (Validation)

#### Khái niệm

- Xác thực tập trung vào việc đảm bảo sản phẩm được xây dựng là **đúng sản phẩm (building the right product)**, tức là đáp ứng nhu cầu và mong đợi của người dùng.
- Xem xét từ **góc nhìn của người dùng (customer’s point of view)**, bao gồm:
  - Tính hữu ích (usability).
  - Tính dễ tiếp cận (accessibility).
  - Trải nghiệm người dùng (user experience).
- Không nhất thiết phải dựa vào yêu cầu đã ghi, mà tập trung vào sự hài lòng của người dùng.

#### Ví dụ

- Với chiếc áo (shirt):
  - Áo có vừa với người dùng không?
  - Có thoải mái khi mặc để đi làm không?
  - Màu sắc có phù hợp với mắt người dùng không?
  - Giá cả có hợp lý không?
  - Chất lượng có tốt không? Người thân (vợ, bạn) có thích không?
- Với ứng dụng:
  - Người dùng có cảm thấy dễ sử dụng và muốn tiếp tục sử dụng không?

#### Đặc điểm

- Thường được thực hiện ở các giai đoạn kiểm thử cao hơn, như:
  - [[Testing-level#Kiểm Thử Chấp Nhận (Acceptance Testing)|Kiểm thử chấp nhận (acceptance testing)]].
  - [[Testing-type#Kiểm Thử Phi Chức Năng (Non-Functional Testing)|Kiểm thử tính khả dụng (usability testing)]].
- Đánh giá xem sản phẩm có phù hợp và hữu ích cho người dùng cuối hay không.

### So Sánh Xác Minh và Xác Thực

- **Xác minh (Verification)**:
  - Hỏi: “Chúng ta có đang xây dựng sản phẩm đúng cách không?”
  - Tập trung vào việc tuân thủ yêu cầu và tiêu chuẩn.
  - Ví dụ: Kiểm tra mã nguồn, kiểm tra tài liệu yêu cầu.
- **Xác thực (Validation)**:
  - Hỏi: “Chúng ta có đang xây dựng đúng sản phẩm không?”
  - Tập trung vào trải nghiệm và nhu cầu của người dùng.
  - Ví dụ: Kiểm tra tính hữu ích, sự thoải mái, hoặc sự hài lòng của người dùng.

### Giao Thoa Giữa Xác Minh và Xác Thực

- Một số loại kiểm thử thuộc cả xác minh và xác thực, ví dụ:
  - **[[Testing-level#Kiểm Thử Hệ Thống (System Testing)|Kiểm thử hệ thống (system testing)]]**: Kiểm tra cả tính đúng đắn kỹ thuật (xác minh) và tính phù hợp với người dùng (xác thực).
  - **Kiểm thử beta (beta testing)**: Đánh giá trải nghiệm người dùng thực tế, nhưng cũng kiểm tra tính năng theo yêu cầu.
- Tuy nhiên, một số loại kiểm thử chỉ thuộc một danh mục:
  - **[[Testing-level#Kiểm Thử Đơn Vị (Unit Testing/Component Testing/Module Testing)|Kiểm thử đơn vị (unit testing)]]**: Chỉ tập trung vào xác minh (kiểm tra mã nguồn).
  - **Kiểm thử tính khả dụng (usability testing)**: Chỉ tập trung vào xác thực (đánh giá trải nghiệm người dùng).

### Tầm Quan Trọng

- **Xác minh**: Đảm bảo sản phẩm được xây dựng đúng theo yêu cầu kỹ thuật, tránh lỗi trong quá trình phát triển.
- **Xác thực**: Đảm bảo sản phẩm đáp ứng nhu cầu người dùng, tăng khả năng bán hàng và sự hài lòng của khách hàng.
- Nếu chỉ xác minh mà không xác thực, sản phẩm có thể đúng kỹ thuật nhưng không hữu ích, dẫn đến thất bại về mặt thương mại.

### Trách Nhiệm của Người Kiểm Thử

- Người kiểm thử cần thực hiện cả xác minh và xác thực.
- Phải phân biệt rõ hoạt động đang thực hiện thuộc xác minh hay xác thực để căn chỉnh mục tiêu kiểm thử.

### Ghi Chú Thêm

- Các kỹ thuật kiểm thử khác nhau được áp dụng cho xác minh và xác thực, ví dụ:
  - Xác minh: Kiểm thử hộp trắng, kiểm tra tài liệu yêu cầu.
  - Xác thực: Kiểm thử tính khả dụng, kiểm thử chấp nhận.
- Các mức độ kiểm thử (testing levels) như kiểm thử đơn vị, kiểm thử hệ thống, và kiểm thử chấp nhận sẽ được thảo luận chi tiết trong các phần sau.

---

## Liên kết liên quan

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Object-of-testing|Mục Tiêu của Kiểm Thử]] - Mục tiêu "đáp ứng yêu cầu" liên quan đến verification
- [[Testing-level|Các Mức Độ Kiểm Thử]] - Unit testing (verification) vs Acceptance testing (validation)
- [[Testing-type|Các Loại Kiểm Thử]] - Functional testing vs Non-functional testing
- [[Dynamic-Static-Testing|Kiểm Thử Động và Tĩnh]] - Static testing thường là verification
