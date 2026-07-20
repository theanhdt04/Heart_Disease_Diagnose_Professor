# ❤️ Heart Disease Diagnose Professor

An interactive Machine Learning web application designed to evaluate and provide clinical-style risk feedback for heart disease based on patient physiological attributes. Built with **Streamlit**, this project demonstrates a robust, end-to-end data preparation workflow and inference deployment.

---

## 📌 Project Overview
Cardiovascular diseases are a leading cause of mortality globally. This project aims to build a reliable assistance system to assess heart disease risks using patient health metrics. 

As a **Data / Data Preprocessing Engineer**, my primary focus was establishing a clean, structured, and highly reproducible data preparation pipeline that serves as the solid foundation for downstream Machine Learning models.

---

## 👨‍💻 Role & Core Responsibilities

### 1. Data Engineering & Preprocessing
* **Source:** Heart Disease Dataset (Obtained from Kaggle / originally from UCI Machine Learning Repository).
* **Data Cleaning:** Handled missing values, formatted inconsistent data types, and filtered outliers using **Pandas** and **NumPy**.
* **Feature Scaling:** Implemented **`StandardScaler`** from Scikit-Learn to normalize continuous physiological features (e.g., blood pressure, cholesterol), ensuring distance-based and tree-based metrics operate seamlessly without magnitude bias.
* **Pipeline Replication:** Encapsulated preprocessing steps into modular operations to guarantee identical transformations for both training batches and real-time user inputs.

### 2. Exploratory Data Analysis (EDA)
* Investigated structural statistics and data distributions of 14 core clinical attributes.
* Analyzed correlation matrices to identify influential features and hidden patterns prior to the modeling stage.
* Documented visual patterns and insights within `EDA.ipynb`.

### 3. Model Wrapping & Deployment Assistance
* Assisted in formatting data matrices required by state-of-the-art gradient boosting algorithms (**CatBoost**, **XGBoost**, **LightGBM**).
* Managed model serialization, metadata versioning, and loading mechanics utilizing **Joblib**.
* Developed the interactive user dashboard using **Streamlit** to handle single-sample feature input and real-time risk evaluation.

---

## 🛠️ Tech Stack
* **Language:** Python 3.10+
* **Data Preprocessing & EDA:** Pandas, NumPy, Scikit-Learn
* **Machine Learning Baselines:** CatBoost, XGBoost, LightGBM
* **Model Serialization:** Joblib
* **Deployment & UI:** Streamlit

---

## 📂 Directory Structure

```text
Heart_Disease_Diagnose_Professor/
│
├── app.py                  # Main Streamlit web application
├── app_chon.py             # Alternative UI layout
├── EDA.ipynb               # Exploratory Data Analysis & visualization
├── modeling.ipynb          # Model training & baseline evaluation
├── train.csv               # Raw clinical dataset
├── train_processed.csv     # Cleaned & preprocessed dataset
├── requirements.txt        # Project dependencies
├── README.md               # Documentation
│
├── saved_models/           # Serialized models & assets
│   ├── cb_model.pkl
│   ├── xgb_model.pkl
│   ├── lgb_model.pkl
│   └── metadata.pkl
│
└── .gitignore
⚙️ Installation & Usage1. Clone the RepositoryBashgit clone [https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor.git](https://github.com/theanhdt04/Heart_Disease_Diagnose_Professor.git)
cd Heart_Disease_Diagnose_Professor
2. Set Up Virtual EnvironmentBash# Create environment
python -m venv .venv

# Activate environment (Windows PowerShell)
.venv\Scripts\Activate

# Activate environment (Windows CMD)
.venv\Scripts\activate.bat
3. Install DependenciesBashpip install -r requirements.txt
4. Run the ApplicationBashstreamlit run app.py
Once successfully launched, access the local dashboard at: http://localhost:8501📊 Development WorkflowPlaintext      [Raw Data Collection]
                │
                ▼
    [Data Preprocessing (Cleaning)]
                │
                ▼
   [Exploratory Data Analysis (EDA)]
                │
                ▼
    [Model Training & Evaluation]
                │
                ▼
     [Model Serialization (Joblib)]
                │
                ▼
    [Streamlit UI Core Deployment]
                │
                ▼
 [Real-time Medical Inference Feedback]
📦 Supported Model FrameworksModel BasePurpose / Core StrengthCatBoostOptimized for categorical features and robust tabular data performance.XGBoostHigh-performance, scalable gradient boosting framework.LightGBMHighly efficient, rapid training speed, and low memory usage.👤 AuthorNguyen The AnhBachelor of Information Technology - Hanoi University of Industry (HaUI)GitHub: theanhdt04
