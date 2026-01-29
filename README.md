# KỸ NGHỆ YÊU CẦU PHẦN MỀM

## ĐỀ CƯƠNG DỰ ÁN – ObserOne

**Phiên bản:** 1.2  \
**Ngày:** 22/01/2026

---

## 1. Tên đề tài

**Xây dựng hệ thống phát hiện và phản ứng sự cố an ninh trên máy tính (EDR) dựa trên phân tích hành vi và giám sát qua nền tảng web**

---

## 2. Tổng quan dự án

ObserOne là một hệ thống **Endpoint Detection and Response (EDR)** dựa trên phân tích hành vi, được thiết kế để giám sát, phát hiện và phản ứng các sự cố an ninh trên máy tính người dùng. Hệ thống kết hợp **AI cục bộ (Local AI)** tại endpoint và **AI trên nền tảng cloud (Cloud AI)**, đồng thời cung cấp **giao diện web** để giám sát và quản lý tập trung.

---

## 3. Nhóm người dùng & các bên liên quan

Hệ thống ObserOne phục vụ **03 nhóm người dùng chính**, mỗi nhóm có vai trò, mục tiêu và chức năng sử dụng khác nhau.

---

## 4. Nhóm người dùng 1: Chủ đầu tư / Đơn vị sở hữu hệ thống

### 4.1 Mô tả
Là tổ chức hoặc cá nhân đầu tư, sở hữu và định hướng phát triển hệ thống. Nhóm này không thao tác kỹ thuật trực tiếp mà quan tâm đến hiệu quả tổng thể, mức độ an toàn và khả năng mở rộng lâu dài của hệ thống.

### 4.2 Mục tiêu
- Đảm bảo toàn bộ hệ thống máy tính được bảo vệ an ninh
- Theo dõi tình trạng an toàn tổng thể
- Hỗ trợ ra quyết định chiến lược dựa trên báo cáo

### 4.3 Chức năng
- Xem **dashboard tổng quan an ninh hệ thống**
- Xem báo cáo thống kê (ngày / tuần / tháng)
- Theo dõi số lượng và mức độ sự cố an ninh
- Theo dõi trạng thái hoạt động của hệ thống
- Cấu hình chính sách an ninh ở mức cao

### 4.4 Yêu cầu phi chức năng
- Giao diện trực quan, dễ hiểu
- Độ ổn định và sẵn sàng cao
- Phân quyền truy cập rõ ràng và bảo mật

---

## 5. Nhóm người dùng 2: Đơn vị vận hành – IT / An ninh mạng

### 5.1 Mô tả
Là nhóm trực tiếp vận hành hệ thống hằng ngày thông qua nền tảng web. Nhóm này chịu trách nhiệm giám sát, phân tích, điều tra và phản ứng các sự cố an ninh.

### 5.2 Mục tiêu
- Giám sát máy tính theo thời gian thực
- Phát hiện và xử lý kịp thời các mối đe dọa
- Quản lý agent và chính sách an ninh

### 5.3 Chức năng
- Đăng nhập và sử dụng hệ thống web
- Theo dõi trạng thái các endpoint theo thời gian thực
- Nhận và xử lý cảnh báo an ninh
- Phân tích hành vi và sự kiện nghi vấn
- Thực hiện phản ứng (kill process, cô lập máy, chặn kết nối)
- Quản lý agent (thêm, xóa, cập nhật)
- Cấu hình luật phát hiện và ngưỡng cảnh báo
- Xem log chi tiết và dữ liệu phục vụ điều tra

### 5.4 Yêu cầu phi chức năng
- Hiển thị dữ liệu thời gian thực, độ trễ thấp
- Độ chính xác cao, giảm cảnh báo giả
- Bảo mật dữ liệu và kênh truyền thông
- Khả năng mở rộng cho nhiều máy tính

---

## 6. Nhóm người dùng 3: Người dùng cuối (được bảo vệ)

### 6.1 Mô tả
Là người sử dụng máy tính được cài đặt agent. Nhóm này không quản trị hệ thống nhưng chịu ảnh hưởng trực tiếp từ các phản ứng bảo mật.

### 6.2 Mục tiêu
- Sử dụng máy tính an toàn, không phức tạp
- Nhận cảnh báo rõ ràng khi có nguy cơ an ninh
- Phối hợp với đơn vị IT khi cần thiết

### 6.3 Chức năng
- Nhận thông báo cục bộ khi phát hiện hành vi bất thường
- Xem thông tin cảnh báo cơ bản trên máy
- Xác nhận hoặc từ chối hành động (nếu được cho phép)
- Được bảo vệ ngay cả khi mất kết nối Internet

### 6.4 Yêu cầu phi chức năng
- Ít ảnh hưởng đến hiệu năng máy tính
- Thông báo đơn giản, không gây phiền nhiễu
- Hoạt động ổn định, liên tục

---

## 7. Chức năng phát hiện dựa trên AI

### 7.1 AI cục bộ (Local AI)
- Học hành vi sử dụng bình thường của từng máy
- Phát hiện bất thường về tiến trình, file và mạng
- Phản ứng nhanh mà không phụ thuộc cloud
- Hoạt động khi mất kết nối Internet

### 7.2 AI trên Cloud (Cloud AI)
- Tương quan sự kiện từ nhiều endpoint
- Phát hiện các cuộc tấn công diện rộng
- Huấn luyện và cập nhật mô hình AI toàn cục
- Phân phối luật và mô hình xuống agent

---

## 8. Tổng quan kiến trúc hệ thống

Hệ thống được thiết kế theo mô hình **3 lớp**:

1. **Agent (Endpoint):** Giám sát hành vi, Local AI, phản ứng sự cố
2. **Backend Cloud:** Xử lý dữ liệu, lưu trữ, Cloud AI
3. **Web Dashboard:** Giám sát, quản lý và báo cáo tập trung

Thiết kế này đảm bảo khả năng bảo vệ thời gian thực và quản lý tập trung hiệu quả.

---

## 9. Khả dụng và độ tin cậy

- Hệ thống hoạt động 24/7
- Agent vẫn bảo vệ cơ bản khi offline
- Cloud được thiết kế sẵn sàng cao

---

## 10. Hướng phát triển mở rộng

- Tích hợp SIEM
- Threat Hunting nâng cao
- Báo cáo tuân thủ tự động
- Hỗ trợ thêm nhiều hệ điều hành
