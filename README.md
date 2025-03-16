# Nhận diện khuôn mặt độ chính xác cao với InsightFace và mạng nơ-ron sâu

## 📝 Giới thiệu
Dự án này áp dụng **InsightFace** kết hợp với **mạng nơ-ron sâu** để nhận diện khuôn mặt với độ chính xác cao. Hệ thống có thể được sử dụng trong các ứng dụng điểm danh, kiểm soát truy cập và bảo mật.

## 🚀 Tính năng chính
- **Nhận diện khuôn mặt tự động** với độ chính xác cao.
- **Phản hồi trực quan** qua giao diện đồ họa hoặc API web.
- **Lưu trữ dữ liệu** nhận diện bằng MongoDB.
- **Hỗ trợ thời gian thực** với OpenCV và mô hình InsightFace.

## 🛠️ Công nghệ sử dụng
- **Python 3+**
- **InsightFace** (nhận diện khuôn mặt)
- **OpenCV** (xử lý ảnh, truy xuất camera)
- **MongoDB** (cơ sở dữ liệu)
- **Flask** (API web)
- **Tkinter** (giao diện quản lý)

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
3. **Cấu hình MongoDB**
   - Cài đặt MongoDB và đảm bảo chạy tại `mongodb://localhost:27017/`
   - Khôi phục dữ liệu nếu có:
     ```bash
     mongorestore --db FaceDB ./DataStore
     ```

## 🎯 Hướng dẫn sử dụng
### 1️⃣ Huấn luyện mô hình
```bash
python trainModel.py
```
### 2️⃣ Khởi động hệ thống nhận diện khuôn mặt
```bash
python nhanDien.py
```
### 3️⃣ Khởi động giao diện quản lý
```bash
python quanLy.py
```

## 📖 Ghi chú
- Đảm bảo camera hoạt động ổn định trước khi chạy chương trình.
- Nếu dùng GPU, bạn có thể tăng tốc xử lý bằng **PyTorch CUDA**.

## 🤝 Đóng góp
Mọi đóng góp đều được hoan nghênh! Hãy tạo **Pull Request** hoặc **Issue** để cải thiện dự án.

## 📜 Giấy phép
Dự án này được phát hành theo giấy phép **MIT License**.

© 2025 Nhóm 1, CNTT16-03, Đại học Đại Nam.

