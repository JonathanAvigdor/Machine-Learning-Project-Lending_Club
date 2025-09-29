# 📊 Loan Default Prediction (LendingClub Dataset)

This project applies machine learning to **LendingClub loan data (2007–2020)** to predict **loan defaults**.  
The dataset contains **2.2M loans and 151 features**, including borrower information, loan terms, and repayment outcomes.  
Using models such as **Logistic Regression, Random Forest, and XGBoost**, I achieved a recall of **0.90** — meaning the model successfully identifies 90% of defaulting loans.

---

## 📂 Dataset
- Source: LendingClub public dataset (2007–2020)  
- Size: ~2.2M loans, 151 features  
- Features include:
  - Borrower info: employment length, annual income, credit history  
  - Loan terms: loan amount, period, interest rate, monthly installment  
  - Outcomes: loan status (Fully Paid / Default), total payments, recoveries  

⚠️ **Note:** The full dataset is too large for GitHub (>100MB).  
You can download it here: [Kaggle – LendingClub Loan Data](https://www.kaggle.com/wordsforthewise/lending-club)  

---

## 🧹 Data Preparation
- Removed IDs, text fields, and leakage features (e.g., payment history)  
- Dropped rows with missing values and capped outliers  
- Encoded categorical features (ordinal + one-hot)  
- Scaled numeric variables for certain models  
- Train/test split to ensure fair evaluation  

---

## ⚙️ Feature Engineering
- Created key ratios:
  - Loan-to-Income = `loan_amnt / annual_inc`  
  - Revol-to-Income = `revol_bal / annual_inc`  
- Consolidated rare loan purposes into "Other"  

---

## 🤖 Models Tested
- Logistic Regression
- Decision Tree  
- Random Forest  
- XGBoost ✅ (best performance)  

All models were built with **pipelines** to combine preprocessing and training steps.  

---

## 📈 Results
- Best model: **XGBoost**  
- Recall = **0.90** (caught 90% of defaults)  
- Precision ≈ **0.24**  

---

## 🔮 Next Steps
- Apply advanced resampling methods (SMOTE, ADASYN)  
- Deploy an interactive dashboard with Streamlit  

---

## 👨‍💻 Author
Developed by **Jonathan Avigdor**  
- [LinkedIn](www.linkedin.com/in/jonathanavigdor)  
