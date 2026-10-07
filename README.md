# LAB 7: KIỂM THỬ API BẰNG POSTMAN

## Thông tin sinh viên

- **Họ và tên:** Lê Quang Thắng
- **Mã sinh viên:** 23010236
- **Lớp:** CNTT_3
- **Nội dung thực hành:** Kiểm thử API bằng Postman

---

## 1. Mục tiêu bài thực hành

Bài thực hành nhằm làm quen với công cụ **Postman** và cách sử dụng Postman để gửi, kiểm tra các HTTP Request khi làm việc với REST API.

Sau khi hoàn thành bài thực hành, có thể:

- Làm quen với giao diện và các chức năng cơ bản của Postman.
- Hiểu cách gửi Request và nhận Response từ API.
- Thực hiện các phương thức HTTP cơ bản: `GET`, `POST`, `PUT`, `DELETE`.
- Biết cách truyền dữ liệu JSON trong Request Body.
- Kiểm tra HTTP Status Code của Response.
- Quan sát và kiểm tra dữ liệu JSON được Server trả về.
- Hiểu cách các phương thức HTTP tương ứng với các thao tác CRUD.

---

## 2. Công cụ và API sử dụng

### 2.1. Postman

**Postman** là công cụ hỗ trợ phát triển và kiểm thử API. Postman cho phép gửi các HTTP Request đến Server và kiểm tra Response mà không cần xây dựng một ứng dụng Client riêng.

Trong bài thực hành này, Postman được sử dụng để:

- Gửi HTTP Request.
- Thiết lập URL và HTTP Method.
- Truyền dữ liệu JSON trong Request Body.
- Kiểm tra HTTP Status Code.
- Kiểm tra Response Body trả về từ Server.

### 2.2. API kiểm thử

Bài thực hành sử dụng **JSONPlaceholder**, một REST API giả lập được sử dụng cho mục đích học tập và kiểm thử.

**Base URL:**

```text
https://jsonplaceholder.typicode.com
```

Tài nguyên được sử dụng:

```text
/posts
```

Các API Endpoint được kiểm thử:

| Method | Endpoint | Chức năng |
|---|---|---|
| GET | `/posts/1` | Lấy thông tin bài viết |
| POST | `/posts` | Tạo bài viết mới |
| PUT | `/posts/1` | Cập nhật bài viết |
| DELETE | `/posts/1` | Xóa bài viết |

---

## 3. Kiến thức cơ bản

### 3.1. REST API

REST API cho phép Client và Server trao đổi dữ liệu thông qua giao thức HTTP.

Trong bài thực hành, dữ liệu trao đổi giữa Client và Server chủ yếu sử dụng định dạng **JSON**.

Bốn phương thức HTTP được sử dụng tương ứng với các thao tác CRUD:

| HTTP Method | CRUD | Ý nghĩa |
|---|---|---|
| POST | Create | Tạo mới dữ liệu |
| GET | Read | Đọc/lấy dữ liệu |
| PUT | Update | Cập nhật dữ liệu |
| DELETE | Delete | Xóa dữ liệu |

### 3.2. HTTP Status Code

HTTP Status Code cho biết kết quả xử lý Request của Server.

Một số Status Code được sử dụng trong bài:

- `200 OK`: Request được xử lý thành công.
- `201 Created`: Tài nguyên mới được tạo thành công.

---

# 4. Kết quả thực hiện

## 4.1. Kiểm thử GET Request

### Mục đích

Sử dụng phương thức `GET` để lấy thông tin của bài viết có **ID = 1**.

### Thông tin Request

**Method:**

```text
GET
```

**URL:**

```text
https://jsonplaceholder.typicode.com/posts/1
```

GET Request trong trường hợp này không cần truyền Request Body.

### Kết quả mong đợi

Server trả về:

```text
200 OK
```

Response Body chứa thông tin bài viết có `id = 1`.

### Kết quả thực tế

Postman trả về Status Code:

```text
200 OK
```

Response Body trả về dữ liệu JSON chứa thông tin của bài viết, bao gồm các trường như:

- `userId`
- `id`
- `title`
- `body`

### Hình ảnh kết quả

<img width="1607" height="1007" alt="GET Request" src="https://github.com/user-attachments/assets/e5bfc808-2f63-4183-9e85-70aa2cab467e" />

### Nhận xét

Request `GET` được thực hiện thành công. Server trả về đúng bài viết có ID bằng 1 và Status Code `200 OK` đúng với kết quả mong đợi.

**Kết quả: `PASS`**

---

## 4.2. Kiểm thử POST Request

### Mục đích

Sử dụng phương thức `POST` để gửi dữ liệu lên Server và tạo một bài viết mới.

### Thông tin Request

**Method:**

```text
POST
```

**URL:**

```text
https://jsonplaceholder.typicode.com/posts
```

Dữ liệu được gửi lên Server thông qua Request Body dưới định dạng JSON.

Trong Postman lựa chọn:

```text
Body → raw → JSON
```

### Kết quả mong đợi

Khi Server tiếp nhận và xử lý yêu cầu tạo mới thành công, Status Code mong đợi là:

```text
201 Created
```

Response Body trả về thông tin của tài nguyên vừa được tạo.

### Kết quả thực tế

Postman trả về:

```text
201 Created
```

Server đồng thời trả về Response Body chứa thông tin bài viết được tạo.

### Hình ảnh kết quả

<img width="1610" height="1000" alt="POST Request" src="https://github.com/user-attachments/assets/06fca4eb-a22e-4a78-9881-a2407084a6f5" />

### Nhận xét

Request `POST` được thực hiện thành công. Dữ liệu JSON được gửi đến Server và Server trả về Status Code `201 Created`, phù hợp với chức năng tạo mới tài nguyên.

