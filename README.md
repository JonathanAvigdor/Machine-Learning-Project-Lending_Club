Loan Default Prediction (LendingClub Dataset)
📌 Project Overview

This project analyzes LendingClub loan data (2007–2020) and builds machine learning models to predict loan default risk.
The goal is to identify which borrowers are more likely to default, helping improve risk assessment and lending strategies.

📊 Dataset

Source: LendingClub public dataset (2007–2020)

Size: ~2.2M loans, 151 features

Categories of features:

Borrower info: employment length, annual income, credit history

Loan terms: amount, period, interest rate, monthly installment

Outcomes: loan status (Fully Paid / Default), payments, recoveries

⚠️ The full dataset is too large for GitHub (>100MB).
You can download it from: Kaggle – LendingClub Loan Data

🧹 Data Cleaning & Preprocessing

Steps included:

Dropped ID/text columns (id, url, etc.)

Removed rows with missing values

Handled outliers (1%–99% capping)

Encoded categorical variables (one-hot, ordinal for sub_grade)

Removed leakage features (e.g., total_pymnt, last_pymnt_d)

Train/test split + scaling for Logistic Regression

⚙️ Feature Engineering

Created new ratios:

Loan-to-Income = loan_amnt / annual_inc

Revol-to-Income = revol_bal / annual_inc

Grouped rare loan purposes into “Other”

🤖 Models Used

Logistic Regression

Random Forest

XGBoost

Models were wrapped in pipelines to combine preprocessing and training.

📈 Results

Best model: XGBoost

Achieved Recall = 0.90 (high ability to catch defaults)

Precision at this recall: ~0.24


🔮 Future Work

Try advanced resampling methods (SMOTE, ADASYN)

Hyperparameter tuning with cross-validation

Deploy as an interactive Streamlit app

👨‍💻 Author

Developed by Jonathan Avigdor

* LinkedIn: www.linkedin.com/in/jonathanavigdor
