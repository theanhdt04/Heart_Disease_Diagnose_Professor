# Heart Disease Diagnose Professor

Ứng dụng dự đoán nguy cơ mắc bệnh tim bằng Machine Learning, xây dựng với **Python** và **Streamlit**.

## Công nghệ sử dụng

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

## Cấu trúc dự án

```
Heart_Disease_Diagnose_Professor-main/
│
├── app.py                  # Giao diện chính
├── app_chon.py             # Giao diện phụ (nếu có)
├── EDA.ipynb               # Phân tích dữ liệu
├── modeling.ipynb          # Huấn luyện mô hình
├── train.csv               # Dữ liệu gốc
├── train_processed.csv     # Dữ liệu sau xử lý
├── saved_models/           # Các mô hình đã huấn luyện
│   ├── cb_model.pkl
│   ├── xgb_model.pkl
│   ├── lgb_model.pkl
│   └── metadata.pkl
└── README.md
```

---

# Yêu cầu

- Windows 10/11
- Visual Studio Code
- Python 3.10 hoặc mới hơn
- Git (khuyến nghị)

---

# Hướng dẫn chạy dự án bằng Visual Studio Code

## Bước 1. Clone dự án

```bash
git clone https://github.com/<username>/<repository>.git
```

Hoặc tải file ZIP và giải nén.

---

## Bước 2. Mở dự án bằng VS Code

Chọn

```
File
    Open Folder...
```

Chọn thư mục

```
Heart_Disease_Diagnose_Professor-main
```

---

## Bước 3. Tạo môi trường ảo

Mở Terminal trong VS Code:

```
Terminal
    New Terminal
```

Chạy:

```bash
python -m venv .venv
```

---

## Bước 4. Kích hoạt môi trường ảo

PowerShell

```powershell
.venv\Scripts\Activate
```

CMD

```cmd
.venv\Scripts\activate.bat
```

Sau khi kích hoạt thành công sẽ xuất hiện

```
(.venv)
```

ở đầu Terminal.

---

## Bước 5. Cài đặt thư viện

Nếu dự án có file requirements.txt

```bash
pip install -r requirements.txt
```

Nếu chưa có thì cài thủ công

```bash
pip install streamlit
pip install numpy
pip install pandas
pip install scikit-learn
pip install joblib
pip install catboost
pip install xgboost
pip install lightgbm
```

Hoặc

```bash
pip install streamlit numpy pandas scikit-learn joblib catboost xgboost lightgbm
```

---

## Bước 6. Chạy ứng dụng

```bash
streamlit run app.py
```

Hoặc

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

## Thiếu thư viện

Ví dụ

```
ModuleNotFoundError
```

Khắc phục

```bash
pip install <tên_thư_viện>
```

Ví dụ

```bash
pip install joblib
pip install scikit-learn
pip install catboost
pip install xgboost
pip install lightgbm
```

---

## Không nhận lệnh streamlit

```bash
python -m streamlit run app.py
```

Hoặc

```bash
pip install streamlit
```

---

## Kiểm tra phiên bản Python

```bash
python --version
```

---

# Tác giả

Nguyễn Thế Anh
