## Quy Trình Kiểm Thử Phần Mềm (Test Process)

> **Xem thêm**: [[Software-testing|Tổng quan về Kiểm thử phần mềm]]

### Tổng Quan

- **Quy trình kiểm thử (test process)** là các bước mà phần mềm trải qua để được kiểm thử, tập trung chủ yếu vào **[[Dynamic-Static-Testing#Kiểm Thử Động (Dynamic Testing)|kiểm thử động (dynamic testing)]]**, tức là thực thi mã nguồn.
- Quy trình kiểm thử khác với quy trình phát triển phần mềm (software development lifecycle), nhưng có liên quan chặt chẽ.
- Không có quy trình kiểm thử chung cho tất cả các công ty; quy trình thay đổi tùy theo ngành, tiêu chuẩn, và văn hóa công ty.
- Quy trình kiểm thử phổ biến nhất được đề xuất bởi **ISTQB (International Software Testing Qualifications Board)** gồm **7 bước chính**.

### Các Bước trong Quy Trình Kiểm Thử (Theo ISTQB)

#### 1. Lập Kế Hoạch (Test Planning)

- **Mục đích**: Xác định kế hoạch kiểm thử (test plan) dựa trên thông tin về dự án, lịch trình, và yêu cầu.
- **Nội dung của kế hoạch kiểm thử**:
  - Xác định đội ngũ kiểm thử và trách nhiệm của từng thành viên.
  - Xác định phương pháp kiểm thử (testing approaches).
  - Xác định các mốc thời gian (milestones).
  - Lựa chọn công cụ kiểm thử (tools), tiêu chuẩn (standards), và mẫu tài liệu (templates).
- **Người thực hiện**: Thường do **quản lý kiểm thử (test manager)** hoặc **trưởng nhóm kiểm thử (test leader)** thực hiện.
- **Lưu ý**: Người kiểm thử mới (junior tester) hoặc làm tự do (freelancer) hiếm khi được yêu cầu viết kế hoạch kiểm thử.

#### 2. Giám Sát và Kiểm Soát (Test Monitoring and Control)

- **Giám sát (Monitoring)**:
  - So sánh tiến độ thực tế với kế hoạch kiểm thử.
  - Ví dụ: Kế hoạch dự kiến viết 500 trường hợp kiểm thử (test cases) trong 2 tuần. Sau 2 tuần, kiểm tra xem đã hoàn thành đúng số lượng và thời gian hay chưa.
- **Kiểm soát (Control)**:
  - Thực hiện các hành động khắc phục (corrective actions) nếu tiến độ lệch khỏi kế hoạch (ví dụ: chậm trễ hoặc vượt trước lịch trình).
- **Đặc điểm**:
  - Là hoạt động liên tục, kéo dài từ đầu đến cuối quy trình kiểm thử.
  - Thường do quản lý kiểm thử hoặc trưởng nhóm kiểm thử thực hiện.
- **Tài liệu**: Có thể tạo **báo cáo tiến độ kiểm thử (test progress report)** để chia sẻ với các bên liên quan (stakeholders) nhằm hỗ trợ quyết định tiếp theo.

#### 3. Phân Tích Kiểm Thử (Test Analysis)

- **Mục đích**: Phân tích tài liệu yêu cầu (requirements), thiết kế (design), hoặc câu chuyện người dùng (user stories) để xác định **điều kiện kiểm thử (test conditions)** hoặc **kịch bản kiểm thử (test scenarios)**.
- **Ví dụ kịch bản kiểm thử**:
  - Xác minh/ xác thực đăng nhập với tên người dùng và mật khẩu hợp lệ.
  - Xác thực hành vi khi để trống trường email và nhấn nút đăng ký.
  - Xác thực hành vi khi nhập mật khẩu sai.
- **Đặc điểm**:
  - Là bước đầu tiên mà hầu hết người kiểm thử tham gia khi bắt đầu dự án.
  - Kịch bản kiểm thử thường được viết dưới dạng câu đơn giản, mô tả chức năng cần kiểm tra.

#### 4. Thiết Kế Kiểm Thử (Test Design)

- **Mục đích**: Chuyển các kịch bản kiểm thử thành **trường hợp kiểm thử (test cases)** chi tiết.
- **Nội dung của trường hợp kiểm thử**:
  - Các bước thực hiện (steps).
  - Kết quả kỳ vọng (expected result).
  - Kết quả thực tế (actual result).
  - Môi trường kiểm thử (test environment).
- **Ví dụ**: Kịch bản “Xác thực đăng nhập với tên người dùng và mật khẩu hợp lệ” được cụ thể hóa thành:
  - Bước 1: Nhập tên người dùng “user123”.
  - Bước 2: Nhập mật khẩu “pass123”.
  - Bước 3: Nhấn nút đăng nhập.
  - Kết quả kỳ vọng: Hệ thống chuyển hướng đến trang chính.

#### 5. Thực Hiện Kiểm Thử (Test Implementation)

- **Mục đích**: Chuẩn bị mọi thứ để sẵn sàng cho việc thực thi kiểm thử.
- **Hoạt động**:
  - Đảm bảo môi trường kiểm thử đã sẵn sàng (ví dụ: kiểm thử trên thiết bị di động thực tế hay trình mô phỏng/emulator).
  - Chuẩn bị dữ liệu kiểm thử (test data). Ví dụ: Thêm sản phẩm vào website thương mại điện tử để kiểm tra chức năng giỏ hàng, thanh toán, hoặc đánh giá.
- **Câu hỏi then chốt**: “Chúng ta đã sẵn sàng để bắt đầu thực thi kiểm thử chưa?”

#### 6. Thực Thi Kiểm Thử (Test Execution)

- **Mục đích**: Chạy các trường hợp kiểm thử và kịch bản kiểm thử.
- **Quy trình**:
  - So sánh kết quả thực tế (actual result) với kết quả kỳ vọng (expected result).
  - Nếu giống nhau: Trường hợp kiểm thử **đạt (passed)**.
  - Nếu khác nhau: Trường hợp kiểm thử **thất bại (failed)** → Viết báo cáo lỗi (defect report) gửi cho nhà phát triển.
- **Sau khi lỗi được sửa**:
  - Thực hiện **[[Testing-Debugging#Kiểm Thử Lại (Confirmation Testing/Retesting)|kiểm thử lại (retesting)]]** để xác minh lỗi đã được khắc phục.
  - Thực hiện **[[Testing-Debugging#Kiểm Thử Hồi Quy (Regression Testing)|kiểm thử hồi quy (regression testing)]]** để đảm bảo các phần không thay đổi không bị ảnh hưởng.

#### 7. Hoàn Tất Kiểm Thử (Test Completion)

- **Mục đích**: Kết thúc quy trình kiểm thử và bàn giao kết quả.
- **Hoạt động**:
  - Bàn giao tài liệu kiểm thử cho đội ngũ bảo trì (maintenance team).
  - Thông báo cho đội hỗ trợ kỹ thuật (technical support) về các vấn đề chưa giải quyết và cách khắc phục tạm thời (workarounds).
  - Viết **báo cáo hoàn tất kiểm thử (test completion report)** để quyết định xem ứng dụng có sẵn sàng triển khai cho người dùng cuối hay không.

### Đặc Điểm Chung của Quy Trình Kiểm Thử

- Quy trình kiểm thử áp dụng cho nhiều loại kiểm thử: kiểm thử thủ công (manual testing), kiểm thử di động (mobile testing), kiểm thử API, kiểm thử hiệu suất (performance testing), kiểm thử bảo mật (security testing), v.v.
- Dù loại kiểm thử hoặc [[Testing-level|mức độ kiểm thử (testing level)]] thay đổi, quy trình cơ bản vẫn bao gồm: **lập kế hoạch → phân tích → thiết kế → thực thi → hoàn tất**.
- Các hoạt động lập kế hoạch, giám sát và kiểm soát là liên tục, kéo dài suốt quy trình kiểm thử.

### Ghi Chú Thêm

- Quy trình kiểm thử của ISTQB là tiêu chuẩn phổ biến, nhưng mỗi công ty có thể điều chỉnh tùy theo nhu cầu.
- Các bước như phân tích và thiết kế kiểm thử là nền tảng cho các hoạt động thực hành trong kiểm thử phần mềm.

---

## Liên kết liên quan

- [[Software-testing|Tổng quan về Kiểm thử phần mềm]] - Khái niệm cơ bản
- [[Testing-level|Các Mức Độ Kiểm Thử]] - Áp dụng quy trình cho từng mức độ
- [[Dynamic-Static-Testing|Kiểm Thử Động và Tĩnh]] - Quy trình chủ yếu cho dynamic testing
- [[Testing-Debugging|Kiểm Thử vs Gỡ Lỗi]] - Thực thi, retesting và regression trong quy trình
- [[Object-of-testing|Mục Tiêu của Kiểm Thử]] - Mục tiêu được thực hiện qua 7 bước
