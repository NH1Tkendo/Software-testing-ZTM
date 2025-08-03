## Kiểm thử phần mềm (Software Testing)

### Khái niệm kiểm thử phần mềm

- **Định nghĩa**: Kiểm thử phần mềm (Software Testing) là quá trình đánh giá chất lượng của phần mềm (software quality) và giảm thiểu rủi ro xảy ra lỗi trong quá trình vận hành.
  - Theo tài liệu ISTQB (International Software Testing Qualifications Board), kiểm thử phần mềm được sử dụng để:
    - Đánh giá chất lượng phần mềm.
    - Giảm thiểu rủi ro lỗi (software failure) khi phần mềm được triển khai.
- **Không chỉ là thực thi kiểm thử (test execution)**:
  - Kiểm thử phần mềm không chỉ bao gồm việc chạy thử và kiểm tra đầu ra (output) từ đầu vào (input) – còn gọi là [[Dynamic-Static-Testing#Kiểm Thử Động (Dynamic Testing)|kiểm thử động (dynamic testing)]].
  - Đây là một quá trình bao gồm nhiều hoạt động, trong đó thực thi kiểm thử chỉ là một phần.

### Tại sao cần kiểm thử phần mềm?

- **Hệ quả của lỗi phần mềm (defects/failures)**:

  - **Tổn thất tài chính (loss of money)**:
    - Chi phí phát triển tính năng mới hoặc sửa lỗi sau khi phát hiện.
    - Khách hàng không hài lòng, yêu cầu hoàn tiền.
  - **Tổn thất thời gian (loss of time)**: Thời gian tiêu tốn để sửa lỗi.
  - **Tổn hại danh tiếng doanh nghiệp (business reputation)**:
    - Phần mềm chứa nhiều lỗi có thể làm giảm uy tín công ty.
    - Người dùng có thể mất niềm tin, đặc biệt nếu phần mềm có lỗ hổng bảo mật (security threats).
  - **Hậu quả nghiêm trọng**:
    - Trong các hệ thống nhúng (embedded systems) hoặc phần mềm liên quan đến phần cứng (ví dụ: ô tô, máy bay), lỗi có thể dẫn đến tai nạn, thương tích hoặc tử vong (injury or death).

- **Vai trò của kiểm thử phần mềm**:
  - Phát hiện lỗi sớm trong chu kỳ phát triển phần mềm (software development lifecycle) để:
    - Ngăn chặn lỗi xuất hiện trong giai đoạn vận hành (operation).
    - Tiết kiệm chi phí, thời gian và bảo vệ danh tiếng doanh nghiệp.
  - Đảm bảo chất lượng phần mềm đáp ứng yêu cầu người dùng.

### Quá trình kiểm thử phần mềm

- **Gồm nhiều hoạt động**:
  - Kiểm thử phần mềm không chỉ là thực thi kiểm thử mà bao gồm **7 hoạt động chính** (chi tiết xem [[Testing-process|Quy Trình Kiểm Thử Phần Mềm]]), ví dụ:
    - Lập kế hoạch (planning).
    - Phân tích (analysis).
    - Thiết kế (design).
    - Thực thi kiểm thử (test execution).
- **Tầm quan trọng của tester chuyên trách**:
  - Trong quá khứ (ví dụ: thời kỳ phát triển Windows 95, XP), lập trình viên thường tự kiểm thử phần mềm.
  - Ngày nay, vai trò kiểm thử viên (software tester) được chuyên môn hóa để đảm bảo chất lượng tốt hơn.

### Ghi chú thêm

- **ISTQB (International Software Testing Qualifications Board)**: Tổ chức cung cấp các chứng chỉ kiểm thử phần mềm, tài liệu của họ là nguồn tham khảo quan trọng để định nghĩa và hiểu về kiểm thử phần mềm.
- Kiểm thử phần mềm là một quá trình liên tục, bắt đầu từ giai đoạn phát triển (development) và xuyên suốt vòng đời phần mềm.

---

## Liên kết nội dung

### Khái niệm cơ bản

- [[Object-of-testing|Mục Tiêu của Kiểm Thử Phần Mềm]] - Tìm hiểu 7 mục tiêu chính của kiểm thử
- [[Dynamic-Static-Testing|Kiểm Thử Động và Tĩnh]] - Phân biệt hai loại kiểm thử chính
- [[Verification-validation|Xác Minh và Xác Thực]] - Hiểu sự khác biệt giữa building right vs building the right product

### Quy trình và phương pháp

- [[Testing-process|Quy Trình Kiểm Thử]] - 7 bước chuẩn của ISTQB
- [[Testing-level|Các Mức Độ Kiểm Thử]] - Từ unit testing đến acceptance testing
- [[Testing-type|Các Loại Kiểm Thử]] - Functional, non-functional, black-box, white-box

### Thực hành

- [[Testing-Debugging|Kiểm Thử vs Gỡ Lỗi]] - Phân biệt vai trò tester và developer
