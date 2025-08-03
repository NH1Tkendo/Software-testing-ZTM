## Các Loại Kiểm Thử Phần Mềm

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- Các loại kiểm thử phần mềm được phân loại dựa trên mục đích, cách tiếp cận và giai đoạn thực hiện.
- Một số loại đã được đề cập trong các chủ đề trước ([[Dynamic-Static-Testing|kiểm thử tĩnh, động]], hộp trắng, hộp đen), nhưng phần này sẽ đi sâu hơn vào chi tiết và giới thiệu thêm các loại kiểm thử khác.

### 1. Kiểm Thử Chức Năng (Functional Testing)

#### Khái niệm

- Kiểm thử chức năng tập trung vào **hệ thống làm gì (what the system does)**, tức là kiểm tra các chức năng của ứng dụng có hoạt động đúng như yêu cầu hay không.
- Kết quả thường được đánh giá bằng câu trả lời **có/không (yes/no)**.

#### Ví dụ

- Kiểm tra chức năng đăng nhập (login functionality):
  - Nhập tên người dùng (username) và mật khẩu (password) hợp lệ → Kiểm tra xem ứng dụng có chuyển hướng đến màn hình đúng hay không.
  - Để trống tên người dùng → Kiểm tra xem ứng dụng có hiển thị thông báo lỗi (error message) yêu cầu điền tên người dùng hay không.
  - Nhập tên người dùng không hợp lệ (ví dụ: sử dụng số Ả Rập thay vì số tiếng Anh, hoặc nhập tên quá dài/ngắn) → Kiểm tra phản hồi của hệ thống.
- Các tình huống kiểm thử (test cases/scenarios) này đều thuộc kiểm thử chức năng.

#### Đặc điểm

- Tập trung vào các chức năng cụ thể được mô tả trong yêu cầu.
- Thường sử dụng câu hỏi dạng: “Hệ thống có hoạt động đúng với đầu vào này không?”

### 2. Kiểm Thử Phi Chức Năng (Non-Functional Testing)

#### Khái niệm

- Kiểm thử phi chức năng tập trung vào **hệ thống hoạt động như thế nào (how the system performs)**, ví dụ: tốc độ, tính khả dụng, bảo mật.
- Là một **danh mục kiểm thử** bao gồm nhiều loại như:
  - Kiểm thử tính khả dụng (usability testing).
  - Kiểm thử hiệu suất (performance testing).
  - Kiểm thử bảo mật (security testing).
- Kết quả thường không trả lời được bằng **có/không**, mà là một **phạm vi (range)** hoặc dữ liệu cần phân tích.

#### Ví dụ

- Kiểm tra hiệu suất: Ứng dụng có phản hồi trong thời gian hợp lý không?
  - Ví dụ: Thời gian phản hồi 1 giây có thể nhanh với ứng dụng thông thường, nhưng chậm với ứng dụng chơi game (yêu cầu dưới 100 mili giây).
- Kết quả được so sánh với:
  - Tiêu chuẩn thị trường (market benchmarks).
  - Tiêu chuẩn quốc tế (international standards).
  - Kỳ vọng của người dùng.

#### Đặc điểm

- Phụ thuộc vào đặc tính của ứng dụng và người dùng.
- Cần thu thập dữ liệu để đưa ra quyết định, thay vì trả lời đơn giản.

### 3. Kiểm Thử Hộp Đen (Black-Box Testing)

#### Khái niệm

- Người kiểm thử cung cấp đầu vào (input) và kiểm tra đầu ra (output) mà không cần biết cấu trúc bên trong của hệ thống (database, code, APIs).
- Gần với cách người dùng thực tế sử dụng ứng dụng.

#### Ví dụ

- Nhập thông tin vào form đăng nhập và kiểm tra xem hệ thống có phản hồi đúng hay không, mà không quan tâm đến cách mã nguồn xử lý.

#### Đặc điểm

- Ưu điểm: Phù hợp với yêu cầu của người dùng cuối.
- Nhược điểm: Có thể bỏ sót một số lỗi hoặc kịch bản do không hiểu cấu trúc bên trong.
- Chiếm khoảng **80% công việc của người kiểm thử**.

### 4. Kiểm Thử Hộp Trắng (White-Box Testing)

#### Khái niệm

- Người kiểm thử có quyền truy cập vào cấu trúc bên trong của hệ thống (mã nguồn, APIs, cơ sở dữ liệu).
- Tập trung vào **cách hệ thống thực hiện chức năng (how the system performs)**.

#### Ví dụ

- Kiểm tra chức năng thêm sản phẩm vào giỏ hàng:
  - Không chỉ kiểm tra xem sản phẩm có được thêm vào giỏ hàng hay không, mà còn kiểm tra:
    - Yêu cầu API (API request) được gửi đi.
    - Phản hồi API (API response) nhận được.
    - Cách mã nguồn xử lý quá trình.

#### Đặc điểm

