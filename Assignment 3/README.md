# 📧 Email Spam vs Ham Classification

## 📌 Assignment Overview
This assignment focuses on **classifying emails as Spam or Ham** using three supervised machine learning algorithms:
- **Naïve Bayes (GaussianNB, BernoulliNB)**
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machines (SVM with multiple kernels)**

The models are trained, validated, and compared based on **accuracy, precision, recall, F1-score, and ROC curves**. Additionally, **K-Fold Cross Validation** is used to ensure robust evaluation.

---

## 🎯 Aim
To classify emails as spam or ham using Naïve Bayes, KNN, and SVM, and evaluate their performance with multiple metrics and cross-validation.

---

## 🛠️ Libraries Used
- **pandas** – Data manipulation and preprocessing  
- **numpy** – Numerical operations  
- **matplotlib** – Visualization of confusion matrices and ROC curves  
- **seaborn** – Enhanced data visualization  
- **scikit-learn** – Model training, evaluation, and cross-validation  
- **os** – File handling and dataset access  

---

## 🧑‍💻 Models Implemented

### 1. Naïve Bayes
- Implemented **GaussianNB** and **BernoulliNB**  
- Evaluated using confusion matrices and ROC curves  
- Best performance: **BernoulliNB (Accuracy ≈ 90.1%, F1 ≈ 0.87)**

---

### 2. K-Nearest Neighbors (KNN)
- Tested with **k = 1, 3, 5, 7**  
- Algorithms used: **auto, KDTree, BallTree**  
- Best performance: **k = 7 (Accuracy ≈ 90.8%, F1 ≈ 0.881)**  

---

### 3. Support Vector Machines (SVM)
- Implemented with **Linear, Polynomial, RBF, and Sigmoid kernels**  
- Best performance: **Linear Kernel (Accuracy ≈ 93.1%, F1 ≈ 0.911)**  

---

## 📊 Results & Comparison

### Naïve Bayes Performance
| Variant       | Accuracy | Precision | Recall | F1-Score |
|---------------|----------|-----------|--------|----------|
| GaussianNB    | 0.833    | 0.715     | 0.959  | 0.819    |
| BernoulliNB   | 0.901    | 0.902     | 0.840  | 0.870    |

---

### KNN Performance
| k | Accuracy | Precision | Recall | F1-Score |
|---|----------|-----------|--------|----------|
| 1 | 0.898    | 0.877     | 0.862  | 0.869    |
| 3 | 0.901    | 0.882     | 0.865  | 0.873    |
| 5 | 0.906    | 0.888     | 0.871  | 0.879    |
| 7 | **0.908**| **0.895** | 0.868  | **0.881**|

---

### SVM Performance
| Kernel      | Accuracy | F1-Score |
|-------------|----------|----------|
| Linear      | **0.931**| **0.911**|
| Polynomial  | 0.780    | 0.622    |
| RBF         | 0.927    | 0.906    |
| Sigmoid     | 0.884    | 0.852    |

---

### Cross-Validation (K=5)
| Fold | Naïve Bayes | KNN   | SVM   |
|------|-------------|-------|-------|
| 1    | 0.913       | 0.901 | 0.934 |
| 2    | 0.912       | 0.902 | 0.934 |
| 3    | 0.915       | 0.921 | 0.900 |
| 4    | 0.930       | 0.918 | 0.938 |
| 5    | 0.818       | 0.788 | 0.830 |
| **Avg** | **0.898**   | **0.884** | **0.904** |

---

## 📈 Visualizations
- **Confusion Matrices** for all models  
- **ROC Curves** with AUC scores  
- **Comparative bar charts** for Accuracy, Precision, Recall, and F1  

---

## ✅ Key Learnings
- **Naïve Bayes** works well for text classification due to probabilistic assumptions.  
- **KNN** shows competitive accuracy but is slower with larger datasets.  
- **SVM (Linear kernel)** outperformed others, achieving the highest classification accuracy.  
- **Cross-validation** confirmed SVM as the most robust model overall.  

---

## 🚀 Conclusion
- **Best Model:** Support Vector Machine (Linear Kernel)  
- Achieved **93.1% accuracy and 0.911 F1-score**.  
- The project highlights the importance of testing multiple classifiers and validating with cross-validation to avoid overfitting.  

---

## 📎 Author
- **Student Name:** Anusha K N  
- **Batch:** 2023–2028  
- **Course:** Machine Learning Algorithms Lab (ICS1512)  

---

