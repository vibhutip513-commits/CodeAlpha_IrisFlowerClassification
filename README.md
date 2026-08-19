# Iris Flower Classification — CodeAlpha Task 1

An end-to-end machine learning project developed as part of the **CodeAlpha Data Science Internship**. This project classifies Iris flowers into three distinct species (*Iris-setosa*, *Iris-versicolor*, and *Iris-virginica*) using physical sepal and petal measurements via Scikit-Learn.

---

## Project Overview

- **Domain:** Data Science / Machine Learning
- **Task:** Multiclass Classification
- **Dataset:** Iris Flower Dataset (150 instances, 4 continuous features)
- **Algorithm:** Random Forest Classifier (`sklearn.ensemble`)
- **Model Accuracy:** 90.00%
- **Data Source:** Ingested dynamically via GitHub Raw CSV URL

---

## Features & Target

### Feature Matrix ($X$)[cite: 2]
- `SepalLengthCm`: Sepal length in centimeters
- `SepalWidthCm`: Sepal width in centimeters
- `PetalLengthCm`: Petal length in centimeters
- `PetalWidthCm`: Petal width in centimeters

### Target Variable ($y$)[cite: 2]
- `Species`: *Iris-setosa*, *Iris-versicolor*, *Iris-virginica*

---

## Workflow & Implementation

1. **Data Ingestion & Integrity Check**
   - Ingested the raw dataset directly from GitHub into a `pandas` DataFrame for reliable, session-independent execution.
   - Removed the non-predictive `Id` index column to prevent data leakage[cite: 2].
   - Verified zero missing values across all columns[cite: 2].

2. **Exploratory Data Analysis (EDA)**
   - Generated pairwise feature distribution plots using `seaborn` to examine class separability and cluster boundaries[cite: 2].

3. **Stratified Train-Test Split**
   - Partitioned the dataset using an 80/20 train-test ratio (`test_size=0.2`) with `stratify=y` to preserve balanced class distributions across splits[cite: 2].

4. **Model Training**
   - Trained an ensemble `RandomForestClassifier` configured with 100 decision trees (`n_estimators=100`, `random_state=42`)[cite: 2].

5. **Model Evaluation**
   - Assessed generalization performance on unseen test data using Accuracy, Classification Report (Precision, Recall, F1-Score), and a Confusion Matrix heatmap[cite: 2].

6. **Sample Inference**
   - Tested real-time prediction using a sample input vector `[5.1, 3.5, 1.4, 0.2]`, correctly classifying the sample as `Iris-setosa`[cite: 2].

---

## Model Performance

| Metric | Score |
| :--- | :--- |
| **Overall Accuracy** | **90.00%**[cite: 2] |
| ***Iris-setosa* F1-Score** | **1.00**[cite: 2] |
| ***Iris-versicolor* F1-Score** | **0.86**[cite: 2] |
| ***Iris-virginica* F1-Score** | **0.84**[cite: 2] |

### Confusion Matrix Breakdown[cite: 2]
```text
[[10   0   0]   -> Setosa: 10/10 correct (100% precision/recall)
 [ 0   9   1]   -> Versicolor: 9/10 correct (1 misclassified as Virginica)
 [ 0   2   8]]  -> Virginica: 8/10 correct (2 misclassified as Versicolor)

Tech Stack
Language: Python

Libraries:

pandas — Tabular data manipulation[cite: 2]

matplotlib & seaborn — Data visualization and evaluation heatmaps[cite: 2]

scikit-learn — Model training, stratified splitting, and evaluation metrics[cite: 2]

Getting Started
Clone the repository:


Install dependencies:

Bash
pip install pandas scikit-learn matplotlib seaborn

Install dependencies:

Bash
pip install pandas scikit-learn matplotlib seaborn
Run the notebook:

Open CodeAlpha_Iris_flower_prediction.ipynb in Jupyter Notebook, VS Code, or Google Colab and run all cells sequentially[cite: 2]


Author
Intern: Vibhuti Prajapati

Domain: Data Science

Organization: CodeAlpha
