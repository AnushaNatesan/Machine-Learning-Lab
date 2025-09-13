# 🌳 Ensemble Prediction & Decision Tree Model Evaluation

## 📌 Assignment Overview
This Assignment explores the effectiveness of **Decision Trees** and **Ensemble Learning methods** for classification using the **Breast Cancer Wisconsin Dataset**.  
The models include:
- **Decision Tree**
- **AdaBoost**
- **Gradient Boosting**
- **XGBoost**
- **Random Forest**
- **Stacked Ensemble (SVM + Naïve Bayes + Decision Tree, with Logistic Regression as meta-learner)**

The models were tuned using **GridSearchCV** and evaluated through **5-Fold Cross-Validation**.

---

## 🎯 Aim
To build and evaluate individual and ensemble classifiers, and compare their performance using cross-validation and hyperparameter tuning.

---

## 🛠️ Libraries Used
- **numpy, pandas** – Data handling  
- **matplotlib, seaborn** – Visualization  
- **scikit-learn** – Decision Tree, AdaBoost, Gradient Boosting, Random Forest, evaluation metrics  
- **xgboost** – XGBoost classifier  

---

## 📂 Dataset
- **Dataset:** Breast Cancer Wisconsin (from `sklearn.datasets`)  
- **Features:** 30 numerical features (e.g., radius, texture, smoothness)  
- **Target:** Binary classification (*Malignant = 0, Benign = 1*)  
- **Preprocessing:** Standardization using `StandardScaler`  

---

## 🔄 Models & Hyperparameter Tuning
- **Decision Tree**  
  - Params: `criterion = entropy, max_depth = 7`  
  - Accuracy: **91.23%**

- **AdaBoost**  
  - Params: `n_estimators = 100, learning_rate = 1`  
  - Accuracy: **95.61%**

- **Gradient Boosting**  
  - Params: `n_estimators = 50, learning_rate = 0.5, max_depth = 3`  
  - Accuracy: **95.61%**

- **XGBoost**  
  - Params: `n_estimators = 100, learning_rate = 0.1, max_depth = 3, gamma = 0`  
  - Accuracy: **94.74%**

- **Random Forest**  
  - Params: `n_estimators = 50, criterion = entropy, max_depth = None`  
  - Accuracy: **95.61%**

- **Stacked Ensemble**  
  - Base models: SVM, Naïve Bayes, Decision Tree  
  - Meta-learner: Logistic Regression  
  - Accuracy: **97.37%** ✅ (Best performer)  

---

## 📊 Results

### Classification Reports (Summary)
| Model            | Accuracy | F1 Score |
|------------------|----------|----------|
| Decision Tree    | 0.9123   | 0.9275   |
| AdaBoost         | 0.9561   | 0.9660   |
| Gradient Boosting| 0.9561   | 0.9660   |
| XGBoost          | 0.9474   | 0.9589   |
| Random Forest    | 0.9561   | 0.9655   |
| Stacked Ensemble | **0.9737** | **0.9793** |

---

### Cross-Validation (5-Fold Average Accuracies)
| Model            | CV Accuracy |
|------------------|-------------|
| Decision Tree    | 0.9367 |
| AdaBoost         | **0.9772** |
| Gradient Boosting| 0.9580 |
| XGBoost          | 0.9684 |
| Random Forest    | 0.9666 |
| Stacked Ensemble | 0.9596 |

---

## 📈 Visualizations
- **Confusion Matrices** for each model  
- **ROC Curves** with AUC comparison  
- **Cross-validation performance plots**  

---

## ✅ Key Insights
- **Ensembles significantly outperform standalone Decision Trees**.  
- **Stacked Ensemble** gave the **best test accuracy (97.37%)** and F1-score (97.93%).  
- **AdaBoost** achieved the **best CV accuracy (97.72%)**, showing strong robustness.  
- **Random Forest & XGBoost** provided stable, generalizable performance.  
- **Decision Tree alone (91.23%)** was clearly weaker compared to ensemble methods.  

---

## 🚀 Conclusion
- Ensemble methods (especially **Stacking** and **AdaBoost**) are highly effective for cancer classification tasks.  
- **Stacked Ensemble Model** provided the best overall generalization on test data.  
- This experiment reinforces the value of **model combination** for boosting predictive performance.  

---

## 📎 Author
- **Name:** Anusha K N  
- **Roll No:** 3122237001005  
- **Batch:** 2023–2028  
- **Course:** Machine Learning Algorithms Lab (ICS1512)  

---

