# Chức năng tìm kiếm sản phẩm yêu cầu người dùng nhập từ khóa(từ 3 tới 50 ký tự) và có thể chọn một khoảng giá từ danh sách thả xuống (dưới 100k, từ 100k - 500k, trên 500k ), Hãy áp dụng kỹ thuật phân vùng tương đương để xác định lớp giá trị cho cả 2 đầu vào


## **Đầu vào 1 - Từ khóa (Keyword)**

| **Điều kiện** | **Lớp tương đương hợp lệ** | **Số thứ tự** | **Lớp tương đương không hợp lệ** | **Số thứ tự** |
| ------------- | -------------------------- | ------------- | -------------------------------- | ------------- |
| Từ khóa       | ​ [3-50]                   | 1             | keyword < 3 ký tự                | 2             |
|               |                            |               | keyword > 50 ký tự               | 3             |
	
## **Đầu vào 2 - Khoảng giá (Price Range)**

|**Điều kiện**|**Lớp tương đương hợp lệ**|**Số thứ tự**|**Lớp tương đương không hợp lệ**|**Số thứ tự**|
|---|---|---|---|---|
|Khoảng giá|Dưới 100k|4|Không chọn giá|5|
||Từ 100k - 500k|6|Giá trị không hợp lệ|7|
||Trên 500k|8|||