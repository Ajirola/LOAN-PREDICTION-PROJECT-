# LOAN-PREDICTION-PROJECT

## 🗒️ Table of Contents
- [Project Overview](#project-overview)  
- [Description](#description)  
- [Problem Statement](#problem-statement)  
- [Project Objective](#project-objective)  
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
A machine learning project to predicts **whether a loan application will be approved or not** based on applicant details such as age, income, employment, credit history, and loan details.  
It uses **Logistic Regression**, a statistical model, to make predictions.

## 📝 Description
Financial institutions like banks and loan companies face the challenge of deciding **who should be given a loan**. Poor lending decisions can lead to defaults.  
This project provides a **data-driven approach** to help lenders make informed decisions.

## ❓ Problem Statement
Loan default is one of the biggest challenges faced by financial institutions. Traditional manual methods of assessing applications are time-consuming and may overlook important patterns in customer data. This leads to high rejection rates, approval of risky applicants, and loss of potential revenue. To address this, a data-driven approach is required to analyze customer attributes and build a predictive system that can improve decision-making, reduce risks, and ensure fair loan approvals.

## 🎯 Project Objective
To develop a **predictive model** that accurately determines **loan approval** based on applicant attributes.


## 📂 Data Source
The dataset was obtained from kaggle website | [LINK](#https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data)

## 📊 Dataset Description
The dataset used is a loan application dataset containing **45,000 records** and **14 features**.  

- **Target variable:** loan_status (0 = Not Approved, 1 = Approved)

- **Independent variables:** applicant’s demographics, loan details, and credit history.

| Feature | Description |
|---------|-------------|
| person_age | Age of applicant |
| person_gender | Gender of applicant |
| person_education | Education level |
| person_income | Annual income |
| person_emp_exp | Employment experience (years) |
| person_home_ownership | Home ownership status |
| loan_amnt | Loan amount requested |
| loan_intent | Loan purpose (Education, Medical, etc.) |
| loan_int_rate | Loan interest rate (%) |
| loan_percent_income | Loan-to-income ratio |
| cb_person_cred_hist_length | Credit history length (years) |
| credit_score | Credit score of applicant |
| previous_loan_defaults_on_file | Past default record (Yes/No) |
| loan_status | Target variable (0 = Not Approved, 1 = Approved) |


## 🛠 Tools
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)

- **Scikit-learn** (Logistic Regression, preprocessing, evaluation)

- **Statsmodels** (VIF for multicollinearity checks)

## 🔍 Methodology
1. Data Cleaning – Handle missing values, duplicates, inconsistent data.

2. Exploratory Data Analysis (EDA) – Understand data patterns using statistics and visualizations.

3. Multicollinearity Check – Ensure predictors are not too closely related.

4. Model Building – Train a Logistic Regression model.

5. Model Evaluation – Check accuracy, precision, recall, ROC-AUC.

## 🧹 Data cleaning 
- No missing values found.

- No duplicate records.

- Encoded categorical variables (gender, education, loan intent, etc.) into numbers.

## 📈 Summary Statistics Interpretation
- **Average age = 28 years** → mostly young applicants.  
- **Average income = 80,000**.  
- **Loan amounts ranged from 500 – 35,000.**  
- **Credit scores mostly between 600 – 850.**  
- About **22% of applicants were approved** (`loan_status = 1`), while **78% were rejected** (`loan_status = 0`).

## 📊 Visual insights 
![Screenshot](Screenshot_20250830-182947.jpg)

**Loan Status Distribution**  
  - Majority of applicants (78%) had their loans **not approved**.  
  - Only about 22% were **approved**, showing that lenders are more conservative in approvals.
    
![Screenshot](Screenshot_20250830-183043.jpg)

**Loan Intent**  
  - Most loan applications were for **medical, education, and personal use**.  
  - This shows that many applicants borrow for essential needs (health, school) and personal expenses.  

![Screenshot](Screenshot_20250830-183059.jpg)

**Education Level**  
  - Majority of applicants had **Bachelor’s education**.  
  - Applicants with **Master’s and Doctorate degrees** were fewer but still significant.
    

![Screenshot](Screenshot_20250830-183113.jpg)

**Home Ownership**  
- Most applicants were **renters**, followed by those with a **mortgage**.  
- Few applicants fully owned their homes, showing higher dependency on borrowed housing.

## 📉 Multicollinearity Check (VIF)

Variance Inflation Factor (VIF) was calculated to detect multicollinearity among predictors:

| Feature                        | VIF       | Interpretation |
|--------------------------------|-----------|----------------|
| const                          | 379.91    | ❌ Very high (ignored, constant term) |
| person_age                     | 14.12     | ❌ High multicollinearity |
| person_gender                  | 1.00      | ✅ No multicollinearity |
| person_education               | 1.00      | ✅ No multicollinearity |
| person_income                  | 1.44      | ✅ Acceptable |
| person_emp_exp                 | 11.27     | ❌ High multicollinearity |
| person_home_ownership          | 1.16      | ✅ Acceptable |
| loan_amnt                      | 2.20      | ✅ Acceptable |
| loan_intent                    | 1.00      | ✅ No multicollinearity |
| loan_int_rate                  | 1.08      | ✅ Acceptable |
| loan_percent_income            | 2.21      | ✅ Acceptable |
| cb_person_cred_hist_length     | 3.93      | ✅ Moderate, acceptable |
| credit_score                   | 1.07      | ✅ Acceptable |
| previous_loan_defaults_on_file | 1.13      | ✅ Acceptable |

### 🔎 Interpretation
- **Threshold:** A VIF > 10 indicates **high multicollinearity**.  
- `person_age (14.12)` and `person_emp_exp (11.27)` show **serious multicollinearity** ❌.  
- Most other predictors have **VIF < 5**, meaning they are acceptable ✅.  






