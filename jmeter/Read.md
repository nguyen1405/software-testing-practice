# 📊 JMeter Performance Test Report

## 👨‍💻 Student Information
- Họ và tên: Hoàng Xuân Nguyên
- Môn học: Kiểm thử phần mềm
- Công cụ sử dụng: Apache JMeter 5.6.3

---

## 🌐 Website được kiểm thử
Website:  https://www.wikipedia.org

Mục tiêu: Đánh giá hiệu năng phản hồi của website khi có nhiều người dùng truy cập đồng thời.

---

## ⚙️ Cấu hình kiểm thử chung

- Công cụ: Apache JMeter
- Giao thức: HTTP/HTTPS
- Phương thức yêu cầu: GET
- Listener sử dụng:
  - View Results Tree
  - Summary Report
  - Aggregate Report

---

# 🧪 KỊCH BẢN KIỂM THỬ

## 🔹 Thread Group 1 – Kịch bản cơ bản

| Thông số | Giá trị |
|---------|--------|
| Số người dùng (Threads) | 10 |
| Ramp-up Period | 10 giây |
| Loop Count | 5 |
| Hành vi | Truy cập trang chủ |

### 📈 Kết quả

| Chỉ số | Giá trị |
|-------|--------|
| Average Response Time | [xxx] ms |
| Min Response Time | [xxx] ms |
| Max Response Time | [xxx] ms |
| Throughput | [xxx] requests/second |
| Error Rate | [x] % |

📷 Hình minh chứng:  
*(Chèn ảnh Summary Report của Thread Group 1 vào đây)*

---

## 🔹 Thread Group 2 – Kịch bản tải nặng

| Thông số | Giá trị |
|---------|--------|
| Số người dùng | 50 |
| Ramp-up Period | 30 giây |
| Loop Count | 3 |
| Hành vi | Truy cập trang chủ + 1 trang con |

### 📈 Kết quả

| Chỉ số | Giá trị |
|-------|--------|
| Average Response Time | [xxx] ms |
| Min Response Time | [xxx] ms |
| Max Response Time | [xxx] ms |
| Throughput | [xxx] requests/second |
| Error Rate | [x] % |

📷 Hình minh chứng:  
*(Chèn ảnh Summary Report của Thread Group 2 vào đây)*

---

## 🔹 Thread Group 3 – Kịch bản tùy chỉnh

| Thông số | Giá trị |
|---------|--------|
| Số người dùng | 20 |
| Thời gian chạy | 60 giây |
| Hành vi | Truy cập 2 trang con khác nhau |

### 📈 Kết quả

| Chỉ số | Giá trị |
|-------|--------|
| Average Response Time | [xxx] ms |
| Min Response Time | [xxx] ms |
| Max Response Time | [xxx] ms |
| Throughput | [xxx] requests/second |
| Error Rate | [x] % |

📷 Hình minh chứng:  
*(Chèn ảnh Summary Report của Thread Group 3 vào đây)*

---

# 📊 Nhận xét & Phân tích

- Khi số lượng người dùng tăng lên, **thời gian phản hồi trung bình tăng** do server phải xử lý nhiều request cùng lúc.
- Throughput tăng ở kịch bản tải nặng cho thấy hệ thống vẫn xử lý được nhiều yêu cầu mỗi giây.
- Tỉ lệ lỗi thấp (hoặc bằng 0%) chứng tỏ hệ thống hoạt động ổn định trong phạm vi kiểm thử.
- Nếu thời gian phản hồi tăng cao hoặc xuất hiện lỗi nhiều, cần xem xét:
  - Tối ưu backend
  - Tối ưu truy vấn cơ sở dữ liệu
  - Sử dụng cache hoặc CDN

---

# 📁 File đính kèm trong thư mục `/jmeter`

- `performance_test.jmx` – File kịch bản JMeter  
- `result_threadgroup1.csv` – Kết quả test kịch bản 1  
- `result_threadgroup2.csv` – Kết quả test kịch bản 2  
- `result_threadgroup3.csv` – Kết quả test kịch bản 3  
- Ảnh chụp màn hình kết quả Summary Report

---

# ✅ Kết luận

Bài kiểm thử đã mô phỏng nhiều mức tải người dùng khác nhau để đánh giá khả năng đáp ứng của hệ thống.  
Kết quả cho thấy website có thể hoạt động ổn định trong phạm vi kiểm thử đã thiết lập.

