# Customer Churn Prediction Using Decision Tree

A machine learning classification project that predicts whether a bank customer is likely to leave the bank using a Decision Tree Classifier.

The project covers data preprocessing, exploratory data analysis (EDA), categorical encoding, model training, hyperparameter tuning, feature importance analysis, cross-validation, and performance evaluation.

---

## Project Overview

Customer churn is an important business problem for banks because retaining existing customers can be more valuable than acquiring new customers.

In this project, a Decision Tree classification model is developed to predict whether a bank customer will exit the bank based on demographic, financial, and account-related features.

Two models are developed and compared:

- Baseline Decision Tree
- Tuned Decision Tree

The project also analyzes important features and evaluates the model from a business perspective.

---

## Objectives

- Analyze customer churn data.
- Perform exploratory data analysis (EDA).
- Prepare the dataset for machine learning.
- Remove unnecessary identifier columns.
- Encode categorical variables.
- Split the dataset into training and testing sets.
- Train a baseline Decision Tree Classifier.
- Tune the Decision Tree model.
- Evaluate model performance using classification metrics.
- Evaluate ROC-AUC performance.
- Analyze feature importance.
- Perform 5-Fold Cross-Validation.
- Derive useful business insights from the model.

---

## Dataset

The dataset contains information about bank customers and whether they exited the bank.

### Dataset Size

- **Rows:** 10,000
- **Original Columns:** 14

### Target Variable

The target variable is `Exited`.

- `Exited = 0` → Customer stayed
- `Exited = 1` → Customer exited

### Main Features

- `CreditScore`
- `Geography`
- `Gender`
- `Age`
- `Tenure`
- `Balance`
- `NumOfProducts`
- `HasCrCard`
- `IsActiveMember`
- `EstimatedSalary`

### Original Columns

```text
RowNumber
CustomerId
Surname
CreditScore
Geography
Gender
Age
Tenure
Balance
NumOfProducts
HasCrCard
IsActiveMember
EstimatedSalary
Exited
