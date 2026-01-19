# ObserOne – Endpoint Detection & Response (EDR)

ObserOne là một hệ thống **giám sát & bảo mật máy tính theo thời gian thực**, sử dụng **phân tích hành vi và AI** để phát hiện tấn công, tự động phản ứng và hiển thị sự kiện ngay trên **Web Dashboard**.

Hệ thống được thiết kế theo mô hình **Agent – Cloud – Web**, phù hợp cho cá nhân, doanh nghiệp nhỏ đến môi trường enterprise.

---

## 🚀 Tính năng chính

### 🖥️ Giám sát Endpoint (Agent)
- Theo dõi **process**, **file**, **network**, **resource usage**
- Phân tích quan hệ **parent–child process**
- Thu thập hành vi hệ thống theo thời gian thực
- Hoạt động **offline**, không phụ thuộc cloud

---

### 🧠 Phân tích hành vi & AI
- Phát hiện bất thường dựa trên:
  - Rule-based (heuristic)
  - Behavioral analysis
  - Anomaly detection (AI/ML – ONNX)
- Không phụ thuộc signature truyền thống
- Phát hiện:
  - Malware
  - Ransomware
  - Backdoor / C2
  - Cryptominer
  - Zero-day behavior

---

### ⚡ Phản ứng tự động (Response)
Thực hiện **ngay tại máy bị tấn công**:
- Kill / suspend process độc hại
- Quarantine file
- Block IP / domain
- Cách ly mạng (Network Isolation)
- Ngăn lây lan sang máy khác

---

### ☁️ Cloud Backend
- Nhận log & alert từ agent
- Xử lý sự kiện bảo mật tập trung
- Lưu trữ dữ liệu, timeline tấn công
- Đồng bộ chính sách & cấu hình
- Không ảnh hưởng đến khả năng phản ứng real-time của agent

---

### 🌐 Web Dashboard
- Hiển thị **alert real-time**
- Danh sách endpoint đang hoạt động
- Timeline & phân tích sự cố
- Process tree & hành vi
- Thao tác phản ứng từ xa (Kill / Isolate / Block)
- Phân quyền người dùng (Admin / Analyst / Viewer)

---

## 🧩 Kiến trúc hệ thống

