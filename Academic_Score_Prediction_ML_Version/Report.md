# 🧠 Student Academic Score Prediction -> Machine Learning Model Benchmarking Edition

### 📘 Updated Project Overview  
This upgraded version extends the previous study by introducing **multiple machine learning models** and performing a complete comparison across **7 algorithms**:

- Linear Regression  
- Decision Tree  
- Random Forest  
- XGBoost  
- Gradient Boosting  
- Support Vector Regression (SVR)  
- Stacking Regressor (RF + GB + SVR → Ridge)

The goal is to determine **which model best predicts academic scores** after applying advanced preprocessing, outlier handling, encoding, and scaling techniques.

---

## 🔧 What’s New in This Version?

### ✔️ Multi-Model Benchmarking  
Evaluate how different ML algorithms perform on the **same cleaned dataset**.

### ✔️ Hyperparameter-Tuned Models  
Includes optimal configurations such as:

- Random Forest → `n_estimators = 200`  
- XGBoost, Gradient Boosting → `learning_rate = 0.05`  
- SVR → `C = 100`, `kernel = 'rbf'`

### ✔️ Stacking Regressor (Ensemble)
A layered architecture:  
**Random Forest + Gradient Boosting + SVR → Ridge Regressor** (meta model)

### ✔️ Performance Comparison Visualization  
A final bar chart comparing **RMSE** and **R²** for all 7 models.

---

## 📊 Dataset Overview

- Same dataset as previous version  
- **5,000 students**, **11 features**  
- The same cleaned, imputed, encoded, and scaled dataset is used for all models to ensure fairness

---

## 🧼 Preprocessing Pipeline

| Step | Techniques Used |
|------|----------------|
| Missing Value Handling | Iterative Imputer, KNN, Random Sample |
| Outlier Handling | IQR + Z-score hybrid |
| Encoding | One-Hot Encoding (Gender), Label Encoding (Stress) |
| Scaling | StandardScaler |
| Train/Test Split | 80% train / 20% test |

---

## 🚀 ML Models and Results

| Model | MAE | MSE | RMSE | R² | Train R² | Test R² |
|-------|------|-------|--------|--------|----------|-----------|
| Linear Regression | 5.434 | 47.43 | 6.887 | 0.729 | 0.720 | 0.729 |
| Decision Tree | 8.136 | 106.70 | 10.33 | 0.391 | 1.000 | 0.391 |
| Random Forest | 5.587 | 50.96 | 7.139 | 0.709 | 0.961 | 0.709 |
| XGBoost | 5.653 | 51.57 | 7.181 | 0.706 | 0.850 | 0.706 |
| Gradient Boosting | 5.641 | 51.43 | 7.172 | 0.706 | 0.857 | 0.706 |
| SVR | 6.266 | 62.24 | 7.890 | 0.645 | 0.819 | 0.645 |
| Stacking Regressor | 5.534 | 49.98 | 7.07 | 0.715 | 0.913 | 0.715 |

---

## 🏆 Key Findings

### 🔹 Best Performers  

| Metric | Best Model |
|--------|--------------|
| Lowest MAE | **Stacking Regressor** |
| Lowest MSE | **Linear Regression** |
| Highest Test R² | **Linear Regression (0.729)** |
| Best Ensemble | **Stacking Regressor (0.715)** |

---

## 🔍 Why Linear Regression Outperformed?

- Dataset relationships are **mostly linear**  
- After encoding & scaling, LR becomes highly stable  
- Complex models like RF & DT show signs of **overfitting**

---

## 🔍 Why Stacking Regressor Performed Well?

- Combines predictions from diverse models  
- Ridge meta-model reduces bias  
- Balances variance (trees) + non-linearity (SVR)  

---

## 🔎 Comparison with Previous Version

| Area | Previous Version | Current Version |
|-------|------------------|-------------------------|
| Models Used | Linear Regression only | 7 ML Models |
| Evaluation | Basic | Full Benchmark |
| Best Model | LR (R² = 0.73) | LR (0.73) + Stacking (0.715) |
| New Finding | Study habits + attendance strongest predictors | Linear patterns dominate; ensemble improves stability |
| Visual Output | Correlation + LR results | Complete multi-model comparison graph |

---

## 🎯 Final Conclusion

This upgraded version provides a **complete performance comparison** of multiple ML models on the same dataset.

- **Linear Regression remains the best performer**, likely due to the linear nature of the data.  
- **Stacking Regressor** offers a strong balanced approach by combining trees and SVR.  
- Advanced models (RF, XGBoost, GB) perform well but may overfit.  

This study highlights:

- Which models generalize best  
- Which models overfit  
- How preprocessing impacts each algorithm  
- How ensembles improve prediction stability  

---

## 👩‍💻 Author

**Noor Fatima**  
🎓 Computer Science Student  
💡 Data Science & ML Enthusiast  
📍 Pakistan  

---

