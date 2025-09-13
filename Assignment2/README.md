# Loan Amount Prediction using Machine Learning

## 📌 Assignment Overview
This Assignment focuses on predicting **Loan Sanction Amounts** using **Linear Regression** and other regression models. The work was completed as part of the **Machine Learning Algorithms Laboratory** (ICS1512) at **Sri Sivasubramaniya Nadar College of Engineering, Chennai**.

The assignment covers the **end-to-end machine learning workflow**, including data preprocessing, exploratory data analysis, feature engineering, model training, evaluation, and visualization.

---

## 🎯 Aim
To build and evaluate regression models for **loan sanction prediction**, incorporating:
- **K-Fold Cross Validation**
- **Performance metrics (MAE, MSE, RMSE, R²)**
- **Visualization techniques (Residual plots, Correlation Heatmaps, Actual vs Predicted plots, etc.)**

---

## 🛠️ Libraries Used
- **pandas** – Data manipulation and analysis  
- **numpy** – Numerical computations  
- **matplotlib** – Data visualization  
- **seaborn** – Statistical data visualization  
- **scikit-learn** – Model training, validation, and evaluation  

---

## 📂 Dataset
- Original dataset size: **30,000 rows × 24 columns**  
- After preprocessing (handling missing values & outliers): **29,660 rows × 24 columns**  

### Features
- Demographic features: *Gender, Age, Income, Income Stability*  
- Financial features: *Credit Score, Loan Amount Request, Property Price*  
- Loan history: *No. of Defaults, Active Credit Card, Dependents*  
- Property details: *Property Age, Property Type, Property Location*  

### Target
- **Loan Sanction Amount (USD)**

---

## 🔄 Data Preprocessing
1. **Handling Missing Values** – filled using mean/median/mode.  
2. **Outlier Treatment** – capped using percentile-based approach.  
3. **Encoding Categorical Variables** – Label Encoding applied.  
4. **Feature Scaling** – StandardScaler used for normalization.  

---

## 📊 Exploratory Data Analysis
- **Histograms & Distribution plots** to check feature distributions.  
- **Scatter plots** for Income, Credit Score vs Loan Amount.  
- **Correlation Heatmap** to study feature relationships.  
- **Boxplots** to identify and treat outliers.  

---

## 🧠 Models Implemented
- **Linear Regression (Baseline)**
- **Regularized Regression:** Ridge, Lasso, ElasticNet
- **Polynomial Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **AdaBoost Regressor**
- **Gradient Boosting Regressor**
- **XGBoost Regressor**
- **Support Vector Regressors (Linear, Polynomial, RBF, Sigmoid)**
- **K-Neighbors Regressor**

---

## 📈 Performance Metrics
Evaluation was performed using:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**
- **Adjusted R² Score**

### Cross-Validation (K=5)
- Linear Regression Average: **MAE = 18,891.93 | RMSE = 26,895.81 | R² = 0.62**

### Final Test Results (Best Models)
| Model                | MAE     | RMSE     | R²   |
|-----------------------|---------|----------|------|
| **Linear Regression** | 19,022  | 27,266   | 0.60 |
| **Decision Tree**     | 1,211   | 10,977   | 0.94 |
| **Random Forest**     | **928** | **9,599**| 0.95 |
| **Gradient Boosting** | 951     | 9,747    | 0.95 |
| **XGBoost**           | **808** | **8,826**| **0.96** |

---

## 📊 Visualizations
- Histogram / Distribution plots  
- Scatter plots  
- Correlation heatmap  
- Actual vs Predicted plots  
- Residual plots  
- Boxplots  
- Feature Coefficient bar plots  

---

## ✅ Key Learnings
- End-to-end workflow of a regression task: **Preprocessing → Training → Evaluation**  
- Importance of **data cleaning** (missing values, outliers)  
- How **cross-validation** strengthens model reliability  
- Performance trade-offs between **linear models and ensemble models**  
- Visual validation using **residuals and actual vs predicted plots**  

---

## 🚀 Conclusion
- Linear models provided a strong baseline, but ensemble methods like **Random Forest, Gradient Boosting, and XGBoost** significantly outperformed them.  
- **XGBoost Regressor** achieved the **best performance** with **MAE ≈ 808, RMSE ≈ 8,826, and R² ≈ 0.96**.  
- This shows ensemble learning techniques are more suitable for complex, non-linear datasets like loan prediction.  

---

## 📎 Author
- **Student Name:** Anusha K N 
- **Batch:** 2023–2028  
- **Course:** Machine Learning Algorithms Lab (ICS1512)  

---
