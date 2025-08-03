## Phân Biệt Kiểm Thử (Testing) và Gỡ Lỗi (Debugging)

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- Kiểm thử (testing) và gỡ lỗi (debugging) là hai hoạt động khác nhau trong quy trình phát triển phần mềm, thường được thực hiện bởi các vai trò khác nhau trong đội ngũ.
- Hiểu rõ sự khác biệt giữa hai khái niệm này là rất quan trọng để thực hiện kiểm thử hiệu quả.

### 1. Kiểm Thử (Testing)

#### Khái niệm

- Kiểm thử là tập hợp các hoạt động nhằm phát hiện lỗi (defects) hoặc thất bại (failures) trong phần mềm.
- Bao gồm hai loại chính:
  - **[[Dynamic-Static-Testing#Kiểm Thử Tĩnh (Static Testing)|Kiểm thử tĩnh (static testing)]]**: Xem xét tài liệu, thiết kế, hoặc mã nguồn mà không thực thi.
  - **[[Dynamic-Static-Testing#Kiểm Thử Động (Dynamic Testing)|Kiểm thử động (dynamic testing)]]**: Thực thi mã nguồn, cung cấp đầu vào và kiểm tra đầu ra.
- Mục tiêu: Xác định các vấn đề trong ứng dụng và báo cáo chúng qua báo cáo lỗi (defect report).

#### Vai trò

- Thường được thực hiện bởi **người kiểm thử phần mềm (software tester)**.
- Người kiểm thử không sửa lỗi, mà chỉ xác định và báo cáo lỗi.

### 2. Gỡ Lỗi (Debugging)

#### Khái niệm

- Gỡ lỗi là quá trình **xác định và loại bỏ nguyên nhân gây ra lỗi hoặc thất bại** trong phần mềm.
- Đây là **hoạt động phát triển (development activity)**, không phải hoạt động kiểm thử.

#### Vai trò

- Thường được thực hiện bởi:
  - **Nhà phát triển (developer)**: Nếu lỗi liên quan đến mã nguồn (code).
  - **Nhà thiết kế (designer)**: Nếu lỗi nằm ở thiết kế (design).
  - **Chủ sở hữu sản phẩm (product owner)** hoặc **nhà phân tích kinh doanh (business analyst)**: Nếu lỗi liên quan đến yêu cầu (requirements).
- Nhà phát triển phân tích báo cáo lỗi từ người kiểm thử, xác định nguồn gốc vấn đề (ví dụ: mã nguồn, thiết kế, hoặc yêu cầu) và sửa chữa.

#### Quy trình

- Người kiểm thử phát hiện lỗi → Gửi báo cáo lỗi cho nhà phát triển.
- Nhà phát triển đọc báo cáo, phân tích hệ thống, xác định nguyên nhân và sửa lỗi.
- Sau khi sửa, nhà phát triển thông báo rằng lỗi đã được khắc phục.

### 3. Kiểm Thử Lại (Confirmation Testing/Retesting)

#### Khái niệm

- Sau khi lỗi được sửa, người kiểm thử thực hiện **kiểm thử lại (confirmation testing)** bằng cách lặp lại các bước đã gây ra lỗi để xác minh xem lỗi đã được khắc phục hoàn toàn hay chưa.

#### Quy trình

- Nếu lỗi đã được sửa:
  - Người kiểm thử đóng báo cáo lỗi (defect report).
  - Quy trình hoàn tất.
- Nếu lỗi chưa được sửa:
  - Người kiểm thử mở lại báo cáo lỗi (reopen) và yêu cầu nhà phát triển tiếp tục gỡ lỗi.

### 4. Kiểm Thử Hồi Quy (Regression Testing)

#### Khái niệm

- Kiểm thử hồi quy được thực hiện để đảm bảo rằng các phần không thay đổi của ứng dụng không bị ảnh hưởng bởi các thay đổi (sửa lỗi hoặc cập nhật) trong quá trình gỡ lỗi.
- Tập trung vào các khu vực không được sửa đổi nhưng có nguy cơ bị tác động.

#### Đặc điểm

- Thường được thực hiện sau kiểm thử lại.
- Có thể sử dụng **tự động hóa kiểm thử (test automation)** để kiểm tra hiệu quả, đặc biệt trong các dự án Agile.

> **Chi tiết**: Xem [[Testing-type#Kiểm Thử Hồi Quy (Regression Testing)|Kiểm Thử Hồi Quy]] trong phần Các Loại Kiểm Thử.

### So Sánh Kiểm Thử và Gỡ Lỗi

- **Kiểm thử (Testing)**:
  - Mục đích: Phát hiện lỗi và báo cáo.
  - Thực hiện bởi: Người kiểm thử.
  - Bao gồm: Kiểm thử tĩnh, động, kiểm thử lại, kiểm thử hồi quy.
- **Gỡ lỗi (Debugging)**:
  - Mục đích: Tìm và sửa nguyên nhân gây ra lỗi.
  - Thực hiện bởi: Nhà phát triển, nhà thiết kế, hoặc nhà phân tích kinh doanh.
  - Là bước trung gian giữa kiểm thử và kiểm thử lại.

### Ghi Chú Thêm

- Kiểm thử và gỡ lỗi là các bước bổ trợ lẫn nhau trong quy trình phát triển phần mềm.
- Kiểm thử lại và kiểm thử hồi quy là hai loại kiểm thử quan trọng sau khi gỡ lỗi để đảm bảo chất lượng ứng dụng.

---

## Liên kết liên quan

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Object-of-testing|Mục Tiêu của Kiểm Thử]] - Mục tiêu "tìm lỗi và thất bại"
- [[Dynamic-Static-Testing|Kiểm Thử Động và Tĩnh]] - Hai loại kiểm thử chính
- [[Testing-type|Các Loại Kiểm Thử]] - Chi tiết về retesting và regression testing
- [[Testing-process|Quy Trình Kiểm Thử]] - Thực thi kiểm thử trong quy trình 7 bước
