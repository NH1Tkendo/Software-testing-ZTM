# Tại sao việc đạt 100% bao phủ câu lệnh không đảm bảo tất cả các lỗi logic được phát hiển ?

Vì bao phủ câu lệnh chỉ đảm bảo toàn bộ câu lệnh trong mã nguồn được thực hiện ít nhất một lần, bao gồm các điểm quyết định. Vì các điểm quyết định chỉ được kiểm tra một lần thay vì kiểm tra cả giá trị TRUE và FALSE của chúng cho nên có thể bỏ qua lỗi về logic của điểm quyết định. nghĩa là các điểm quyết định có thể chứa lỗi về logic mà bao phủ câu lệnh không phát hiện ra được
