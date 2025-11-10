# 🧠 Student Academic Score Prediction → Advanced Feature Engineering Edition

## 📘 Project Overview

This project investigates how **lifestyle factors** — including *sleep, exercise, social media use, stress level, and study habits* influence students’ academic performance.  
Using a dataset of **5,000 students**, the study applies advanced **data preprocessing**, **outlier treatment**, **encoding**, and **feature scaling** techniques to ensure analytical accuracy and reliability.

## 🔧 Key Enhancements Over Previous Version

- **Hybrid Outlier Detection:** Combined **IQR** and **Z-Score** methods for robust outlier handling  
- **Multi-Strategy Missing Value Imputation:** Implemented **Iterative**, **KNN**, and **Random Sampling** techniques  
- **Categorical Encoding:** Applied **LabelEncoder** and **OrdinalEncoder** for better model interpretation  
- **Feature Scaling:** Used **StandardScaler** to standardize feature distributions and enhance model performance  

These improvements not only strengthened the dataset’s statistical validity but also increased the Linear Regression model’s R² score from 0.66 to 0.73, reflecting better predictive accuracy and feature consistency.

The project combines statistical validation with machine learning preprocessing to derive meaningful insights and also confirming that study habits, attendance, and stress management are the most influential factors in predicting academic success.

---

## 2. Dataset Overview
Dataset is same as one which I have used in my previous version.
**Total Records:** 5,000 students  
**Columns:** 11  

### Numerical Columns:
- Age  
- Study_Hours_Per_Day  
- Sleep_Hours  
- Physical_Activity_Hours  
- Screen_Time_Hours  
- Social_Activity_Score  
- Mental_Wellbeing_Score  
- Attendance_Rate  
- Academic_Score  

### Categorical Columns:
- Gender  
- Stress_Level  

---

## 3. Data Preprocessing and Cleaning

### ✅ Missing Value Handling
Applied multiple imputation strategies depending on data type and missing ratio:
| Column | Missing % | Imputation Technique |
|---------|------------|----------------------|
| Study_Hours_Per_Day | ~5% | **Iterative Imputer** |
| Sleep_Hours | ~6% | **Iterative Imputer** |
| Physical_Activity_Hours | ~4% | **KNN Imputer** |
| Social_Activity_Score | ~7% | **Random Sample Imputation** |
| Stress_Level | >5% | **Mode Imputation** |

### ✅ Categorical Standardization
- Cleaned inconsistent entries in **Gender** and **Stress_Level**  
- Converted all text entries to lowercase and replaced variants (e.g., “fmmale” → “female”)  

---

## 4. Outlier Handling

To ensure accurate statistical interpretation, multiple methods were applied across numerical variables:

| Column | Method | Description |
|---------|---------|-------------|
| Study_Hours_Per_Day | IQR | Negative values replaced with 0; capped at upper whisker |
| Sleep_Hours | IQR | Replaced extreme values with median |
| Physical_Activity_Hours | IQR | Handled outliers beyond 1.5×IQR |
| Screen_Time_Hours | Z-Score | Outliers beyond ±3σ replaced with median |
| Social_Activity_Score | Z-Score | Outliers beyond ±3σ replaced with median |
| Attendance_Rate | IQR | Values below 0 or above 100 corrected |

---

## 5. Feature Engineering

### 🧩 Encoding
- Converted categorical variables into numerical format for modeling:
  - **Gender:** Encoded using One_Hot Encoding (`male = 0`, `female = 1`)
  - **Stress_Level:** Encoded using LabelEncoder to preserve category order

### ⚙️ Feature Scaling
- Applied **StandardScaler** to normalize numerical features (mean = 0, std = 1)  
- Ensured consistent scale across predictors to improve model stability and regression performance

### 🔍 Data Split
- Used **train-test split (80-20)** for model preparation and future predictive tasks

---

## 7. Model Improvement and Accuracy
- Implemented **Linear Regression** to predict students’ `Academic_Score` based on lifestyle features.  
- After applying feature engineering techniques including **missing value imputation**, **outlier correction**, **encoding**, and **standard scaling** model accuracy improved significantly.  

| Model Version | MAE | MSE | RMSE | R² Score |
|----------------|-----|-----|------|-----------|
| Before Feature Engineering | 5.99 | 59.60 | 7.72 | **0.66** |
| After Feature Engineering | 4.82 | 48.13 | 6.93 | **0.73** |

✅ **Accuracy improved from 0.66 → 0.73**, indicating stronger predictive performance and reduced error after statistical and feature-based refinements.

---

## 8. Key Insights
- **Study hours** and **attendance rate** have the strongest positive correlation with academic performance.  
- **Stress Level** significantly impacts scores, lower stress correlates with higher performance.   
- **Screen time** and **physical activity** have limited direct correlation with scores.  
- Proper handling of **outliers, missing values, encoding, and scaling** improved data reliability and model accuracy.

---

## 9. Tools and Technologies
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scipy, scikit-learn  
- **Statistical Methods:** ANOVA, F-Test, Z-Score, IQR, Skewness 
- **Environment:** Google Colab / Jupyter Notebook  

---

## 10. Conclusion
This enhanced version integrates **advanced preprocessing and feature engineering techniques** including multiple imputation, hybrid outlier detection, categorical encoding, and standard scaling to deliver statistically valid and reliable insights.  
The refinements not only improved data quality but also **boosted model accuracy from 0.66 to 0.73**, demonstrating the impact of robust preprocessing on predictive analysis.  
Overall, the study confirms that **study habits**, **attendance**, and **stress management** are the most influential factors driving students’ academic performance.

---

### 👩‍💻 Author
**Noor Fatima**  
🎓 *Computer Science Student | 💡 Data Science Enthusiast*  
📍 *Pakistan*
