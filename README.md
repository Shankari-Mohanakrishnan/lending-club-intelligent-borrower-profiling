# Lending Club Intelligent Borrower Profiling

An end-to-end machine learning project that builds an intelligent borrower profiling framework for credit risk assessment, risk-aware loan decision making, and portfolio optimization using the Lending Club loan dataset.

---

## Project Overview

Financial institutions receive thousands of loan applications every day. Approving every application increases credit losses, while rejecting too many borrowers reduces revenue and customer growth.

The objective of this project is to build an end-to-end credit risk framework that predicts borrower default risk, estimates expected credit loss, supports explainable lending decisions, and demonstrates portfolio optimization techniques commonly used in banking.

The project follows a practical credit risk workflow used by financial institutions:

```
Loan Application
        ↓
Data Understanding
        ↓
Data Cleaning & Preprocessing
        ↓
Feature Engineering
        ↓
Probability of Default (PD) Modeling
        ↓
Model Explainability (SHAP)
        ↓
Borrower Risk Segmentation
        ↓
Loss Given Default (LGD)
        ↓
Exposure at Default (EAD)
        ↓
Expected Loss Calculation
        ↓
Risk-Based Loan Decision Engine
        ↓
Portfolio Optimization
        ↓
Executive Business Summary
```

---

## Dataset

**Source:** Lending Club Loan Dataset

The dataset contains historical loan application information including borrower demographics, financial attributes, repayment history, loan characteristics, and loan outcomes.

Because of dataset size and licensing considerations, the raw dataset is not included in this repository.

---

## Project Structure

```
lending-club-intelligent-borrower-profiling/

│
├── data/
│
├── notebooks/
│   ├── 01_Data_Understanding.ipynb
│   ├── 02_Data_Cleaning_Preprocessing.ipynb
│   ├── 03_Feature_Engineering.ipynb
│   ├── 04_Probability_of_Default_Model.ipynb
│   ├── 05_Model_Explainability_SHAP.ipynb
│   ├── 06_Risk_Segmentation.ipynb
│   ├── 07_LGD_EAD_Expected_Loss.ipynb
│   ├── 08_Risk_Decision_Engine.ipynb
│   ├── 09_Portfolio_Optimization.ipynb
│   └── 10_Executive_Business_Summary.ipynb
│
├── images/
│
├── README.md
└── requirements.txt
```

---

## Machine Learning Workflow

### 1. Data Understanding

* Dataset exploration
* Data quality assessment
* Missing value analysis
* Target variable analysis
* Feature categorization

### 2. Data Cleaning

* Removal of highly missing features
* Target variable creation
* Removal of leakage variables
* Duplicate checking
* Data preprocessing

### 3. Feature Engineering

Engineered multiple business-driven borrower risk indicators including:

* Loan-to-Income Ratio
* Installment-to-Income Ratio
* Credit History Length
* Creditworthiness Score
* Financial Stability Score
* Repayment Capacity Score
* High DTI Flag
* High Revolving Utilization Flag
* Delinquency Indicators
* Bankruptcy Indicators
* Grade and Sub-grade Ordinal Encoding

### 4. Probability of Default (PD) Modeling

Models evaluated:

* Logistic Regression
* Random Forest
* LightGBM

Evaluation metrics:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

### 5. Model Explainability

Global feature importance was analyzed using SHAP values to improve model transparency and explainability.

### 6. Borrower Risk Segmentation

Borrowers were segmented into five credit risk bands:

* Very Low Risk
* Low Risk
* Medium Risk
* High Risk
* Very High Risk

### 7. Credit Risk Metrics

The project estimates:

* Probability of Default (PD)
* Loss Given Default (LGD)
* Exposure at Default (EAD)
* Expected Loss (EL)

### 8. Risk-Based Decision Engine

Loan applications are classified into:

* Approve
* Manual Review
* Reject

based on predicted credit risk.

### 9. Portfolio Optimization

A portfolio optimization strategy is developed to compare lending performance before and after risk-based borrower selection.

---

## Key Results

### Best Probability of Default Model

| Metric     | Value    |
| ---------- | -------- |
| Best Model | LightGBM |
| ROC-AUC    | 0.7625   |
| Recall     | 0.6743   |
| Precision  | 0.3918   |

### Top SHAP Risk Drivers

* Sub Grade
* Issue Year
* Total Late Fees
* Loan Term
* Loan Grade
* Number of Recently Opened Accounts
* Average Current Balance
* Financial Stability Score
* Creditworthiness Score
* Revolving Credit Accounts

### Risk Segmentation

Borrowers were grouped into five risk categories with progressively increasing default rates, enabling risk-aware lending decisions.

### Portfolio Optimization

The optimized lending portfolio demonstrated:

* Lower average Probability of Default
* Lower observed default rate
* Reduced expected credit loss
* Improved risk-adjusted portfolio performance

---

## Technologies Used

### Programming

* Python

### Data Analysis

* Pandas
* NumPy

### Machine Learning

* Scikit-learn
* LightGBM

### Explainable AI

* SHAP

### Visualization

* Matplotlib
* Seaborn

---

## Skills Demonstrated

* Credit Risk Modeling
* Feature Engineering
* Machine Learning
* Explainable AI (XAI)
* Probability of Default Modeling
* Expected Loss Modeling
* Portfolio Analytics
* Risk Segmentation
* Business Decision Support
* Financial Data Analysis

---

## Future Enhancements

Potential improvements include:

* Hyperparameter optimization
* Cross-validation framework
* Probability calibration
* Cost-sensitive learning
* Fairness analysis
* Model deployment using FastAPI
* Interactive dashboard using Streamlit or Power BI

---




