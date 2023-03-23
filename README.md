# Loan Defaulter
This project focuses on analyzing features and risk flags associated with business loans. We aim to build statistical models and apply machine learning techniques to address the imbalance and overfitting issues in the dataset, ultimately achieving higher accuracy scores and AUC values as measured by a confusion matrix. Additionally, the developed model can help predict future loan defaulters based on the analyzed features.

## Table of Content
* [Features](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#Features)
* [Get Started](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#Get-Started)
* [Contributors](https://github.com/Weijia-Wang341/Loan_Defaulter/blob/main/README.md#contributors)

## Features
The data analysis will provide:
* Logistic Regression
* Decision Trees
* Confusion Matrix
* AUC-ROC Curve

## Get Started
1. Data Cleaning:
    - One-hot endcoing: The dataset contains both numerical and categorical columns. To convert categorical values into numerical values, apply *OneHotEncoder()* to columns such as 'Married_Single', 'House_Ownership', 'Car_Ownership', 'Profession', 'CITY', and 'STATE'.
    - SMOTE: The dataset has imbalanced data of faulters and non-faulters. To improve the model's accuracy, balance the data using *SMOTE()* for oversampling.
    
2. Modeling:
    - Logistic Regression
    - Random Forest

3. Model Evaluation:
    - Confusion Matrix
    - AUC-ROC Curve

## Contributors
* Weijia Wang
* Barry Yu
* Giani Kurniawan
