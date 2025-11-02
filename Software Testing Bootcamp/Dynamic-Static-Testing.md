## Kiểm Thử Phần Mềm: Phân Biệt Kiểm Thử Động (Dynamic Testing) và Kiểm Thử Tĩnh (Static Testing)

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- Kiểm thử phần mềm được chia thành hai loại chính: **kiểm thử động (dynamic testing)** và **kiểm thử tĩnh (static testing)**.
- Cả hai loại đều là trách nhiệm của người kiểm thử phần mềm.
- Kiểm thử tĩnh và động có thể được thực hiện trong cùng một dự án, đôi khi kết hợp với nhau.

### Kiểm Thử Động (Dynamic Testing)

#### Khái niệm

- Kiểm thử động yêu cầu thực thi mã nguồn (code must be run).
- Quy trình: Cung cấp đầu vào (input) cho hệ thống, hệ thống xử lý, và trả về đầu ra (output).
- Kết quả đầu ra được so sánh với đầu ra kỳ vọng (expected output) để đánh giá tính đúng đắn.

#### Ví dụ

- Thực hiện các thao tác trên ứng dụng, như:
  - Đăng nhập để xem video.
  - Thêm sản phẩm vào giỏ hàng.
  - Tương tác với website, ứng dụng desktop, hoặc trò chơi.
- Bất kỳ hành động nào trong lúc sử dụng ứng dụng đều thuộc kiểm thử động.

#### Đặc điểm

- Yêu cầu mã nguồn đã được viết và sẵn sàng thực thi.
- Thường được thực hiện ở giai đoạn sau của vòng đời phát triển phần mềm (software development lifecycle).

### Kiểm Thử Tĩnh (Static Testing)

#### Khái niệm

- Kiểm thử tĩnh không yêu cầu thực thi mã nguồn, không cung cấp đầu vào hoặc chờ đầu ra.
- Tập trung vào việc **xem xét (review)** các sản phẩm công việc (work products) như tài liệu, thiết kế, hoặc mã nguồn để tìm lỗi.

#### Ví dụ

- **Xem xét thiết kế**: Kiểm tra giao diện Figma, wireframe, hoặc các bản thiết kế khác.
- **Xem xét tài liệu yêu cầu**: Đọc và đánh giá các tài liệu như câu chuyện người dùng (user stories), tài liệu yêu cầu hệ thống (SRS - System Requirements Specification), hoặc tài liệu yêu cầu kinh doanh (BRD - Business Requirements Document).
- **Xem xét mã nguồn (code review)**:
  - Kiểm tra mã nguồn để tìm lỗi, đảm bảo tuân thủ chuẩn mã hóa (coding standards) hoặc kiểm tra tính đầy đủ của chú thích (comments).
  - Thường được gọi là **[[Testing-type#Kiểm Thử Hộp Trắng (White-Box Testing)|kiểm thử hộp trắng (white box testing)]]**, yêu cầu kiến thức về ngôn ngữ lập trình.

#### Đặc điểm

- Có thể thực hiện sớm trong vòng đời phát triển phần mềm, trước khi mã nguồn được viết.
- Tiết kiệm thời gian và chi phí nhờ phát hiện lỗi ở giai đoạn đầu (early testing saves time and money).
- Áp dụng được trong các mô hình phát triển:
  - **Waterfall**: Xem xét yêu cầu, thiết kế trước khi phát triển.
  - **V model**: Xem xét tài liệu ở bên trái của mô hình V.
  - **Agile**: Xem xét câu chuyện người dùng và tiêu chí chấp nhận (acceptance criteria) trước khi triển khai tính năng.

### So Sánh Kiểm Thử Động và Tĩnh

- **Kiểm thử động**:
  - Yêu cầu thực thi mã nguồn.
  - Cần đầu vào và đầu ra.
  - Thực hiện ở giai đoạn sau, khi ứng dụng đã sẵn sàng.
- **Kiểm thử tĩnh**:
  - Không thực thi mã nguồn.
  - Tập trung vào xem xét tài liệu, thiết kế, hoặc mã nguồn.
  - Có thể thực hiện từ ngày đầu của dự án.

### Tương Tác Giữa Kiểm Thử Động và Tĩnh

- Một số hoạt động có thể thuộc cả hai loại:
  - Ví dụ: Khi xem xét tài liệu yêu cầu để tìm lỗi (kiểm thử tĩnh), người kiểm thử có thể đồng thời xây dựng các kịch bản kiểm thử (test scenarios) để chuẩn bị cho kiểm thử động.
- Kỹ thuật như **INVEST** (dùng để đánh giá chất lượng câu chuyện người dùng trong Agile) có thể được áp dụng trong kiểm thử tĩnh, nhưng hỗ trợ lập kế hoạch cho kiểm thử động.

### Lợi Ích của Kiểm Thử Tĩnh

- Phát hiện lỗi sớm, giảm chi phí sửa chữa.
- Tiết kiệm thời gian và công sức so với kiểm thử động.
- Có thể thực hiện trước khi ứng dụng được phát triển hoàn chỉnh.

### Ghi Chú Thêm

- Người kiểm thử không cần lo lắng nếu chưa quen với lập trình khi thực hiện kiểm thử tĩnh (như xem xét mã nguồn). Các khái niệm lập trình sẽ được giải thích chi tiết trong các phần sau.
- Kiểm thử tĩnh và động đều quan trọng, bổ trợ lẫn nhau để đảm bảo chất lượng phần mềm.

---

## Liên kết liên quan

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Testing-type|Các Loại Kiểm Thử]] - Black-box, White-box testing chi tiết
- [[Testing-process|Quy Trình Kiểm Thử]] - Kiểm thử tĩnh trong quy trình 7 bước
- [[Verification-validation|Xác Minh và Xác Thực]] - Kiểm thử tĩnh thường liên quan đến verification
