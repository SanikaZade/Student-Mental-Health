Here is a comprehensive and professional `README.md` file tailored for your GitHub repository, incorporating all the details provided.

***

# 🧠 Student Mental Health Prediction using Machine Learning

### *3rd Semester PBL Project*

This project aims to build and evaluate machine learning classification models capable of predicting student mental health categories based on survey responses. By analyzing demographic details, academic performance, lifestyle habits, and mental health screening results, this study identifies the most accurate predictive model for early identification and intervention of mental health issues (such as depression and anxiety) among university students.

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Objective](#objective)
- [Tech Stack & Libraries](#tech-stack--libraries)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Model Performance & Results](#model-performance--results)
- [Key Takeaways](#key-takeaways)
- [How to Run](#how-to-run)
- [Contributors](#contributors)

---

## 🎯 Objective

The primary objectives of this study are:
1. To evaluate the accuracy of six Machine Learning algorithms in predicting mental health problems in FEAT, DMIHER (DU) university students.
2. To identify the best model for **early identification and intervention**.
3. To help establish targeted approaches that assist students in mitigating the negative effects of mental health problems on their academic performance, social well-being, and overall quality of life.

---

## 🛠 Tech Stack & Libraries

*   **Language:** Python
*   **Data Manipulation:** Pandas
*   **Data Visualization:** Seaborn, Matplotlib
*   **Machine Learning Framework:** Scikit-Learn (`sklearn`)
*   **Preprocessing:** `StandardScaler`
*   **Data Splitting:** `train_test_split`

### Models Implemented:
1.  Logistic Regression
2.  Support Vector Machine (SVM - Linear Kernel)
3.  Decision Tree Classifier
4.  Random Forest Classifier
5.  K-Nearest Neighbors (KNN)
6.  Naive Bayes (GaussianNB)

### Evaluation Metrics:
*   Accuracy Score
*   Precision
*   Recall
*   F1-Score (Weighted Average)
*   Confusion Matrix

---

## 📊 Dataset

*   **Source:** Survey data collected from university students.
*   **Size:** 142 student responses.
*   **Features:** The dataset encompasses:
    *   Demographic information
    *   Academic performance metrics
    *   Lifestyle habits
    *   Results of mental health screening (20-question survey)
*   **Target Variable:** Mental Health Category/Status (`'Target'` column).

> **File:** `Dataset_student_mental_health.csv`

---

## ⚙️ Methodology

The project follows a standard machine learning pipeline:

### 1. Data Loading & Preprocessing
*   The dataset is loaded using Pandas.
*   **Feature Extraction ($X$):** Irrelevant or non-numeric metadata columns such as `'Email Address'`, `'Sum'`, `'Category'`, and the target label `'Target'` are dropped.
*   **Target Variable ($y$):** Classification labels are extracted from the `'Target'` column.

### 2. Data Splitting
*   The dataset is split into training and testing sets using an **80-20 split** (`test_size=0.2`).
*   A fixed `random_state=42` is used for reproducibility.
*   **Training Set Size:** 113 samples.

### 3. Feature Scaling
*   Features are standardized using Scikit-Learn’s `StandardScaler`.
*   The scaler is fitted on the training data and applied to both training and test sets to ensure all variables contribute equally to model performance.

### 4. Model Training & Comparison
*   Multiple machine learning models are trained and evaluated in a loop.
*   Performance metrics (Accuracy, Precision, Recall, F1-Score) are calculated for each model.
*   A confusion matrix and heatmap are generated for detailed error analysis (specifically demonstrated for the SVM model).

---

## 📈 Model Performance & Results

The following table compares the performance of the six classifiers based on weighted averages:

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Logistic Regression** | **96.55%** | 0.967 | 0.966 | 0.965 |
| **SVM (Linear)** | **96.55%** | 0.967 | 0.966 | 0.965 |
| **Naive Bayes** | 93.10% | 0.937 | 0.931 | 0.928 |
| **Random Forest** | 79.31% | 0.786 | 0.793 | 0.768 |
| **K-Nearest Neighbors** | 79.31% | 0.839 | 0.793 | 0.744 |
| **Decision Tree** | 75.86% | 0.741 | 0.759 | 0.717 |

*(Note: Percentages are rounded for readability)*

---

## 💡 Key Takeaways

*   **Top Performers:** **Logistic Regression** and **Linear SVM** significantly outperform other algorithms on this dataset, achieving the highest accuracy of **~96.55%**.
*   **Efficiency:** Simple linear models proved more effective than complex ensemble methods (like Random Forest) for this specific dataset size and feature set.
*   **Impact:** Early identification using these high-accuracy models can facilitate timely interventions, helping students manage stress, anxiety, and depression before they severely impact academic and social life.

---

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/SanikaZade/Student-Mental-Health.git
    cd Student-Mental-Health
    ```

2.  **Install dependencies:**
    Ensure you have Python installed, then install the required libraries:
    ```bash
    pip install pandas seaborn matplotlib scikit-learn
    ```

3.  **Run the Notebook:**
    Open `ML Code.ipynb` in Jupyter Notebook or JupyterLab to view the code, visualizations, and results.

---
