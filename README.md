# KỸ NGHỆ YÊU CẦU PHẦN MỀM

## ĐỀ CƯƠNG DỰ ÁN (PROJECT PROPOSAL)

**Phiên bản:** 1.1
**Ngày:**

---

## TÊN ĐỀ TÀI

**Xây dựng hệ thống phát hiện và phản ứng sự cố an ninh trên máy tính (EDR) dựa trên phân tích hành vi và giám sát qua nền tảng web**

---

## THỰC HIỆN BỞI NHÓM _LỚP

*(Cập nhật theo thông tin nhóm thực tế)*

---

## XÁC NHẬN CỦA GIẢNG VIÊN HƯỚNG DẪN

| Họ tên | Chữ ký | Ngày |
|------|--------|------|
|      |        |      |

---

# THÔNG TIN DỰ ÁN

**Tên viết tắt dự án:** ObserOne  
**Tên đầy đủ dự án:** ObserOne – Hệ thống EDR dựa trên phân tích hành vi  
**Thời gian bắt đầu:**  
**Thời gian kết thúc:**  

**Đơn vị chủ trì:**  
**Giảng viên hướng dẫn:**  
**Chủ đầu tư / Đơn vị sở hữu hệ thống:**  

**Trưởng nhóm & Thông tin liên hệ:**  
Họ tên:  
Email:  
SĐT:  
MSSV:  

**Đơn vị phối hợp:**  
**Website dự án:**  

---

## DANH SÁCH THÀNH VIÊN NHÓM

| MSSV | Họ tên | Email | SĐT |
|------|--------|-------|-----|
|      |        |       |     |

---

## LỊCH SỬ CẬP NHẬT

| Phiên bản | Ngày | Mô tả | Người thực hiện | Phê duyệt |
|----------|------|-------|----------------|----------|
| 1.0 | | Phát hành lần đầu | Tất cả thành viên | |

---

## 1. Tên đề tài

Xây dựng hệ thống phát hiện và phản ứng sự cố an ninh trên máy tính (EDR) dựa trên phân tích hành vi và giám sát qua nền tảng web.

---

## 2. Thành viên nhóm

| Họ tên | MSSV | Vai trò | Email |
|------|------|--------|-------|
| | | Trưởng nhóm | |
| | | Phát triển Agent | |
| | | Phát triển Backend | |
| | | Phát triển Frontend | |

---

## 3. Giảng viên hướng dẫn

| Họ tên | Email | Khoa |
|------|-------|------|
| | | |

---

## 4. Mô tả vấn đề (Problem Statement)

Trong bối cảnh công nghệ thông tin phát triển mạnh mẽ, các máy tính cá nhân và hệ thống doanh nghiệp ngày càng đối mặt với nhiều mối đe dọa an ninh mạng như virus, mã độc, ransomware và các hình thức tấn công chưa từng được biết đến trước đó. Các giải pháp antivirus truyền thống chủ yếu dựa trên chữ ký nên gặp nhiều hạn chế trong việc phát hiện các mối đe dọa mới.

Hiện nay, nhiều tổ chức và cá nhân chưa có một hệ thống tập trung có khả năng giám sát hành vi máy tính theo thời gian thực, tự động phát hiện bất thường và phản ứng kịp thời khi xảy ra tấn công. Do đó, việc xây dựng một hệ thống EDR dựa trên phân tích hành vi và giám sát qua web là cần thiết.

---

## 5. Khảo sát các giải pháp hiện có

Các phần mềm diệt virus truyền thống chỉ cung cấp khả năng bảo vệ cơ bản và phụ thuộc nhiều vào cơ sở dữ liệu chữ ký. Một số giải pháp EDR thương mại hiện đại có khả năng phát hiện nâng cao nhưng chi phí cao, khó tiếp cận và không phù hợp cho mục đích học tập, nghiên cứu.

Dự án ObserOne hướng đến xây dựng một hệ thống EDR đơn giản, dễ mở rộng, giúp sinh viên và tổ chức nhỏ tiếp cận mô hình bảo mật hiện đại.

---

## 6. Mục tiêu và phạm vi

### Mục tiêu
- Xây dựng agent giám sát hành vi máy tính theo thời gian thực
- Phát hiện hành vi bất thường và mã độc dựa trên phân tích hành vi
- Tự động phản ứng để giảm thiểu thiệt hại khi xảy ra tấn công
- Cung cấp nền tảng web để giám sát và quản lý tập trung

### Phạm vi
- Giám sát máy tính cá nhân và máy trạm
- Thu thập và phân tích hành vi hệ thống
- Hiển thị cảnh báo và thông tin trên giao diện web

---

## 7. Các chức năng và yêu cầu hệ thống

### 7.1 Chức năng chính
- Giám sát tiến trình, file và kết nối mạng
- Phát hiện hành vi bất thường
- Phản ứng tự động khi phát hiện mối đe dọa
- Gửi dữ liệu và cảnh báo lên hệ thống cloud
- Hiển thị thông tin theo thời gian thực trên web
- **Phân tích và phát hiện bằng AI cục bộ (Local AI)**
- **Phân tích nâng cao và tương quan sự kiện bằng AI trên cloud (Cloud AI)**

