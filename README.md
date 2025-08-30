# LOAN-PREDICTION-PROJECT

## 🗒️ Table of Contents
- [Project Overview](#project-overview)  
- [Description](#description)  
- [Problem Statement](#problem-statement)  
- [Project Objective](#project-objective)  
- [Key Areas Analyzed](#key-areas-analyzed)  
- [Data Source](#data-source)  
- [Dataset Description](#dataset-description)  
- [Tools](#tools)  
- [Methodology](#methodology)  
- [Data Cleaning](#data-cleaning)  
- [Summary Statistics Interpretation](#summary-statistics-interpretation)  
- [Visual Insights](#visual-insights)  
- [Multicollinearity Check (VIF)](#multicollinearity-check-vif)  
- [Handling Multicollinearity](#handling-multicollinearity)  
- [Logistic Regression Model](#logistic-regression-model)  
- [Predictors Interpretation](#predictors-interpretation)  
- [Model Evaluation](#model-evaluation)  
- [Recommendation](#recommendation)  
- [Acknowledgement](#acknowledgement)  
- [Contact](#contact)

  ## 📌 Project Overview
This project predicts **whether a loan application will be approved or not** based on applicant details such as age, income, employment, credit history, and loan details.  
It uses **Logistic Regression**, a statistical model, to make predictions.

## 📝 Description
Financial institutions like banks and loan companies face the challenge of deciding **who should be given a loan**. Poor lending decisions can lead to defaults.  
This project provides a **data-driven approach** to help lenders make informed decisions.

## ❓ Problem Statement
Loan default is one of the biggest challenges faced by financial institutions. Traditional manual methods of assessing applications are time-consuming and may overlook important patterns in customer data. This leads to high rejection rates, approval of risky applicants, and loss of potential revenue. To address this, a data-driven approach is required to analyze customer attributes and build a predictive system that can improve decision-making, reduce risks, and ensure fair loan approvals.

## 🎯 Project Objective
1. Clean and explore the loan dataset.  
2. Identify key features affecting loan approval.  
3. Build a logistic regression model to predict loan approval.  
4. Evaluate model performance.  
5. Provide recommendations for decision-making.


## 📂 Data Source
The dataset was obtained from kaggle website | LINK 


## 📊 Dataset Description
- **Rows:** 45,000 applicants  
- **Columns:** 14 variables (age, gender, income, loan amount, credit score, etc.)  
- **Target Variable:** `loan_status` (0 = Not Approved, 1 = Approved)  

## 🛠 Tools
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels)  
