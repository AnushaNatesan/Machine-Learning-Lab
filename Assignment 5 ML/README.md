# 🧠 Perceptron vs Multilayer Perceptron (MLP)

## 📌 Assignment Overview
This assignment compares a **Single-Layer Perceptron (PLA)** and a **Multilayer Perceptron (MLP)** for classification tasks.  
Both models are trained on an **English handwritten character dataset** with **62 classes**, and their performance is evaluated using standard metrics.  

The experiment focuses on **hyperparameter tuning** for MLP, including:
- Activation functions  
- Optimizers  
- Learning rates  
- Batch sizes  
- Epochs  

---

## 🎯 Aim
To implement and compare the performance of:
- **Model A:** Single-Layer Perceptron Learning Algorithm (PLA)  
- **Model B:** Multilayer Perceptron (MLP) with hidden layers and nonlinear activations  

and to **systematically tune hyperparameters** to determine the best configuration.

---

## 🛠️ Libraries Used
- **pandas, numpy** – Data preprocessing  
- **matplotlib** – Visualization (training curves, confusion matrices)  
- **scikit-learn** – Metrics (accuracy, precision, recall, F1-score)  
- **Pillow (PIL)** – Image preprocessing  
- **tensorflow / keras** – MLP implementation and training  

---

## 📂 Dataset
- **Source:** English handwritten characters dataset (`english.csv` with image paths)  
- **Samples:** 3,410 images  
- **Classes:** 62 (A–Z, a–z, digits 0–9)  
- **Preprocessing:**  
  - Converted to grayscale  
  - Resized to **32×32**  
  - Normalized pixel values to [0,1]  
  - Labels encoded and one-hot encoded for MLP  

---

## 🔄 Models Implemented

### 🔹 Perceptron (PLA – One-vs-Rest)
- Implemented manually with stochastic gradient descent updates  
- Hyperparameters:  
  - Learning rate = **0.01**  
  - Epochs = **30**  
- **Performance:**  
  - Accuracy = **17.74%**  
  - Precision = 0.2708  
  - Recall = 0.1774  
  - F1-score = 0.1576  

---

### 🔹 Multilayer Perceptron (MLP)
- Architecture:  
  - Input layer (flattened 32×32 image = 1024 features)  
  - Dense(512, activation)  
  - Dense(256, activation)  
  - Dense(NUM_CLASSES, softmax)  
- Hyperparameter Tuning (grid search):  
  - Activations: `relu`, `tanh`  
  - Optimizers: `sgd`, `adam`  
  - Learning rates: 0.001, 0.01  
  - Batch sizes: 32, 64  
- **Best Config:**  
  - Activation = **ReLU**  
  - Optimizer = **Adam**  
  - Learning rate = **0.001**  
  - Batch size = **32**  
  - Epochs = **25**  
- **Performance:**  
  - Accuracy = **29.77%**  
  - Precision = 0.3207  
  - Recall = 0.2977  
  - F1-score = 0.2752  

---

## 📊 Results Summary
| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| PLA   | 0.1774   | 0.2708    | 0.1774 | 0.1576   |
| MLP   | 0.2977   | 0.3207    | 0.2977 | 0.2752   |

---

## 📈 Visualizations
- **Confusion Matrices** for PLA & MLP  
- **ROC Curves (micro & macro averages)** for MLP  
- **Training Curves (loss & accuracy per epoch)**  

---

## 🔍 Observations & Analysis
- **PLA underperforms** due to its linear decision boundaries → cannot capture nonlinear class separations.  
- **MLP performs better** by leveraging nonlinear activations and hidden layers.  
- **ReLU + Adam + lr=0.001** gave the most stable convergence.  
- **SGD** showed unstable convergence, often diverging.  
- More hidden layers ≠ always better; risk of overfitting and diminishing returns.  
- No strong overfitting was observed, but **dropout/regularization** could further stabilize deeper models.  

---

## ✅ Learning Outcomes
- Understood the **limitations of linear models (PLA)**.  
- Learned how **MLPs capture nonlinear decision boundaries**.  
- Explored the impact of **key hyperparameters** on model performance.  
- Applied **grid search** for hyperparameter tuning.  
- Gained experience in **evaluating models using multiple metrics**.  

---
---

