# Customer Churn Prediction Using Decision Tree

A machine learning classification project that predicts whether a bank customer is likely to leave the bank using a Decision Tree Classifier. The project covers data preprocessing, exploratory data analysis, categorical encoding, model training, hyperparameter tuning, and performance evaluation.

## Project Overview

Customer churn is an important business problem for banks because retaining existing customers is often more valuable than acquiring new ones.

In this project, a Decision Tree classification model is developed to predict customer churn based on demographic, financial, and account-related features.

The project includes both a baseline Decision Tree and a tuned Decision Tree model to compare model performance.

## Objectives

- Analyze customer churn data.
- Perform exploratory data analysis (EDA).
- Prepare data for machine learning.
- Encode categorical variables.
- Train a baseline Decision Tree Classifier.
- Tune the Decision Tree model.
- Evaluate model performance using classification metrics and ROC-AUC.
- Identify important features influencing model predictions.
- Derive useful business insights from the model.

## Dataset

The dataset contains information about bank customers and whether they exited the bank.

### Target Variable

- `Exited = 0` → Customer stayed
- `Exited = 1` → Customer exited

### Main Features

- CreditScore
- Geography
- Gender
- Age
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary

The dataset contains **10,000 customer records** and **14 original columns**.

## Data Preprocessing

The following preprocessing steps were performed:

1. Removed unnecessary identifier columns:
   - `RowNumber`
   - `CustomerId`
   - `Surname`

2. Removed the temporary `AgeGroup` feature after exploratory analysis.

3. Separated the features (`X`) and target (`y`).

4. Split the dataset into training and testing sets using an 80/20 split.

5. Used stratified splitting to preserve the target-class distribution.

6. Applied One-Hot Encoding to categorical features:
   - `Geography`
   - `Gender`

7. No feature scaling was required because Decision Trees are not distance-based algorithms.

## Machine Learning Models

### 1. Baseline Decision Tree

A default `DecisionTreeClassifier` was trained first to establish a baseline performance.

### 2. Tuned Decision Tree

The model was then tuned using the following parameters:

```python
DecisionTreeClassifier(
    max_depth=5,
    min_samples_split=10,
    min_samples_leaf=5,
    random_state=42
)
