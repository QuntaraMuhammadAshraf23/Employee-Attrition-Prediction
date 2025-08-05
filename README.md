# 🏢 Employee Attrition Prediction

## 📌 Overview
This project predicts whether an employee is likely to leave a company using **machine learning** techniques.  
It uses the IBM HR Analytics Employee Attrition dataset from Kaggle and applies both **Logistic Regression** and **Random Forest** classifiers.

In addition to model training and evaluation, the project **generates predictions** for the test dataset so we can compare model outputs with actual attrition values.

---

## 📂 Dataset
- **Source**: [IBM HR Analytics Employee Attrition Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **Target Variable**: `Attrition` (Yes / No)
- **Features**: Age, Gender, Department, MonthlyIncome, DistanceFromHome, JobSatisfaction, OverTime, YearsAtCompany, JobRole, etc.

---

## 🎯 Objectives
1. Perform **Exploratory Data Analysis (EDA)** to understand factors influencing attrition.
2. Visualize relationships between features and attrition.
3. Train machine learning models to predict attrition.
4. Evaluate model performance using accuracy, confusion matrix, classification report, and ROC curve.
5. **Generate predictions** for employees in the test set.

---

## 📊 Project Workflow

### **1. Data Exploration (EDA)**
- Checked dataset shape and basic statistics.
- Identified attrition counts and average ages for those who left vs. stayed.
- Analyzed attrition rates by department, overtime status, and income levels.

### **2. Data Visualization**
- Count plots for attrition distribution.
- Boxplots for MonthlyIncome vs. Attrition.
- Age distribution histograms.
- Stacked bar charts for Department vs. Attrition.
- Heatmap for feature correlations.

### **3. Data Preprocessing**
- Encoded categorical variables (Label Encoding & One-Hot Encoding).
- Scaled features for Logistic Regression using **StandardScaler**.
- Handled class imbalance using **SMOTE (Synthetic Minority Oversampling Technique)**.

### **4. Model Training**
- **Logistic Regression** (with scaling & SMOTE)
- **Random Forest Classifier** (with SMOTE)

### **5. Model Evaluation**
- **Accuracy**
- **Confusion Matrix**
- **Classification Report**
- **ROC Curve**

### **6. Model Predictions**
- Generated predictions for the test dataset using both models.
- Compared predictions with actual values in a clean comparison table.
- Included probability scores for attrition risk.
---
## Results
### **Logistic Regression Performance**
- **Accuracy**: 0.13
- **Classification Report**:
          precision    recall  f1-score   support

       0       0.00      0.00      0.00       255
       1       0.13      1.00      0.23        39
  
> **Note**: Logistic Regression struggled with extreme class imbalance and predicted only one class for all test samples.

---

### **Random Forest Performance**
- **Accuracy**: 0.88
- **Classification Report**:
          precision    recall  f1-score   support

       0       0.88      1.00      0.93       255
       1       1.00      0.08      0.14        39

> **Note**: Random Forest performed significantly better, achieving high accuracy for the majority class but still showing lower recall for the minority class.



