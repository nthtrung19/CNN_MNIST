# CNN_MNIST
# 🧠 LeNet5 Classifier on MNIST

Huấn luyện mô hình CNN (LeNet5) trên bộ dữ liệu MNIST sử dụng PyTorch, với quy trình đầy đủ từ tiền xử lý, huấn luyện, đánh giá đến trực quan hóa kết quả.

---

## 🗂️ Dataset

- **Bộ dữ liệu**: [MNIST](http://yann.lecun.com/exdb/mnist/)
- **Kích thước ảnh**: 28x28 grayscale
- **Tỷ lệ chia tập**:
  - Train: 90%
  - Validation: 10%
  - Test: dùng tập test riêng từ MNIST

---

## 🔧 Mô hình LeNet5

Cấu trúc mô hình:

```python
Conv2d(1 → 6, kernel_size=5, padding='same')
AvgPool2d(kernel_size=2)
ReLU
Conv2d(6 → 16, kernel_size=5)
AvgPool2d(kernel_size=2)
ReLU
Flatten
Linear(16*5*5 → 120)
Linear(120 → 84)
Linear(84 → 10)