### 7.2 Chức năng AI (Local AI & Cloud AI)

#### a) AI cục bộ tại Agent (Local AI)
AI cục bộ được triển khai trực tiếp trên máy tính người dùng và **tự huấn luyện dựa trên hành vi sử dụng thực tế của từng máy**, nhằm đảm bảo khả năng phát hiện chính xác và phản ứng nhanh ngay tại endpoint.

Local AI có thể thực hiện:
- Học và xây dựng baseline hành vi bình thường của người dùng trên máy đó
- Phân tích hành vi tiến trình theo thời gian thực
- Phát hiện bất thường so với thói quen sử dụng thông thường
- Nhận diện các dấu hiệu tấn công như ransomware và malware hành vi
- Tự động đưa ra quyết định phản ứng ban đầu (kill process, cách ly file, chặn kết nối)
- Hoạt động độc lập ngay cả khi mất kết nối Internet
- Giảm tải công việc giám sát thủ công cho đơn vị vận hành

#### b) AI trên Cloud (Cloud AI)
AI trên cloud được **huấn luyện và quản lý bởi nhà phát triển hệ thống (Dev)**, đóng vai trò là mô hình trí tuệ nhân tạo mang tính **toàn cục** cho toàn bộ hệ thống.

Cloud AI có thể thực hiện:
- Phân tích và tương quan sự kiện từ nhiều máy tính khác nhau
- Phát hiện các chiến dịch tấn công có tính lan rộng
- Học tập từ dữ liệu tổng hợp và các mẫu tấn công phổ biến
- Cập nhật mô hình AI chuẩn và phân phối xuống các agent
- Đánh giá mức độ rủi ro và ưu tiên cảnh báo
- Đề xuất biện pháp xử lý cho đơn vị vận hành

### 7.3 Yêu cầu chức năng
- Người dùng có thể đăng nhập / đăng xuất hệ thống
- Agent thu thập và gửi dữ liệu hành vi
- Hệ thống phát hiện và cảnh báo sự cố an ninh
- Quản trị viên có thể theo dõi và xử lý sự cố từ xa

### 7.3 Yêu cầu phi chức năng
- Hiệu năng cao, ít ảnh hưởng đến hệ thống
- Bảo mật dữ liệu và kênh truyền thông
- Khả năng mở rộng cho nhiều máy tính
- Hoạt động ổn định và liên tục

---

## 8. Khả dụng hệ thống

Hệ thống được thiết kế hoạt động liên tục 24/7. Agent vẫn duy trì khả năng bảo vệ cơ bản ngay cả khi mất kết nối với hệ thống cloud.

---

## 9. Đối tượng sử dụng

Hệ thống ObserOne được thiết kế phục vụ **hai nhóm người dùng chính**, tập trung vào quản lý và vận hành hệ thống. Người dùng cuối không được xem là một nhóm người dùng độc lập mà là **đối tượng nhận cảnh báo và được bảo vệ bởi hệ thống**.

- **Chủ đầu tư / Đơn vị sở hữu hệ thống**: Là bên đầu tư, sở hữu và định hướng phát triển hệ thống. Nhóm này quan tâm đến hiệu quả tổng thể, mức độ an toàn của hệ thống, các báo cáo thống kê và khả năng mở rộng trong dài hạn nhằm phục vụ công tác quản lý và ra quyết định chiến lược.

- **Đơn vị vận hành và quản lý hệ thống (IT / An ninh mạng)**: Là nhóm trực tiếp sử dụng hệ thống hằng ngày thông qua nền tảng web. Nhóm này có nhiệm vụ giám sát các máy tính, theo dõi cảnh báo an ninh, phân tích hành vi bất thường, điều tra sự cố và thực hiện các biện pháp phản ứng như chặn mã độc, cô lập thiết bị hoặc điều chỉnh chính sách bảo mật.

Ngoài hai nhóm trên, **người dùng cuối** là đối tượng được hệ thống bảo vệ và **nhận các cảnh báo an ninh tự động** (ví dụ: phát hiện hành vi bất thường, nguy cơ mã độc, khuyến nghị hành động). Người dùng cuối không trực tiếp quản trị hệ thống mà phối hợp thực hiện các hướng dẫn từ đơn vị vận hành khi cần thiết.

---

## 10. Tổng quan kiến trúc hệ thống

### Mô tả sơ đồ ngữ cảnh hệ thống

- Agent cài đặt trên máy tính người dùng để giám sát và phản ứng sự cố
- Backend cloud tiếp nhận, xử lý và lưu trữ dữ liệu
- Giao diện web hiển thị thông tin, cảnh báo và hỗ trợ quản lý

Hệ thống được thiết kế theo mô hình ba lớp: **Agent – Cloud Backend – Web Dashboard**, đảm bảo khả năng bảo vệ thời gian thực và quản lý tập trung.

