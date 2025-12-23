# 🌸 Flower Classification Project

## 📌 Giới thiệu

Đề tài **Flower Classification** tập trung vào bài toán **phân loại hơn
100 loài hoa** từ ảnh, sử dụng mô hình học sâu nhẹ **MobileNet**.\
Mục tiêu của dự án là đánh giá hiệu quả của các **chiến lược huấn luyện
khác nhau** khi **không sử dụng trọng số pretrain**, đặc biệt trong bối
cảnh dữ liệu đa nguồn và mất cân bằng lớp.

------------------------------------------------------------------------

## 📊 Dữ liệu (Dataset)

Dữ liệu được tổng hợp từ **hai nguồn chính**:

### 1. Hoa Việt Nam

-   Nguồn: hoavietnam.vn\
-   Số lượng: Hơn 100 loài hoa\
-   Đặc điểm:
    -   Ảnh đa dạng về góc chụp, ánh sáng
    -   Phù hợp với bối cảnh thực tế tại Việt Nam

### 2. Oxford Flowers 102

-   Bộ dữ liệu chuẩn Oxford Flowers 102\
-   Số lượng: 102 loài hoa\
-   Đặc điểm:
    -   Ảnh chất lượng cao
    -   Gán nhãn rõ ràng, phổ biến trong nghiên cứu học máy

------------------------------------------------------------------------

## 🧠 Mô hình sử dụng

-   MobileNet (huấn luyện từ đầu -- from scratch)\
-   Không sử dụng trọng số pretrain ImageNet\
-   Kiến trúc CNN nhẹ, phù hợp cho thiết bị hạn chế tài nguyên

------------------------------------------------------------------------

## ⚙️ Chiến lược huấn luyện

Dự án so sánh 4 chiến lược huấn luyện:

1.  **Không tăng cường dữ liệu**\
2.  **Tăng cường dữ liệu (Data Augmentation)**\
3.  **Tăng cường dữ liệu + Focal Loss**\
4.  **Tăng cường dữ liệu + Focal Loss + Mixup**

------------------------------------------------------------------------

## 🧪 Mixup

Mixup là kỹ thuật trộn hai ảnh và nhãn tương ứng:

x = λx₁ + (1−λ)x₂\
y = λy₁ + (1−λ)y₂

Giúp mô hình tổng quát tốt hơn và giảm overfitting.

------------------------------------------------------------------------

## 📈 Đánh giá

-   Accuracy\
-   Loss\
-   Confusion Matrix

So sánh hiệu quả giữa các chiến lược huấn luyện.

------------------------------------------------------------------------

## 🚀 Kết luận

-   Data augmentation giúp cải thiện rõ rệt hiệu suất\
-   Focal Loss hiệu quả với dữ liệu mất cân bằng\
-   Kết hợp Augmentation + Focal Loss + Mixup cho kết quả tốt nhất\
-   MobileNet from scratch vẫn đạt hiệu quả khả quan nếu huấn luyện đúng
    cách

------------------------------------------------------------------------

## 🛠 Công nghệ sử dụng

-   Python\
-   TensorFlow / Keras\
-   NumPy, OpenCV

------------------------------------------------------------------------

## 📄 Giấy phép

Dự án phục vụ cho mục đích học tập và nghiên cứu.
