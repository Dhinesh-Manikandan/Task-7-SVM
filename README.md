# Task-7-SVM

# 🧠 Task 7: Support Vector Machines (SVM)

## 🎯 Objective
The goal of this task is to apply Support Vector Machines (SVM) for binary classification using both linear and non-linear kernels, visualize decision boundaries, and evaluate model performance through cross-validation and hyperparameter tuning.

---

## 🛠️ Tools Used
- **Scikit-learn**: For SVM modeling, preprocessing, and evaluation.
- **NumPy**: For numerical operations.
- **Matplotlib**: For visualizing decision boundaries and results.

---

## 🧪 Dataset
The Breast Cancer Wisconsin dataset is used for this task. It is suitable for binary classification and includes features extracted from images of cell nuclei.

---

## 🔄 Workflow Overview

### 1. **Data Loading and Preparation**
- The dataset is loaded and split into training and testing sets.
- Features are **scaled** to ensure SVM performance is not affected by feature magnitude.

### 2. **Model Training**
Two SVM models are trained:
- **Linear Kernel SVM**: Best for linearly separable data.
- **RBF Kernel SVM**: Can handle non-linear data by mapping it into a higher-dimensional space.

### 3. **Visualization**
Since the dataset has many features, **Principal Component Analysis (PCA)** is applied to reduce dimensions to 2 for visualization purposes.
- This reduction allows plotting of decision boundaries, showing how SVM separates the classes in a 2D space.

### 4. **Hyperparameter Tuning**
A grid search is used to find the best combination of hyperparameters:
- **C (Regularization)**: Controls trade-off between margin size and misclassification.
- **Gamma**: Controls how far the influence of a single training example reaches (RBF kernel).
- **Kernel**: Specifies the type of kernel function (linear or RBF).

### 5. **Model Evaluation**
- Performance is measured using **cross-validation** to ensure the model generalizes well.
- Metrics like accuracy are averaged across folds to get a robust performance estimate.

---

## 🔍 Key Concepts

### 🧱 Support Vector
The data points that lie closest to the decision boundary. They define the position and orientation of the separating hyperplane.

### ⚙️ C Parameter
The regularization parameter:
- **Low C**: Allows wider margin but may tolerate misclassifications.
- **High C**: Aims to classify all training examples correctly by having a smaller margin.

### 📈 Gamma Parameter
Relevant for RBF kernels:
- **High gamma**: Leads to overfitting; the decision boundary is very tight.
- **Low gamma**: Makes the model smoother and more general.

### 🔗 Kernels in SVM
Functions that allow SVM to operate in higher-dimensional space:
- **Linear Kernel**: Suitable for linearly separable data.
- **RBF Kernel**: Handles non-linear relationships by applying Gaussian transformations.

---

## ✅ Benefits of SVM
- Effective in high-dimensional spaces.
- Works well when number of dimensions is greater than number of samples.
- Robust to overfitting, especially in high-dimension, low-sample size settings.

---



---

## 📌 Summary
SVMs are powerful classifiers that aim to find the optimal decision boundary between classes. By tuning parameters and choosing the right kernel, SVM can adapt to both linear and non-linear problems effectively. Visualization and cross-validation are essential to understand and validate the performance of the trained models.
