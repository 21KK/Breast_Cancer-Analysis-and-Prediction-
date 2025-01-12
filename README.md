# Breast Cancer Analysis and Prediction Using Logistic Regression

## 📊 Project Overview

This project aims to analyze and predict breast cancer diagnoses using logistic regression. By applying data preprocessing, exploratory data analysis (EDA), and machine learning, the project demonstrates how predictive modeling can aid in early detection and diagnosis of breast cancer. 

### Why Breast Cancer Data Analysis matters?
Breast cancer remains one of the most prevalent cancers globally, affecting millions of individuals each year. Early detection and effective treatment strategies are essential to improving patient outcomes. Data-driven insights play a key role in enabling innovation in diagnostics, enhancing drug safety, and paving the way for precision medicine. This project provides a foundation for identifying actionable patterns that could support these advancements.
![image](https://github.com/user-attachments/assets/3319675d-b835-4160-95db-23fc389d6a00)
 
---

## 📂 Table of Contents

1. [Introduction](#introduction)  
2. [Dataset Details](#dataset-details)  
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
4. [Data Preprocessing](#data-preprocessing)  
5. [Modeling](#modeling)  
6. [Evaluation Metrics](#evaluation-metrics)  
7. [Results and Insights](#results-and-insights)  
8. [Conclusion and Future Work](#conclusion-and-future-work)  
9. [How to Run](#how-to-run)  

---

## 📖 Introduction

Breast cancer is a significant health issue affecting millions of people worldwide. Accurate classification of tumors as benign or malignant is crucial for effective treatment and improved patient outcomes. This project explores the use of logistic regression, a widely used machine learning technique, to predict tumor diagnoses.

---

## 📁 Dataset Details

### 🔗 Source
The dataset is sourced from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29).

### 📊 Key Features
The dataset contains **569 samples** with the following attributes:
- **30 numerical features** extracted from breast mass measurements (e.g., radius, texture, perimeter, area, smoothness).
- **Diagnosis**: The target variable with two classes:
  - **M**: Malignant (Cancerous)
  - **B**: Benign (Non-Cancerous)

### 🔍 Data Snapshot
| Feature           | Mean Value (Benign) | Mean Value (Malignant) |
|--------------------|---------------------|-------------------------|
| Radius (mean)      | 12.1               | 17.5                   |
| Texture (mean)     | 17.8               | 21.6                   |
| Smoothness (mean)  | 0.09               | 0.1                    |

---

## 📊 Exploratory Data Analysis (EDA)

EDA was conducted to uncover trends and relationships in the data. Below are key findings:

### 🔍 Feature Distributions
Visualizations such as histograms and boxplots were used to understand the distributions of numerical features.

**Example: Distribution of Radius Mean**  
![Radius Mean Distribution](https://github.com/user-attachments/assets/f4b1e83a-3aca-4a8a-9b48-1934dee6d719)

)

### 🔗 Correlation Analysis
A heatmap was used to identify correlations among features. High correlations were found between:
- **Radius_mean** and **Perimeter_mean**
- **Area_mean** and **Compactness_mean**

**Correlation Heatmap**  
![Correlation Heatmap](https://github.com/user-attachments/assets/d4970272-2cde-438f-b1b4-9de8059ed900)

---

## 🛠️ Data Preprocessing

1. **Data Cleaning**:
   - No missing values in the dataset.
   - Target variable encoded: `M = 1`, `B = 0`.

2. **Feature Scaling**:
   - StandardScaler was applied to normalize feature ranges for better model performance.

3. **Train-Test Split**:
   - 80% training, 20% testing.

---

## 🤖 Modeling

### Algorithm: Logistic Regression
- Logistic regression is ideal for binary classification problems due to its simplicity and interpretability.

### Training
The `LogisticRegression` class from `scikit-learn` was used:
- Solver: `liblinear`  
- Regularization: L2 penalty

---

## 📈 Evaluation Metrics

The model was evaluated using multiple metrics to ensure reliability:

## **Accuracy**: 94% on the Train set and 92% on Test set.  

---

## 📊 Results and Insights

- **Key Features**:
  - `radius_mean`, `area_mean`, and `compactness_mean` were the most significant predictors of malignancy.
- **Model Coefficients**:  
  Logistic regression coefficients provided interpretable insights into feature importance.


---

## 🚀 Conclusion and Future Work

### Conclusion
- The logistic regression model effectively classified breast cancer tumors with high accuracy.
- EDA provided valuable insights into key predictors of malignancy.

### Future Work
1. Implement additional algorithms (e.g., Random Forest, XGBoost) for comparison.
2. Deploy the model as a web-based diagnostic tool using Flask or Streamlit.
3. Expand the dataset with more samples for improved generalizability.

---

## ⚙️ How to Run

### Prerequisites
- Python >= 3.7
- Libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`

