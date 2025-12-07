🏍️ TWO-WHEELER LOAN PREDICTION
This project aims to develop a robust machine learning model for financial institutions to accurately predict the creditworthiness of two-wheeler loan applicants, thereby streamlining the approval process and minimizing the risk of loan default.
🚀 Problem Statement Overview
Two-wheeler loans are common in developing countries, but financial institutions face risk when approving them. Manually evaluating each applicant's creditworthiness is time-consuming and often inconsistent. This project addresses this by building a machine learning model that predicts whether a loan should be approved based on the applicant's profile, including their credit, demographic, and financial history.
🎯 Project Objective
The primary objective is to develop a machine learning regression model that can accurately predict the Credit Score (a quantification of creditworthiness) of two-wheeler loan applicants. By leveraging historical data, the model seeks to provide financial institutions with a faster and more reliable decision-making tool.
📝 Data Description
The model was trained on a comprehensive dataset focusing on credit profiles for two-wheeler loans.
Dataset Source: Credit Profile Two-Wheeler Loan Dataset (Kaggle)Dataset Size: 279,856 rows and 15 columns.
Target Variable (to be predicted): Credit Score
Key Features:Demographic/Identity: Age, Gender, Existing Customer, State, CityFinancial/Credit: Income, Credit History Length, Number of Existing Loans, Loan Amount, Loan Tenure, LTV Ratio, Employment Profile, Occupation, Profile Score
⚙️ Methodology and Model
PipelineData Preprocessing & Feature Engineering
1)Imbalance Check: The dataset was found to be highly balanced with an Imbalance Ratio of 1.01, thus eliminating the need for balancing techniques like SMOTE.
2)Transformation:
Square Root Transformation was applied to mildly skewed numerical features like Income and Loan Tenure to reduce skewness.
Power Transformation (Yeo-Johnson) was applied to the Profile Score feature.
Scaling: Features were standardized using StandardScaler for appropriate models.
Model Building (Regression)The project compared the performance of multiple regression algorithms to predict the continuous Credit Score.
AlgorithmDescriptionLinear RegressionSimplest form, best for linear relationships.Decision Tree RegressorSplits data based on feature thresholds to model non-linear relationships.Random Forest RegressorEnsemble method that averages predictions from multiple decision trees to reduce overfitting and improve accuracy.Gradient Boosting RegressorBuilds models sequentially, with each tree correcting the errors of the previous ones.K-Nearest Neighbors RegressorPredicts the value by averaging the values of its $k$ nearest neighbors.📈 Model Evaluation and ResultsThe models were evaluated using Mean Squared Error (MSE) and the R-squared ($R^2$) score.ModelMSER-squaredRandom Forest82.910.9969Decision Tree120.050.9955Gradient Boosting197.280.9926Linear Regression263.100.9901K-Nearest Neighbors1186.120.9556Performance InsightThe Random Forest Regressor achieved the best performance, with the lowest MSE (82.91) and the highest R-squared score (0.9969), indicating an exceptional fit to the data for predicting the credit score.📝 Conclusion and Final VerdictThe project successfully demonstrated that machine learning can be leveraged to predict loan approval outcomes with high accuracy. The final model, the Random Forest Regressor, is highly accurate and has strong potential for real-world application in banking and financial decision-making.Future EnhancementsFine-tune the best-performing model further.Collect more balanced data, especially for low-credit applicants.Apply advanced feature engineering to capture hidden financial behavior patterns.Use cross-validation and additional ensemble techniques for even better generalization and performance.👤 Author & OrganizationName: Sayana POrganization: Entri Elevate