- Yêu cầu kiến thức về ngôn ngữ lập trình của ứng dụng.
- Có thể phát hiện lỗi mà kiểm thử hộp đen không tìm thấy.
- Thường áp dụng cho các hệ thống quan trọng hoặc có rủi ro cao.

### 5. Kiểm Thử Động và Tĩnh (Dynamic and Static Testing)

- **[[Dynamic-Static-Testing#Kiểm Thử Động (Dynamic Testing)|Kiểm thử động (Dynamic Testing)]]**:
  - Thực thi mã nguồn, cung cấp đầu vào và chờ đầu ra.
  - Bao gồm cả kiểm thử hộp đen và hộp trắng.
- **[[Dynamic-Static-Testing#Kiểm Thử Tĩnh (Static Testing)|Kiểm thử tĩnh (Static Testing)]]**:
  - Không thực thi mã nguồn, tập trung vào xem xét tài liệu, thiết kế hoặc mã nguồn.
  - Ví dụ: Xem xét yêu cầu, thiết kế Figma, hoặc mã nguồn.

### 6. Kiểm Thử Lại (Retesting/Confirmation Testing)

#### Khái niệm

- Kiểm tra lại cùng một chức năng với các bước tương tự sau khi nhà phát triển sửa lỗi (defect) để xác minh lỗi đã được khắc phục.

#### Quy trình

- Người kiểm thử phát hiện lỗi → Báo cáo lỗi (defect report) cho nhà phát triển.
- Nhà phát triển sửa lỗi và thông báo hoàn tất.
- Người kiểm thử thực hiện kiểm thử lại:
  - Nếu lỗi được sửa: Đóng báo cáo lỗi.
  - Nếu lỗi chưa được sửa: Gửi lại báo cáo cho nhà phát triển.

### 7. Kiểm Thử Hồi Quy (Regression Testing)

#### Khái niệm

- Kiểm tra các phần không thay đổi của ứng dụng sau khi có thay đổi (thêm, xóa, sửa chức năng) để đảm bảo chúng không bị ảnh hưởng.

#### Ví dụ

- Nhà phát triển thêm một chức năng mới → Kiểm thử hồi quy để đảm bảo các chức năng cũ (như đăng nhập, thanh toán) vẫn hoạt động đúng.

#### Đặc điểm

- Thường sử dụng **tự động hóa kiểm thử (test automation)** vì được thực hiện nhiều lần, đặc biệt trong phát triển theo mô hình Agile.
- Mục tiêu: Phát hiện lỗi do thay đổi gây ra ở các phần khác của ứng dụng.

### 8. Kiểm Thử Khói (Smoke Testing)

#### Khái niệm

- Kiểm tra nhanh các chức năng chính của một bản xây dựng mới (new build) để đảm bảo nó ổn định trước khi kiểm thử chi tiết.

#### Ví dụ

- Với một ứng dụng lớn, kiểm thử khói có thể bao gồm:
  - Đăng nhập với tài khoản hợp lệ.
  - Thêm một sản phẩm vào giỏ hàng.
  - Thanh toán và để lại đánh giá.
- Nếu các kiểm tra này thất bại, bản xây dựng bị từ chối (reject) để nhà phát triển sửa trước khi kiểm thử tiếp.

#### Lợi ích

- Tiết kiệm thời gian bằng cách phát hiện lỗi nghiêm trọng sớm.
- Tránh lãng phí thời gian kiểm thử chi tiết nếu bản xây dựng không ổn định.

#### Đặc điểm

- Chỉ kiểm tra các chức năng chính (main functionalities).
- Mục tiêu: Xác minh bản xây dựng đủ ổn định để tiếp tục kiểm thử sâu hơn.

### Ghi Chú Thêm

- Các loại kiểm thử này có thể kết hợp trong một dự án, tùy thuộc vào mục tiêu và giai đoạn phát triển.
- Một số loại kiểm thử (như kiểm thử khói, hồi quy) thường được ưu tiên tự động hóa để tăng hiệu quả.

---

## Liên kết liên quan

### Khái niệm cơ bản

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Dynamic-Static-Testing|Kiểm Thử Động và Tĩnh]] - Chi tiết về dynamic và static testing

### Quy trình và mức độ

- [[Testing-process|Quy Trình Kiểm Thử]] - Các loại testing áp dụng trong 7 bước
- [[Testing-level|Các Mức Độ Kiểm Thử]] - Functional/non-functional ở các mức độ khác nhau

### Thực hành

- [[Testing-Debugging|Kiểm Thử vs Gỡ Lỗi]] - Retesting và regression testing chi tiết
- [[Verification-validation|Xác Minh và Xác Thực]] - Functional testing (verification) vs usability testing (validation)
  > **Lưu ý**: Để tìm hiểu thêm về tự động hóa kiểm thử hoặc các công cụ hỗ trợ, tham khảo ghi chú liên quan trong hệ thống Obsidian (nếu có).

```

```
