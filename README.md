# 🎓 Student Academic Score Prediction — Complete Project Repository  
### 📊 Feature Engineering | 🧮 Statistical Analysis | 🤖 Machine Learning | 🧠 Ensemble Learning

Welcome! 👋  
This repository contains **multiple versions** of a complete end-to-end project on **Student Academic Score Prediction**.  
Each version represents a different stage of the project from basic statistical exploration to advanced machine learning and ensemble modeling.

This structure allows learners, researchers, and recruiters to easily understand how the project evolved across:

- 📘 Statistical Analysis  
- 🛠️ Feature Engineering  
- 🤖 Machine Learning Models  
- 🧠 Ensemble & Stacking Regressor Models  

---

## 📁 Repository Structure

Academic-Score-Prediction/

├── Students_Academic_Score_Analysis/

│ ├── Academic _Score_EDA.ipynb

│ ├── students_lifestyle_5000.csv #dataset

│ └── README.md

│

├── Academic_Score_Prediction_FeatureEngineering_Version/

│ ├── Academic_Score_FeatureEngineering_Improvements.ipynb

│ └── README.md

│

├── Academic_Score_Prediction_Statistical_Version/

│ ├── Academic _Score_Statists.ipynb

│ └── README.md

|

├── Academic_Score_Prediction_ML_Version/

│ ├── Academic_Score_ML_Comparison.ipynb

│ └── README.md

└── README.md




Each folder includes:

✔️ A dedicated Jupyter Notebook (`.ipynb`)  
✔️ A clear README / report documenting the analysis  
✔️ Visualizations, preprocessing steps, and final results  

---

## 🔍 Version Overview

### 1️⃣ Statistical Analysis Version  
**Focus:** Understanding the data through pure statistical exploration.

Includes:

- Histograms, KDE plots, boxplots  
- Correlation heatmaps  
- Distribution analysis  
- Insights on relationships between study hours, attendance, stress, and academic performance  

No machine learning is involved — purely EDA.

---

### 2️⃣ Feature Engineering Version  
**Focus:** Preparing data for machine learning.

Includes:

- Missing value handling  
  - Iterative Imputer  
  - KNN Imputer  
  - Random Sample Imputation  
- Outlier removal using **IQR + Z-score hybrid**  
- Encoding techniques  
  - One-Hot Encoding  
  - Label Encoding  
- Feature scaling using StandardScaler  
- Feature selection and transformations  
- Creation of a **preprocessed dataset** for ML models  

All steps are explainable and reproducible.

---

### 3️⃣ Machine Learning Version (Advanced ML Benchmarking)  
**Focus:** Comparing multiple ML algorithms on the processed dataset.

Models included:

- Linear Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- XGBoost  
- Support Vector Regression (SVR)  
- Stacking Regressor (RF + GB + SVR → Ridge)

Outputs include:

- MAE, MSE, RMSE  
- Train vs Test R²  
- Overfitting & underfitting analysis  
- Final model comparison bar chart  
- Full documented analysis  

---
## 🧩 Dataset Details

**File name:** `students_lifestyle_5000.csv`  
**Source:** Generated using ChatGPT for educational and analytical purposes

### Overview

| Property | Details |
|-----------|----------|
| **Rows** | 5,000 |
| **Columns** | Mixed numerical and categorical variables |
| **Imperfections** | Missing values (~6%), typos, inconsistent labels, outliers, invalid values, duplicates |

**Intentional Data Imperfections:**
- Missing values (~6% across several columns)
- Typos and inconsistent categorical labels (e.g., `femmale`, `fmale`)
- Lowercase/variant entries in `Stress_Level`
- Duplicate `Student_ID`s
- Outliers in study/sleep/screen time
- Invalid values (e.g., attendance > 100%)

### Column Descriptions

| Column Name | Type | Description |
|--------------|------|-------------|
| Age | Numeric | Age of the student |
| Gender | Categorical | Student gender |
| Study_Hours_Per_Day | Numeric | Average hours spent studying daily |
| Sleep_Hours | Numeric | Average sleep hours per day |
| Physical_Activity_Hours | Numeric | Daily exercise hours |
| Screen_Time_Hours | Numeric | Daily screen/social media time |
| Social_Activity_Score | Numeric | Social interaction frequency score |
| Mental_Wellbeing_Score | Numeric | Overall mental wellness score |
| Attendance_Rate | Numeric | Class attendance percentage |
| Stress_Level | Categorical | Low / Medium / High |
| Academic_Score | Numeric | Final academic performance score |

---


## ▶️ How to Run the Project

### **Option 1: Google Colab (Recommended)**  
All notebooks are fully compatible with Google Colab.

- Open any folder  
- Click on the `.ipynb` file  
- Select **"Open in Colab"**  
- Run all cells — no setup required  

### **Option 2: Local Setup (Jupyter Notebook)**  

Install dependencies:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn xgboost
```


## 🏆 What You Will Learn

This repository will help you understand:

- How to perform **professional statistical analysis**
- How to **clean, transform, and preprocess** real-world data
- How to **benchmark multiple machine learning models** fairly
- How **ensemble learning (stacking)** improves predictive performance
- How to **document a complete Data Science / ML project** for GitHub & portfolios

### Perfect For:

✔️ Students  
✔️ ML & Data Science beginners  
✔️ Recruiters assessing technical depth  
✔️ Anyone learning end-to-end **ML pipelines**  

---

## 👩‍💻 Author

**Noor Fatima**  
🎓 BS Computer Science  
💡 Data Science & Machine Learning Enthusiast  
📍 Pakistan  

---

## ⭐ If You Find This Helpful

Please consider giving the repository a **star ⭐ on GitHub**. It truly motivates and supports my work!


