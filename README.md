# 🌸 Iris Flower Classification — CodeAlpha Task 1

An end-to-end Machine Learning project developed as part of the **CodeAlpha Data Science Internship**. The goal of this task is to classify Iris flowers into three distinct species (*Iris-setosa*, *Iris-versicolor*, *Iris-virginica*) based on physical measurements of their sepals and petals.

---

## 📌 Project Overview
- **Domain:** Data Science / Machine Learning
- **Task:** Multiclass Classification
- **Dataset:** Iris Flower Dataset (150 samples, 4 features)
- **Algorithm:** Random Forest Classifier (`sklearn`)
- **Model Accuracy:** 90.00%

---

## 📊 Features & Target
- **Input Features ($X$):**
  - `SepalLengthCm`: Sepal length in centimeters
  - `SepalWidthCm`: Sepal width in centimeters
  - `PetalLengthCm`: Petal length in centimeters
  - `PetalWidthCm`: Petal width in centimeters
- **Target Variable ($y$):**
  - `Species`: Iris-setosa, Iris-versicolor, Iris-virginica

---

## ⚙️ Workflow & Implementation
1. **Data Preprocessing & EDA:**
   - Loaded and inspected dataset structure.
   - Removed non-predictive identifiers (`Id` column).
   - Checked for missing values.
2. **Train-Test Split:**
   - Split ratio: 80% Training (120 samples) / 20% Testing (30 samples).
   - Stratified split to preserve class distribution across folds.
3. **Model Training:**
   - Trained an ensemble `RandomForestClassifier` with 100 decision trees.
4. **Evaluation:**
   - Assessed model performance using Accuracy, Classification Report (Precision, Recall, F1-Score), and Confusion Matrix.
5. **Inference / Prediction:**
   - Tested real-time prediction pipeline with sample input vectors.

---

## 📈 Model Performance

| Metric | Score |
| :--- | :--- |
| **Accuracy** | **90.00%** |
| **Iris-setosa F1-Score** | **1.00** |
| **Iris-versicolor F1-Score** | **0.86** |
| **Iris-virginica F1-Score** | **0.84** |

### Confusion Matrix
