# TWO-WHEELER LOAN PREDICTION PROJECT

## Title
🏍️ TWO-WHEELER LOAN PREDICTION

## Overview
This project develops a robust machine learning model for financial institutions to accurately predict the creditworthiness of two-wheeler loan applicants, thereby streamlining the approval process and minimizing the risk of loan default.

## Problem Statement Overview
Two-wheeler loans carry inherent risk. Manual evaluation of applicants is slow and inconsistent. This project addresses this by building a machine learning model to predict loan approval based on the applicant's credit, demographic, and financial history.

## Project Objective
The primary objective is to develop a machine learning regression model that can accurately predict the **Credit Score** (a quantification of creditworthiness) of two-wheeler loan applicants, providing a faster and more reliable decision-making tool.

## Data Description
* **Dataset Source:** Credit Profile Two-Wheeler Loan Dataset (Kaggle)
* **Dataset Size:** 279,856 rows and 15 columns.
* **Target Variable (to be predicted):** **Credit Score**
* **Key Features:** Age, Gender, Existing Customer, State, City, Income, Credit History Length, Number of Existing Loans, Loan Amount, Loan Tenure, LTV Ratio, Employment Profile, Occupation, Profile Score.

## Methodology and Model Pipeline

### Data Preprocessing & Feature Engineering
1.  **Imbalance Check:** Dataset is highly balanced (Imbalance Ratio of 1.01).
2.  **Transformation:** Square Root Transformation applied to `Income` and `Loan Tenure`. Power Transformation (Yeo-Johnson) applied to `Profile Score`.
3.  **Scaling:** Features standardized using `StandardScaler`.

### Model Building (Regression)
The following regression algorithms were compared for predicting the continuous Credit Score:
* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor (Ensemble method)
* Gradient Boosting Regressor
* K-Nearest Neighbors Regressor

## Model Evaluation and Results
Evaluation metrics used: **Mean Squared Error (MSE)** and **R-squared ($R^2$) score**.

| Model | MSE | R-squared |
| :--- | :--- | :--- |
| **Random Forest** | **82.91** | **0.9969** |
| Decision Tree | 120.05 | 0.9955 |
| Gradient Boosting | 197.28 | 0.9926 |
| Linear Regression | 263.10 | 0.9901 |
| K-Nearest Neighbors | 1186.12 | 0.9556 |

### Performance Insight
The **Random Forest Regressor** achieved the best performance (Lowest MSE: 82.91; Highest $R^2$: 0.9969), indicating an exceptional fit for credit score prediction.

## Conclusion and Final Verdict
The project successfully demonstrated that machine learning can accurately predict loan approval outcomes. The final model, the Random Forest Regressor, is highly accurate and possesses strong potential for real-world application in banking and financial decision-making.

### Future Enhancements
* Fine-tune the best-performing model further.
* Collect more balanced data, especially for low-credit applicants.
* Apply advanced feature engineering to capture hidden financial behavior patterns.
* Use cross-validation and additional ensemble techniques for better generalization.