**Kết quả: `PASS`**

---

## 4.3. Kiểm thử PUT Request

### Mục đích

Sử dụng phương thức `PUT` để cập nhật thông tin của bài viết có **ID = 1**.

### Thông tin Request

**Method:**

```text
PUT
```

**URL:**

```text
https://jsonplaceholder.typicode.com/posts/1
```

Thông tin cần cập nhật được gửi đến Server thông qua Request Body dưới dạng JSON.

Trong Postman lựa chọn:

```text
Body → raw → JSON
```

### Kết quả mong đợi

Server xử lý yêu cầu cập nhật thành công và trả về:

```text
200 OK
```

Response Body chứa thông tin của bài viết sau khi cập nhật.

### Kết quả thực tế

Postman trả về:

```text
200 OK
```

Response Body trả về dữ liệu JSON của tài nguyên sau khi thực hiện cập nhật.

### Hình ảnh kết quả

<img width="1600" height="990" alt="PUT Request" src="https://github.com/user-attachments/assets/efc99bb6-4ba8-4b6c-8779-6b6e3f10df11" />

### Nhận xét

Request `PUT` được thực hiện thành công. Server tiếp nhận dữ liệu cập nhật và trả về Status Code `200 OK`, đúng với kết quả mong đợi.

**Kết quả: `PASS`**

---

## 4.4. Kiểm thử DELETE Request

### Mục đích

Sử dụng phương thức `DELETE` để gửi yêu cầu xóa bài viết có **ID = 1**.

### Thông tin Request

**Method:**

```text
DELETE
```

**URL:**

```text
https://jsonplaceholder.typicode.com/posts/1
```

Trong trường hợp này không cần gửi Request Body vì tài nguyên cần xóa đã được xác định thông qua ID trên URL.

### Kết quả mong đợi

Server tiếp nhận và xử lý yêu cầu xóa thành công.

Status Code mong đợi:

```text
200 OK
```

### Kết quả thực tế

Postman trả về:

```text
200 OK
```

Điều này cho thấy yêu cầu xóa tài nguyên đã được Server tiếp nhận và xử lý thành công.

### Hình ảnh kết quả

<img width="1603" height="1003" alt="DELETE Request" src="https://github.com/user-attachments/assets/3ebfc8ba-684c-4bd6-8a43-0bd74e2a25af" />

### Nhận xét

Request `DELETE` được thực hiện thành công. Server trả về Status Code `200 OK`, phù hợp với kết quả mong đợi.

**Kết quả: `PASS`**

---

# 5. Tổng hợp kết quả kiểm thử

Sau khi thực hiện bốn HTTP Request bằng Postman, kết quả thu được như sau:

| STT | Method | Endpoint | Chức năng | Kết quả mong đợi | Kết quả thực tế | Đánh giá |
|---:|---|---|---|---|---|---|
| 1 | GET | `/posts/1` | Lấy bài viết ID = 1 | `200 OK` | `200 OK` | PASS |
| 2 | POST | `/posts` | Tạo bài viết mới | `201 Created` | `201 Created` | PASS |
| 3 | PUT | `/posts/1` | Cập nhật bài viết ID = 1 | `200 OK` | `200 OK` | PASS |
| 4 | DELETE | `/posts/1` | Xóa bài viết ID = 1 | `200 OK` | `200 OK` | PASS |

### Kết quả chung

- **Tổng số Test Case:** 4
- **Test Case thành công:** 4
- **Test Case thất bại:** 0
- **Tỷ lệ PASS:** 100%

Tất cả các Request đều trả về Status Code phù hợp với kết quả mong đợi.

---

# 6. Kết quả đạt được

Sau khi hoàn thành bài thực hành, em đã:

- Biết cách sử dụng các chức năng cơ bản của Postman.
- Biết cách gửi HTTP Request đến REST API.
- Thực hiện được các phương thức `GET`, `POST`, `PUT` và `DELETE`.
- Biết cách truyền dữ liệu JSON thông qua Request Body.
- Biết cách đọc HTTP Status Code.
- Biết cách kiểm tra Response Body của API.
- Hiểu rõ hơn mối quan hệ giữa HTTP Method và các thao tác CRUD.
- Biết cách sử dụng Postman để kiểm tra API trước khi tích hợp API vào một ứng dụng.

---

# 7. Kết luận

Qua bài Lab 7, em đã thực hành sử dụng **Postman** để kiểm thử REST API thông qua bốn phương thức HTTP cơ bản gồm `GET`, `POST`, `PUT` và `DELETE`.

Kết quả kiểm thử cho thấy cả **4/4 Test Case đều thực hiện thành công**. Request GET, PUT và DELETE trả về Status Code `200 OK`, trong khi Request POST trả về `201 Created`. Các kết quả thực tế đều phù hợp với kết quả mong đợi.

Thông qua bài thực hành, em đã hiểu rõ hơn quá trình Client gửi Request đến Server, Server xử lý yêu cầu và trả Response về Client. Đồng thời, em cũng đã làm quen với việc truyền dữ liệu JSON, kiểm tra Status Code và phân tích kết quả Response bằng Postman.

Bài thực hành là nền tảng để tiếp tục tìm hiểu về REST API, phát triển Backend và kiểm thử API trong các ứng dụng Web sau này.

---

# 8. Tài liệu tham khảo

1. **Video hướng dẫn Postman theo tài liệu Lab 7:**  
   https://www.youtube.com/watch?v=MFxk5BZulVU

2. **Postman Documentation:**  
   https://learning.postman.com/docs/

3. **JSONPlaceholder – Free Fake REST API:**  
   https://jsonplaceholder.typicode.com/

---

**Sinh viên thực hiện:** Lê Quang Thắng  
**Mã sinh viên:** 23010236  
**Lớp:** CNTT_3
