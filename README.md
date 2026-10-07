# BÁO CÁO LAB 7: KIỂM THỬ API BẰNG POSTMAN

- **Họ và tên:** Le Quang Thang
- **Mã sinh viên:** 23010236
- **Lớp:** CNTT_3

---

## 1. Giới thiệu công cụ Postman
Postman là công cụ phổ biến dùng để kiểm thử API, gửi các yêu cầu HTTP/HTTPS và kiểm tra kết quả phản hồi từ máy chủ.

## 2. Kết quả kiểm thử API

### 2.1. Kiểm thử Request GET (Lấy dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Phương thức:** GET
- **Mô tả:** Lấy thông tin bài viết có ID = 1.
- **Kết quả:** Status `200 OK`.
![GET Request](images/get_request.png)

### 2.2. Kiểm thử Request POST (Tạo mới dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts`
- **Phương thức:** POST
- **Mô tả:** Gửi payload JSON để tạo mới bài viết.
- **Kết quả:** Status `201 Created`.
![POST Request](images/post_request.png)

### 2.3. Kiểm thử Request DELETE (Xóa dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Phương thức:** DELETE
- **Mô tả:** Yêu cầu xóa bài viết có ID = 1.
- **Kết quả:** Status `200 OK`.
![DELETE Request](images/delete_request.png)

---
## 3. Kết luận
Đã nắm rõ quy trình gửi request, truyền tham số, truyền body JSON và kiểm tra Status Code trên Postman.
