# ❤️ Heart Disease Diagnose Professor

Ứng dụng dự đoán nguy cơ mắc bệnh tim sử dụng Machine Learning với giao diện được xây dựng bằng **Streamlit**. Dự án sử dụng nhiều mô hình học máy như **CatBoost**, **XGBoost** và **LightGBM** để hỗ trợ dự đoán dựa trên các chỉ số sức khỏe của bệnh nhân.

## Demo Repository

GitHub: https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor

---

# Công nghệ sử dụng

- Python 3.10+
- Streamlit
- Scikit-learn
- CatBoost
- XGBoost
- LightGBM
- Pandas
- NumPy
- Joblib

---

# Cấu trúc thư mục

```
Heart_Disease_Diagnose_Professor/
│
├── app.py                  # Giao diện chính
├── app_chon.py             # Giao diện phụ
├── EDA.ipynb               # Phân tích dữ liệu
├── modeling.ipynb          # Huấn luyện mô hình
├── train.csv               # Dữ liệu gốc
├── train_processed.csv     # Dữ liệu sau xử lý
├── requirements.txt        # Danh sách thư viện
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

# Yêu cầu

Trước khi chạy dự án, cần cài đặt:

- Visual Studio Code
- Python 3.10 hoặc mới hơn
- Git

Kiểm tra phiên bản Python:

```bash
python --version
```

---

# Hướng dẫn chạy dự án bằng Visual Studio Code

## Bước 1. Clone dự án

```bash
git clone https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor.git
```

Di chuyển vào thư mục dự án:

```bash
cd Heart_Disease_Diagnose_Professor
```

---

## Bước 2. Mở dự án bằng VS Code

Mở Terminal và chạy:

```bash
code .
```

Hoặc mở VS Code → **File → Open Folder...** và chọn thư mục dự án.

---

## Bước 3. Tạo môi trường ảo

Mở Terminal trong VS Code:

```
Terminal → New Terminal
```

Tạo môi trường ảo:

```bash
python -m venv .venv
```

---

## Bước 4. Kích hoạt môi trường ảo

### PowerShell

```powershell
.venv\Scripts\Activate
```

### Command Prompt (CMD)

```cmd
.venv\Scripts\activate.bat
```

Sau khi kích hoạt thành công sẽ hiển thị:

```
(.venv)
```

---

## Bước 5. Cài đặt các thư viện

```bash
pip install -r requirements.txt
```

Nếu gặp lỗi, có thể nâng cấp pip trước:

```bash
python -m pip install --upgrade pip
```

Sau đó cài lại:

```bash
pip install -r requirements.txt
```

---

## Bước 6. Chạy ứng dụng

```bash
streamlit run app.py
```

Hoặc:

```bash
python -m streamlit run app.py
```

---

## Bước 7. Truy cập ứng dụng

Sau khi chạy thành công, Terminal sẽ hiển thị:

```
Local URL: http://localhost:8501
```

Mở trình duyệt và truy cập:

```
http://localhost:8501
```

---

# Các lỗi thường gặp

## 1. Thiếu thư viện

Ví dụ:

```
ModuleNotFoundError: No module named 'joblib'
```

Khắc phục:

```bash
pip install joblib
```

---

Ví dụ:

```
ModuleNotFoundError: No module named 'catboost'
```

Khắc phục:

```bash
pip install catboost
```

---

Ví dụ:

```
ModuleNotFoundError: No module named 'sklearn'
```

Khắc phục:

```bash
pip install scikit-learn
```

---

## 2. Không nhận lệnh Streamlit

```bash
python -m streamlit run app.py
```

Nếu chưa cài Streamlit:

```bash
pip install streamlit
```

---

## 3. Cập nhật toàn bộ thư viện

```bash
pip install -r requirements.txt
```

---

# Tác giả

**Nguyễn Thế Anh**

Sinh viên Trường Đại học Công nghiệp Hà Nội (HaUI)

GitHub: https://github.com/theanhdt04
