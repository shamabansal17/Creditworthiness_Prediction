# Creditworthiness_Prediction
LoanTap Creditworthiness Prediction for Personal Loans

This project focuses on building an underwriting layer for LoanTap, an online platform providing customized loan products. The objective is to determine whether a personal loan should be extended to an individual and recommend suitable repayment terms. This case study will address the underwriting process for personal loans only.

## Project Overview

The goal is to predict whether a credit line should be extended based on the provided data, using logistic regression for classification. We aim to identify real defaulters while minimizing false positives, ensuring we don’t disburse loans to individuals likely to default.

## Dataset

The dataset `LoanTapData.csv` contains attributes related to loan applicants and their financial and credit history. The target variable is `loan_status`, which indicates the current status of the loan.

### Key Features:

- **loan_amnt**: Amount of loan applied for
- **term**: Duration of loan (36 or 60 months)
- **int_rate**: Interest rate on the loan
- **grade**: LoanTap assigned loan grade
- **emp_length**: Borrower's employment length in years
- **annual_inc**: Annual income of the borrower
- **dti**: Debt-to-income ratio
- **revol_bal**: Revolving credit balance
- **pub_rec**: Number of derogatory public records
- **mort_acc**: Number of mortgage accounts
- **application_type**: Individual or joint application
- And many more...

## Conceptual Approach

1. **Exploratory Data Analysis (EDA)**:
   - Checking dataset structure, missing values, and outliers.
   - ViZualization of relationships between features and the target variable (using count plots, box plots, heatmaps).
   - Checking correlations among independent variables.

2. **Feature Engineering**:
   - Creation of flag features: Convert categorical data to binary values for features like `pub_rec`, `mort_acc`, and `pub_rec_bankruptcies`.

3. **Missing Value & Outlier Treatment**:
   - Imputation of missing values and handling of outliers.

4. **Scaling**:
   - Normalization using MinMaxScaler or StandardScaler.

5. **Modeling**:
   - Logistic Regression for predicting loan approval.
   - Evaluation of results using:
     - Classification Report
     - ROC AUC Curve
     - Precision-Recall Curve

## Tradeoff Challenges

- **Minimizing False Positives**: Detecting real defaulters is crucial to avoid non-performing assets (NPAs), ensuring we only disburse loans to creditworthy individuals.
- **Precision vs Recall**: Optimizing the balance between precision (minimizing false positives) and recall (identifying true positives).

## Results

The model's performance will be evaluated based on:
- **Accuracy**: Overall accuracy of the model.
- **ROC AUC**: The area under the ROC curve to evaluate classification performance.
- **Precision-Recall Tradeoff**: Assessing the balance between precision and recall to minimize financial risk.

## Actionable Insights & Recommendations

- **Risk Mitigation**: Focus on reducing false positives to avoid potential NPAs.
- **Loan Approval Optimization**: Tailoring loan approval criteria based on employment length, annual income, and revolving credit balance to ensure the right customers are granted loans.

## Requirements

- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `statsmodels`


## Conclusion

This project provides a structured approach to evaluating loan eligibility based on historical data, with a focus on minimizing financial risk through accurate predictions.
