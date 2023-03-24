# Loan Defaulter
This project focuses on analyzing features and risk flags associated with business loans. We aim to build statistical models and apply machine learning techniques to address the imbalance and overfitting issues in the dataset, ultimately achieving higher accuracy scores and AUC values as measured by a confusion matrix. Additionally, the developed model can help predict future loan defaulters based on the analyzed features.

## Table of Content
* [Features](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#Features)
* [Get Started](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#Get-Started)
* [Conclusion](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#Conclusion)
* [Contributors](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#contributors)

## Features
The data analysis will provide:
* Logistic Regression
* XGBoost
* Hyperparameter Tunning
* Confusion Matrix (Precision, Accuracy, Recall, F1, AUC-ROC Curve)
* Pipeline
* SMOTE
* K-Fold Cross Validation

## Get Started
1. Data Preparation:
    - Data cleaning: removing missing, values, handle outliers, etc.
    - One-hot endcoing: The dataset contains both numerical and categorical columns. To convert categorical values into numerical values, apply *OneHotEncoder()* to columns such as 'Married_Single', 'House_Ownership', 'Car_Ownership', 'Profession', 'CITY', and 'STATE'.
    - SMOTE: The dataset has imbalanced data of faulters and non-faulters. To improve the model's accuracy, balance the data using *SMOTE()* for oversampling.
    
2. Model Building:
    - Logistic Regression: We use the *LogisticRegression* class from the *sklearn.linear_model* library to build a logistic regression model. To improve the model performance, we tune hyperparameters such as the regularization strength and solver type using techniques such as grid search or randomized search. We then use the best hyperparameters to train the final logistic regression model.
    - XGBoost: We use the *XGBClassifier* class from the *xgboost* library to build an XGBoost model. To optimize the model's performance, we tune hyperparameters such as the learning rate, maximum depth, and number of estimators using techniques such as grid search or randomized search. We then use the best hyperparameters to train the final XGBoost model.

3. Pipeline Construction:
    - We import the *Pipeline* class from the *imblearn.pipeline* library to ensure that SMOTE is only applied to the training dataset during cross-validation and that there is no data leakage to the test data. By using the pipeline, we can encapsulate the steps of balancing the training data using SMOTE, fitting the model, and performing cross-validation, thus ensuring that the steps are strictly followed in the correct order. This helps us to obtain reliable estimates of the model's performance and avoid overfitting to the training data.
    
5. Model Evaluation:
    - Cross validation: We employ K-fold cross-validation to identify the optimal C by minimizing the mean squared error. To perform 5-fold cross-validation, we import *KFold* from *sklearn.model_selection*.
    - Confusion Matrix: We use *confusion_matrix* from *sklearn.metrics* to evaluate the model's performance. As this is a business loan defaulter model, we prioritize achieving a high Recall score.

## Conclusion
The Logistic Regression model evaluation reveals underperformance in terms of Accuracy, Recall, Precision, and F1 Score. Consequently, we shift to a nonlinear model, XGBoost, to build a more effective model. After determining the best parameter C, we construct an XGBoost model with an 85% Recall and 93% AUC score.

## Contributors
* Weijia Wang
* Barry Yu
* Giani Kurniawan
