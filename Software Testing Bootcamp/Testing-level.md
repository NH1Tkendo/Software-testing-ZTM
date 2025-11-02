## Các Mức Độ Kiểm Thử (Testing Levels)

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- **Mức độ kiểm thử (test levels)** là các nhóm hoạt động kiểm thử được tổ chức và quản lý cùng nhau, dựa trên loại kiểm thử, cách thực hiện và người thực hiện.
- Mỗi mức độ kiểm thử là một **thể hiện của [[Testing-process|quy trình kiểm thử (instance of the test process)]]**, bao gồm các bước như lập kế hoạch, phân tích, thiết kế, thực thi, và hoàn tất.
- Các mức độ kiểm thử liên quan chặt chẽ đến **vòng đời phát triển phần mềm (software development lifecycle)**, ví dụ:
  - **Waterfall**: Tất cả các mức độ kiểm thử được thực hiện sau khi phát triển hoàn tất.
  - **V model**: Mỗi mức độ kiểm thử tương ứng với một giai đoạn phát triển (ví dụ: yêu cầu → kiểm thử chấp nhận).
  - **Agile**: Các mức độ kiểm thử có thể chồng lấn, ví dụ: kiểm thử đơn vị (unit testing) trên một phần hệ thống trong khi kiểm thử chấp nhận (acceptance testing) được thực hiện trên phần khác.

### Các Mức Độ Kiểm Thử

#### 1. Kiểm Thử Đơn Vị (Unit Testing/Component Testing/Module Testing)

- **Mục đích**: Kiểm tra các thành phần (components) hoặc đơn vị (units) riêng lẻ của hệ thống, là các phần có thể kiểm thử độc lập (ví dụ: phương thức, lớp, giao diện trong mã nguồn).
- **Ví dụ**:
  - Kiểm tra một phương thức (method) trong mã nguồn.
  - Kiểm tra một lớp (class) hoặc giao diện (interface).
- **Người thực hiện**: Chủ yếu là **nhà phát triển (developer)**, sử dụng kỹ thuật như:
  - Phát triển hướng kiểm thử (Test-Driven Development - TDD).
  - Phát triển hướng hành vi (Behavior-Driven Development - BDD).
- **Lưu ý**:
  - Người kiểm thử có thể thực hiện kiểm thử đơn vị trên **mã tự động hóa kiểm thử (test automation scripts)**, không phải trên phần mềm chính.
  - Là mức kiểm thử chi tiết nhất, tập trung vào từng thành phần riêng lẻ.

#### 2. Kiểm Thử Tích Hợp (Integration Testing)

- **Mục đích**: Kiểm tra sự tương tác hoặc tích hợp giữa các thành phần hoặc hệ thống.
- **Hai loại tích hợp**:
  - **Tích hợp thành phần (Component Integration Testing)**:
    - Kiểm tra sự tương tác giữa các thành phần trong mã nguồn (ví dụ: giữa hai lớp hoặc hai phương thức).
    - Chủ yếu do **nhà phát triển** thực hiện.
  - **Tích hợp hệ thống (System Integration Testing)**:
    - Kiểm tra sự tích hợp giữa các hệ thống lớn (ví dụ: giữa ứng dụng di động và máy chủ, hoặc giữa backend và frontend).
    - Thường do **người kiểm thử phần mềm** thực hiện.
- **Trình tự**:
  - Kiểm thử đơn vị → Kiểm thử tích hợp thành phần → Kiểm thử hệ thống → Kiểm thử tích hợp hệ thống.
- **Ví dụ**:
  - Kiểm tra việc gửi dữ liệu từ một API đến cơ sở dữ liệu.
  - Kiểm tra tương tác giữa ứng dụng di động và website.

#### 3. Kiểm Thử Hệ Thống (System Testing)

- **Mục đích**: Kiểm tra toàn bộ hệ thống sau khi hoàn tất phát triển và tích hợp.
- **Đặc điểm**:
  - Bao gồm cả **kiểm thử chức năng (functional testing)** và **kiểm thử phi chức năng (non-functional testing)**.
  - Đôi khi được gọi là **kiểm thử đầu cuối (end-to-end testing)**.
  - Là mức kiểm thử chính mà **người kiểm thử phần mềm** tập trung, áp dụng khoảng **90% kỹ thuật kiểm thử**.
