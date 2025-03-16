# NHẬN DIỆN KHUÔN MẶT ĐỘ CHÍNH XÁC CAO VỚI INSIGHT FACE VÀ MẠNG NƠ-RON SÂU

## 📌 Giới thiệu
Hệ thống nhận diện khuôn mặt sử dụng **InsightFace** và **mạng nơ-ron sâu** để xác định danh tính một cách chính xác. Dự án áp dụng cho các hệ thống điểm danh tự động, kiểm soát truy cập và bảo mật. Nhờ vào **ArcFace**, hệ thống đảm bảo nhận diện ngay cả khi có thay đổi về ánh sáng, góc chụp hoặc biểu cảm khuôn mặt.

## 🌟 Tính năng chính
- **Nhận diện khuôn mặt tự động** từ hình ảnh hoặc camera thời gian thực.
- **Trích xuất đặc trưng khuôn mặt (embedding)** bằng InsightFace.
- **Lưu trữ và quản lý dữ liệu nhận diện** trong MongoDB.
- **Giao diện trực quan** giúp theo dõi và quản lý dữ liệu điểm danh.
- **Tích hợp API Flask** để hỗ trợ nhận diện trên nền tảng web.

## 🏗️ Cấu trúc dự án
📦 **Project**
├── `data_preprocess.py`  # Tiền xử lý dữ liệu, trích xuất embeddings từ ảnh
├── `face_recognition.py`  # Nhận diện khuôn mặt thời gian thực từ camera
├── `face_db.pkl`  # Tệp lưu trữ embeddings của sinh viên
├── `requirements.txt`  # Danh sách thư viện cần cài đặt

## 🛠️ Công nghệ sử dụng
- **Python 3+**
- **InsightFace** (nhận diện khuôn mặt)
- **OpenCV** (xử lý ảnh, truy xuất camera)
- **MongoDB** (lưu trữ dữ liệu nhận diện)
- **Flask** (API nhận diện khuôn mặt qua web)
- **Tkinter** (Giao diện quản lý dữ liệu điểm danh)

## 📦 Cài đặt
1. **Clone repository**
   ```bash
   git clone https://github.com/your-repo/face-recognition-insightface.git
   cd face-recognition-insightface
   ```
2. **Cài đặt thư viện cần thiết**
   ```bash
   pip install -r requirements.txt
   ```
3. **Chuẩn bị dữ liệu nhận diện**
   - Tạo thư mục chứa ảnh khuôn mặt của sinh viên (`dataset/`).
   - Đặt tên ảnh theo định dạng `MaSV_HoTen_Lop.jpg`.
   - Chạy tiền xử lý dữ liệu:
     ```bash
     python data_preprocess.py
     ```

## 🎯 Hướng dẫn sử dụng
### 1️⃣ Chạy hệ thống nhận diện khuôn mặt
```bash
python face_recognition.py
```
- Hệ thống sẽ mở camera, phát hiện khuôn mặt và hiển thị kết quả.
- Kết quả nhận diện hiển thị trên màn hình với thông tin sinh viên.
- Nhấn `q` để thoát chương trình.

### 2️⃣ Tích hợp API nhận diện qua web
```bash
python api.py
```
- Chạy máy chủ Flask để nhận diện khuôn mặt từ ảnh tải lên.
- API có thể nhận yêu cầu và trả về danh tính người được nhận diện.

## 🖥️ Cấu hình khuyến nghị
- **CPU**: Intel Core i5 trở lên.
- **GPU**: NVIDIA GTX 1660 hoặc RTX 2060 (hỗ trợ CUDA).
- **RAM**: 8GB trở lên.
- **Hệ điều hành**: Ubuntu 20.04 LTS hoặc Windows 10.

## 📌 Cách hoạt động của hệ thống
1. **Tiền xử lý dữ liệu**: Phát hiện khuôn mặt trong ảnh và lưu đặc trưng vào `face_db.pkl`.
2. **Nhận diện khuôn mặt**: So sánh embedding của khuôn mặt mới với dữ liệu đã lưu.
3. **Xác định danh tính**: Nếu độ tương đồng cao hơn ngưỡng 0.5, hệ thống hiển thị kết quả.

## 🤝 Đóng góp
Dự án được phát triển bởi:
| Họ và Tên       | Vai trò |
|----------------|--------------------------------|
| Đinh Ngọc Chính | Xây dựng hệ thống nhận diện khuôn mặt |
| Phạm Văn Trà | Lưu trữ và quản lý dữ liệu |
| Trần Dương Anh | Phát triển giao diện API Flask |
| Trương Hữu Vinh | Kiểm thử và đánh giá hiệu suất |

Mọi đóng góp đều được hoan nghênh! Hãy tạo **Pull Request** hoặc **Issue** để cải thiện dự án.

## 📜 Giấy phép
Dự án này được phát hành theo giấy phép **MIT License**.

© 2025 Nhóm 1, CNTT16-03, Đại học Đại Nam.

