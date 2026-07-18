# ❤️ Heart Disease Diagnose Professor

Ứng dụng dự đoán nguy cơ mắc bệnh tim sử dụng **Machine Learning** với giao diện trực quan được xây dựng bằng **Streamlit**. Hệ thống hỗ trợ người dùng nhập các chỉ số sức khỏe và dự đoán nguy cơ mắc bệnh tim bằng các mô hình học máy đã được huấn luyện.

---

# 📌 Giới thiệu dự án

Bệnh tim mạch là một trong những nguyên nhân gây tử vong hàng đầu trên thế giới. Mục tiêu của dự án là xây dựng một hệ thống hỗ trợ dự đoán nguy cơ mắc bệnh tim dựa trên các đặc trưng sức khỏe của bệnh nhân, giúp minh họa quy trình xây dựng một bài toán Machine Learning từ xử lý dữ liệu đến triển khai ứng dụng.

Dự án bao gồm toàn bộ quy trình:

* Thu thập và tiền xử lý dữ liệu.
* Phân tích dữ liệu khám phá (Exploratory Data Analysis - EDA).
* Huấn luyện và đánh giá nhiều mô hình Machine Learning.
* Lưu mô hình đã huấn luyện.
* Xây dựng giao diện Web bằng Streamlit để dự đoán trực tiếp.

---

# 🚀 Demo Repository

**GitHub**

https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor

---

# 👨‍💻 Vai trò trong dự án

Trong dự án này, tôi đảm nhiệm toàn bộ quá trình phát triển, bao gồm:

### 1. Thu thập và xử lý dữ liệu

* Chuẩn bị tập dữ liệu dự đoán bệnh tim.
* Làm sạch dữ liệu.
* Xử lý dữ liệu thiếu.
* Chuyển đổi kiểu dữ liệu.
* Chuẩn hóa dữ liệu đầu vào.
* Xử lý đặc trưng bằng Pandas và NumPy.

---

### 2. Phân tích dữ liệu (EDA)

Sử dụng:

* Pandas
* NumPy

Thực hiện:

* Khám phá dữ liệu.
* Thống kê mô tả.
* Kiểm tra phân bố dữ liệu.
* Phân tích mối quan hệ giữa các đặc trưng.
* Chuẩn bị dữ liệu trước khi huấn luyện.

---

### 3. Xây dựng mô hình Machine Learning

Huấn luyện và đánh giá nhiều thuật toán:

* CatBoost
* XGBoost
* LightGBM

Các bước thực hiện:

* Huấn luyện mô hình.
* Đánh giá hiệu suất.
* So sánh kết quả giữa các mô hình.
* Lựa chọn mô hình phù hợp nhất để triển khai.

---

### 4. Lưu và quản lý mô hình

Sử dụng:

* Joblib

Bao gồm:

* Lưu mô hình đã huấn luyện.
* Quản lý metadata của mô hình.
* Tải mô hình phục vụ dự đoán.

---

### 5. Phát triển ứng dụng Web

Sử dụng:

* Streamlit

Chức năng:

* Nhập thông tin sức khỏe của bệnh nhân.
* Thực hiện dự đoán theo thời gian thực.
* Hiển thị kết quả trực quan.
* Kết nối trực tiếp với mô hình Machine Learning đã huấn luyện.

---

# 🛠️ Công nghệ sử dụng

## Programming Language

* Python 3.10+

## Machine Learning

* Scikit-learn
* CatBoost
* XGBoost
* LightGBM

## Data Processing

* Pandas
* NumPy

## Model Management

* Joblib

## Web Framework

* Streamlit

---

# 📂 Cấu trúc thư mục

```text
Heart_Disease_Diagnose_Professor/
│
├── app.py                  # Giao diện chính
├── app_chon.py             # Giao diện phụ
├── EDA.ipynb               # Phân tích dữ liệu
├── modeling.ipynb          # Huấn luyện mô hình
├── train.csv               # Dữ liệu gốc
├── train_processed.csv     # Dữ liệu sau xử lý
├── requirements.txt
├── README.md
│
├── saved_models/
│   ├── cb_model.pkl
│   ├── xgb_model.pkl
│   ├── lgb_model.pkl
│   └── metadata.pkl
│
└── .gitignore
```

---

# ⚙️ Hướng dẫn cài đặt

## Clone dự án

```bash
git clone https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor.git

cd Heart_Disease_Diagnose_Professor
```

---

## Tạo môi trường ảo

```bash
python -m venv .venv
```

---

## Kích hoạt môi trường

### Windows PowerShell

```powershell
.venv\Scripts\Activate
```

### Windows CMD

```cmd
.venv\Scripts\activate.bat
```

---

## Cài đặt thư viện

```bash
pip install -r requirements.txt
```

---

## Chạy ứng dụng

```bash
streamlit run app.py
```

Hoặc

```bash
python -m streamlit run app.py
```

Sau khi chạy thành công, truy cập:

```
http://localhost:8501
```

---

# 📊 Quy trình phát triển dự án

```
Thu thập dữ liệu
        │
        ▼
Tiền xử lý dữ liệu
        │
        ▼
Phân tích dữ liệu (EDA)
        │
        ▼
Huấn luyện mô hình
        │
        ▼
Đánh giá mô hình
        │
        ▼
Lưu mô hình (Joblib)
        │
        ▼
Triển khai Streamlit
        │
        ▼
Người dùng nhập dữ liệu
        │
        ▼
Dự đoán nguy cơ bệnh tim
```

---

# 📦 Các mô hình sử dụng

| Mô hình  | Mục đích                                  |
| -------- | ----------------------------------------- |
| CatBoost | Gradient Boosting tối ưu cho dữ liệu bảng |
| XGBoost  | Thuật toán Boosting hiệu quả và phổ biến  |
| LightGBM | Huấn luyện nhanh, tối ưu bộ nhớ           |

---

# 👨‍🎓 Tác giả

**Nguyễn Thế Anh**

Bachelor of Information Technology

Hanoi University of Industry (HaUI)

GitHub:

https://github.com/theanhdt04