- **Môi trường kiểm thử**: Cần giống với **môi trường thực tế (production environment)** mà người dùng cuối sử dụng.
- **Tầm quan trọng**: Cung cấp thông tin cho các bên liên quan (stakeholders) để quyết định xem ứng dụng có sẵn sàng triển khai hay không.

#### 4. Kiểm Thử Chấp Nhận (Acceptance Testing)

- **Mục đích**: Đảm bảo ứng dụng sẵn sàng để triển khai, đáp ứng nhu cầu của người dùng cuối hoặc các bên liên quan.
- **Đặc điểm**:
  - Tập trung vào **[[Verification-validation#Xác Thực (Validation)|xác thực (validation)]]**, tức là đảm bảo hệ thống phù hợp với người dùng (ít lỗi nhất có thể).
  - Khác với kiểm thử hệ thống (tập trung tìm lỗi), kiểm thử chấp nhận nhằm **xây dựng niềm tin (building confidence)** rằng ứng dụng sẵn sàng phát hành.
- **Các loại kiểm thử chấp nhận**:
  - **Kiểm thử chấp nhận người dùng (User Acceptance Testing - UAT)**: Người dùng thực tế kiểm tra ứng dụng.
  - **Kiểm thử chấp nhận vận hành (Operational Acceptance Testing)**: Đánh giá khả năng vận hành của hệ thống.
  - **Kiểm thử chấp nhận hợp đồng (Contractual Acceptance Testing)**: Đảm bảo đáp ứng các điều khoản hợp đồng.
- **Hai hình thức phổ biến**:
  - **Kiểm thử alpha (Alpha Testing)**:
    - Mời người dùng tiềm năng đến công ty để kiểm tra ứng dụng dưới sự giám sát.
    - Thực hiện trong môi trường kiểm soát của công ty.
  - **Kiểm thử beta (Beta Testing)**:
    - Gửi ứng dụng đến người dùng để thử nghiệm trong môi trường thực tế (ví dụ: trên thiết bị cá nhân).
    - Thường áp dụng cho ứng dụng di động hoặc game, với giám sát hiệu suất qua báo cáo sự cố (crash reports) và phân tích dữ liệu.

### Mối Quan Hệ Giữa Các Mức Độ Kiểm Thử

- **Trình tự**:
  - Kiểm thử đơn vị → Kiểm thử tích hợp thành phần → Kiểm thử hệ thống → Kiểm thử tích hợp hệ thống (nếu có) → Kiểm thử chấp nhận.
- **Tùy chọn**:
  - Kiểm thử tích hợp hệ thống là tùy chọn, chỉ cần thiết khi có nhiều hệ thống tích hợp (ví dụ: ứng dụng di động và website).
  - Một số ứng dụng chỉ thực hiện kiểm thử alpha, chỉ beta, hoặc cả hai, tùy thuộc vào chiến lược kiểm thử (test strategy) và mục tiêu dự án.

### So Sánh Kiểm Thử Hệ Thống và Kiểm Thử Chấp Nhận

- **Kiểm thử hệ thống**:
  - Mục tiêu: Tìm lỗi (defects) để cải thiện chất lượng.
  - Tập trung vào việc làm hệ thống thất bại để phát hiện vấn đề.
- **Kiểm thử chấp nhận**:
  - Mục tiêu: Xác nhận hệ thống sẵn sàng triển khai, ít lỗi nhất có thể.
  - Tập trung vào xây dựng niềm tin cho các bên liên quan.

### Ghi Chú Thêm

- Mỗi mức độ kiểm thử tuân theo quy trình kiểm thử (lập kế hoạch, phân tích, thiết kế, thực thi, hoàn tất).
- Các kỹ thuật kiểm thử (sẽ được thảo luận sau) chủ yếu áp dụng cho kiểm thử hệ thống.
- Để hiểu rõ hơn về kiểm thử tự động hóa hoặc các công cụ hỗ trợ, tham khảo các phần sau trong khóa học.

---

## Liên kết liên quan

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Testing-process|Quy Trình Kiểm Thử]] - 7 bước áp dụng cho mỗi mức độ
- [[Verification-validation|Xác Minh và Xác Thực]] - Validation trong acceptance testing
- [[Testing-type|Các Loại Kiểm Thử]] - Functional và non-functional testing
- [[Object-of-testing|Mục Tiêu của Kiểm Thử]] - Mục tiêu khác nhau ở các mức độ khác nhau
