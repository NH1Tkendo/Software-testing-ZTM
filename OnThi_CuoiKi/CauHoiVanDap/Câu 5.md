# Một ứng dụng web hiển thị hoàn hảo trên máy tính nhưng khi mở bằng trình duyệt trên điện thoại, các nút bấm quá nhỏ và viền bị tràn ra ngoài màn hình. Vấn đề này thuộc loại hình kiểm thử nào và giải pháp đề xuất là gì?

Vấn đề này thuộc loại [[Kiểm thử tương thích]] (Compatibility Testing), cụ thể là kiểm thử tương thích trên các thiết bị và trình duyệt khác nhau

## **Giải pháp đề xuất**

**1. Phía phát triển (Development):**​

- Áp dụng **Mobile-First Design** - thiết kế cho mobile trước, sau đó mở rộng lên desktop
    
- Sử dụng **Responsive CSS** với media queries cho các breakpoints:
    
    - Mobile: 320px - 480px
        
    - Tablet: 481px - 768px
        
    - Desktop: 769px+
        
- Sử dụng **Flexbox** hoặc **CSS Grid** thay vì fixed width
    
- Đặt kích thước nút tối thiểu **44×44px** (tiêu chuẩn khuyến nghị)
    

**2. Phía kiểm thử (Testing):**​

**Kiểm thử khả năng tương thích:**​

- Kiểm thử trên **nhiều độ phân giải khác nhau**: 320px, 480px, 768px, 1024px, 1920px
    
- Kiểm thử trên **các thiết bị thực** (iPhone, Samsung Galaxy, iPad...) hoặc công cụ mô phỏng như Chrome DevTools
    
- Kiểm thử trên **các trình duyệt khác nhau** (Chrome, Safari, Firefox, Edge) trên cả mobile và desktop
    

**Kiểm thử khả năng sử dụng:**​

- Kiểm thử **kích thước và vị trí nút**: các nút phải dễ bấm trên màn hình cảm ứng
    
- Kiểm thử **hiển thị nội dung**: văn bản, hình ảnh không bị tràn hoặc bị cắt
    
- Kiểm thử **cuộn trang**: thanh cuộn chỉ hiển thị khi cần thiết
    
- Kiểm thử **định hướng màn hình**: dọc (portrait) và ngang (landscape)