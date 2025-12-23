🌸 Flower Classification Project
📌 Giới thiệu
Đề tài Flower Classification tập trung vào bài toán phân loại hơn 100 loài hoa từ ảnh, sử dụng mô hình học sâu nhẹ MobileNet.
Mục tiêu của dự án là đánh giá hiệu quả của các chiến lược huấn luyện khác nhau khi không sử dụng trọng số pretrain, đặc biệt trong bối cảnh dữ liệu đa nguồn và mất cân bằng lớp.

📊 Dữ liệu (Dataset)
Dữ liệu được tổng hợp từ hai nguồn chính:
1. Hoa Việt Nam


Nguồn: hoavietnam.vn


Số lượng: Hơn 100 loài hoa


Đặc điểm:


Ảnh đa dạng về góc chụp, ánh sáng


Phù hợp với bối cảnh thực tế tại Việt Nam




2. Oxford Flowers 102


Bộ dữ liệu chuẩn Oxford Flowers 102


Số lượng: 102 loài hoa


Đặc điểm:


Ảnh chất lượng cao


Được gán nhãn rõ ràng, phổ biến trong nghiên cứu học máy




➡️ Tổng dataset được chuẩn hóa và chia thành tập train / validation / test.

🧠 Mô hình sử dụng


MobileNet (from scratch)


❌ Không sử dụng trọng số pretrain (ImageNet)


✅ Phù hợp cho thiết bị tài nguyên hạn chế


Kiến trúc CNN nhẹ, tốc độ huấn luyện nhanh



⚙️ Chiến lược huấn luyện
Dự án so sánh 4 chiến lược huấn luyện chính:
1️⃣ Không tăng cường dữ liệu


Huấn luyện trực tiếp trên dữ liệu gốc


Làm baseline để so sánh


2️⃣ Tăng cường dữ liệu (Data Augmentation)


Áp dụng các kỹ thuật:


Random rotation


Horizontal / vertical flip


Zoom, shift




Mục tiêu: tăng tính đa dạng dữ liệu, giảm overfitting


3️⃣ Tăng cường dữ liệu + Focal Loss


Sử dụng Focal Loss để:


Giảm ảnh hưởng của các lớp dễ


Tập trung học tốt hơn các lớp khó / ít mẫu




Phù hợp với dữ liệu mất cân bằng


4️⃣ Tăng cường dữ liệu + Focal Loss + Mixup


Kết hợp:


Data Augmentation


Focal Loss


Mixup




Mixup giúp:


Tăng tính tổng quát


Làm mượt ranh giới quyết định


Giảm overfitting





🧪 Mixup


Kỹ thuật trộn hai ảnh và nhãn tương ứng:
x = λx₁ + (1−λ)x₂
y = λy₁ + (1−λ)y₂



Giúp mô hình:


Học được biểu diễn mượt hơn


Chống nhiễu tốt hơn





📈 Đánh giá


Các chỉ số đánh giá:


Accuracy


Loss


Confusion Matrix




So sánh hiệu quả giữa các chiến lược huấn luyện



🚀 Kết luận


Data augmentation giúp cải thiện rõ rệt hiệu suất


Focal Loss đặc biệt hiệu quả với các lớp ít mẫu


Kết hợp Augmentation + Focal Loss + Mixup cho kết quả tổng quát tốt nhất


MobileNet từ scratch vẫn đạt hiệu quả khả quan khi có chiến lược huấn luyện phù hợp



🛠 Công nghệ sử dụng


Python


TensorFlow / Keras (hoặc PyTorch nếu bạn dùng)


OpenCV / Albumentations (augmentation)


NumPy, Matplotlib



📄 Giấy phép
Dự án phục vụ cho mục đích học tập và nghiên cứu.
