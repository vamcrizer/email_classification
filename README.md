# Phân Loại Email Spam

## Giới Thiệu
Dự án này thực hiện việc phân loại email thành hai loại: **Spam** và **Không Spam**. Xử lý ngôn ngữ tự nhiên (NLP) bằng thư viện nltk để phân tích nội dung email, dự án này ứng dụng mô hình **Passive Aggressive Classifier** nhằm huấn luyện và dự đoán các email có phải là spam hay không.

Dataset: https://www.kaggle.com/datasets/ashfakyeafi/spam-email-classification

## Mục Tiêu
- Tiền xử lý văn bản email thông qua NLP.
- Sử dụng mô hình **Passive Aggressive Classifier (PAC)** để phân loại email thành spam và không spam.
- Đánh giá hiệu suất mô hình thông qua các chỉ số đánh giá phổ biến như độ chính xác, độ nhạy, độ đặc hiệu.

## Các Bước Thực Hiện

### 1. Tiền Xử Lý Dữ Liệu
Dữ liệu email ban đầu cần phải được làm sạch và chuyển đổi về dạng có thể xử lý bởi các mô hình máy học. Các bước tiền xử lý chính bao gồm:
- **Loại bỏ ký tự đặc biệt**: Xóa bỏ các ký tự không cần thiết như dấu câu, số.
- **Chuyển đổi về dạng chữ thường**: Để giảm thiểu số lượng từ.
- **Loại bỏ từ dừng (stop words)**: Loại bỏ các từ phổ biến nhưng không mang nhiều ý nghĩa (như "và", "nhưng").
- **Stemming/Lemmatization**: Chuyển đổi từ về dạng gốc.

### 2. Chuyển Đổi Văn Bản Thành Vector (NLP)
Sau khi tiền xử lý, văn bản cần được chuyển đổi thành dạng vector bằng CountVectorizer số để đưa vào mô hình PAC.

### 3. Mô Hình Phân Loại PAC
- **PAC (Passive Aggressive Classifier)** là một thuật toán học máy tuyến tính phù hợp với các bài toán phân loại nhị phân. Nhất là những bài toán phân loại liên quan đến ngôn ngữ tự nhiên, văn bản, ngữ liệu,..

### 4. Đánh Giá Mô Hình
Hiệu suất mô hình sẽ được đánh giá bằng các chỉ số sau:
- **F1-Score**: Sự cân bằng giữa độ nhạy và độ đặc hiệu.
- **ROC-AUC**: Sử dụng diện tích dưới đường cong để đánh giá mô hình
- **K-Folds-CV**: Sử dụng K-Folds Crossvalidation để kiểm tra mô hình có overfit hay không

### 5. Nhưng thư viện cần thiết
```bash
pip install numpy pandas scikit-learn nltk
```

## Lưu ý
Đây chỉ là file notebook để tham khảo
