# ❤️ Heart Disease Diagnose Professor

Ứng dụng web tương tác sử dụng Machine Learning để đánh giá và cung cấp phản hồi về nguy cơ mắc bệnh tim dựa trên các chỉ số sinh lý của bệnh nhân. Được xây dựng bằng **Streamlit**, dự án này minh họa một quy trình chuẩn hóa, khép kín từ tiền xử lý dữ liệu đến triển khai ứng dụng thực tế.

---

## 📌 Tổng quan dự án
Bệnh tim mạch là một trong những nguyên nhân gây tử vong hàng đầu trên toàn cầu. Dự án này nhằm mục đích xây dựng một hệ thống hỗ trợ đáng tin cậy để đánh giá nguy cơ mắc bệnh tim bằng cách sử dụng các chỉ số sức khỏe của bệnh nhân.

Với vai trò là một **Kỹ sư Xử lý dữ liệu (Data / Data Preprocessing Engineer)**, trọng tâm chính của tôi là thiết kế một quy trình chuẩn bị dữ liệu sạch, có cấu trúc tốt và có khả năng tái lặp cao để làm nền tảng vững chắc cho các mô hình Machine Learning ở phía sau.

---

## 👨‍💻 Vai trò & Trách nhiệm chính

### 1. Kỹ thuật dữ liệu & Tiền xử lý (Data Engineering & Preprocessing)
* **Nguồn dữ liệu:** Tập dữ liệu bệnh tim (Lấy từ Kaggle / gốc từ Kho lưu trữ học máy UCI).
* **Làm sạch dữ liệu:** Xử lý các giá trị thiếu, định dạng lại các kiểu dữ liệu không nhất quán và lọc bỏ các giá trị ngoại lai (outliers) bằng cách sử dụng **Pandas** và **NumPy**.
* **Chuẩn hóa đặc trưng (Feature Scaling):** Triển khai bộ công cụ **`StandardScaler`** từ Scikit-Learn để đưa các đặc trưng sinh lý liên tục (như huyết áp, cholesterol) về cùng một phân phối chuẩn, đảm bảo các thuật toán không bị sai lệch do chênh lệch biên độ dữ liệu.
* **Tái đóng gói quy trình:** Đóng gói các bước tiền xử lý thành các hàm mô-đun để đảm bảo dữ liệu khi người dùng nhập vào trên giao diện web sẽ được biến đổi hoàn toàn trùng khớp với dữ liệu lúc huấn luyện mô hình.

### 2. Phân tích dữ liệu khám phá (EDA)
* Nghiên cứu số liệu thống kê cấu trúc và phân phối dữ liệu của 14 thuộc tính lâm sàng cốt lõi.
* Phân tích ma trận tương quan để xác định các đặc trưng có ảnh hưởng lớn và các mẫu dữ liệu tiềm ẩn trước khi đưa vào bước huấn luyện.
* Tài liệu hóa các biểu đồ trực quan và thông tin chuyên sâu trong file `EDA.ipynb`.

### 3. Đóng gói mô hình & Hỗ trợ triển khai
* Hỗ trợ định dạng các ma trận dữ liệu đầu vào theo yêu cầu của các thuật toán Gradient Boosting tiên tiến nhất hiện nay (**CatBoost**, **XGBoost**, **LightGBM**).
* Quản lý việc lưu trữ mô hình (serialization), đồng bộ siêu dữ liệu (metadata) và cơ chế tải mô hình bằng **Joblib**.
* Phát triển giao diện bảng điều khiển trực quan bằng **Streamlit** để tiếp nhận các chỉ số sức khỏe do người dùng nhập vào và đưa ra kết quả dự đoán thời gian thực.

---

## 🛠️ Công nghệ sử dụng
* **Ngôn ngữ:** Python 3.10+
* **Tiền xử lý dữ liệu & EDA:** Pandas, NumPy, Scikit-Learn
* **Thuật toán Machine Learning:** CatBoost, XGBoost, LightGBM
* **Lưu trữ mô hình:** Joblib
* **Triển khai giao diện:** Streamlit

---

## 📂 Cấu trúc thư mục

```text
Heart_Disease_Diagnose_Professor/
│
├── app.py                  # Ứng dụng giao diện Web Streamlit chính
├── app_chon.py             # Giao diện phụ/bố cục thay thế
├── EDA.ipynb               # Phân tích khám phá dữ liệu & trực quan hóa
├── modeling.ipynb          # Huấn luyện mô hình & đánh giá các baseline
├── train.csv               # Tập dữ liệu lâm sàng gốc (raw)
├── train_processed.csv     # Tập dữ liệu sau khi đã làm sạch & tiền xử lý
├── requirements.txt        # Danh sách các thư viện phụ thuộc của dự án
├── README.md               # Tài liệu hướng dẫn dự án (File này)
│
├── saved_models/           # Thư mục lưu trữ mô hình đã huấn luyện
│   ├── cb_model.pkl
│   ├── xgb_model.pkl
│   ├── lgb_model.pkl
│   └── metadata.pkl
│
└── .gitignore
⚙️ Hướng dẫn cài đặt & Sử dụng1. Clone dự án về máy localBashgit clone [https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor.git](https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor.git)
cd Heart_Disease_Diagnose_Professor
2. Thiết lập môi trường ảoBash# Tạo môi trường ảo
python -m venv .venv

# Kích hoạt môi trường (Dành cho Windows PowerShell)
.venv\Scripts\Activate

# Kích hoạt môi trường (Dành cho Windows CMD)
.venv\Scripts\activate.bat
3. Cài đặt các thư viện cần thiếtBashpip install -r requirements.txt
4. Khởi chạy ứng dụngBashstreamlit run app.py
Sau khi ứng dụng khởi chạy thành công, bạn có thể truy cập giao diện tại đường dẫn: http://localhost:8501📊 Quy trình phát triển dự ánPlaintext      [Thu thập dữ liệu thô]
                │
                ▼
      [Tiền xử lý & Làm sạch]
                │
                ▼
    [Phân tích khám phá (EDA)]
                │
                ▼
     [Huấn luyện & Đánh giá]
                │
                ▼
     [Lưu trữ mô hình (Joblib)]
                │
                ▼
     [Triển khai Web Streamlit]
                │
                ▼
  [Dự đoán & Phản hồi thời gian thực]
