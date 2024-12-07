
# Predicting Customer Attrition for strategic Retention
![download](https://github.com/user-attachments/assets/54410f19-8440-49ba-a8fc-b5f9750da2a7)\
This repository contains a complete pipeline for building and deploying a Customer Churn Prediction model using machine learning techniques. The project uses a dataset of customer interactions with an e-commerce company and provides insights into the likelihood of customers canceling their subscription or service.

**Table of Contents**\
•	Introduction\
•	Why Predict Customer Churn?\
•	Dataset\
•	Data Preprocessing\
•	Model Training and Evaluation\
•	Model Deployment\
•	Results\
•	Acknowledgements


**Introduction**\
Customer churn prediction helps businesses identify customers at risk of leaving their service. This project demonstrates how to use historical customer data to predict churn and implement strategies for customer retention.

**Why Predict Customer Churn?**\
Customer retention is more cost-effective than acquiring new customers. Predicting churn enables businesses to launch targeted marketing campaigns and implement strategies to improve customer satisfaction. For example, an Internet Service Provider (ISP) can use this model to retain customers and maintain revenue stability.

**Dataset**\
The dataset is sourced from Kaggle and includes features such as:

•	Customer demographics\
•	Product usage patterns\
•	Payment preferences\
•	Churn status\
The data is in .xlsx format and contains no duplicate rows.

**Data Preprocessing**\
The data preprocessing pipeline includes:

1. Handling Missing Values:
•	Numerical columns: Imputed with mean values.\
•	Categorical columns: Converted to one-hot encoding.\
•	Random Forest Iterative Imputer applied for final imputation.

2. Splitting Data:
•	Training and testing datasets split in an 80:20 ratio.

3. Balancing Classes:
•	Synthetic Minority Over-sampling Technique (SMOTE) used to balance the target variable (churn).

**Model Training and Evaluation**\
The following classification models were evaluated:
1. XGBoost Classifier (Best performer)
2. Random Forest
3. Logistic Regression

Metrics used:
•	Accuracy\
•	F1-Score

Final Model:\
The XGBoost classifier achieved the highest performance and was selected for deployment.

**Model Deployment**\
The final model and its dependencies were saved for deployment:

•	Model saved as a .pkl file.\
•	Data columns saved in a .json file.
The deployment uses Flask to create an API for predictions.

**Results**\
***Feature Importance***\
The top contributing features include:

•	Tenure\
•	Cashback amount\
•	Satisfaction score\
•	Order amount hike from last year\
•	Number of devices registered

***Model Performance***\
Accuracy: 0.993\
F1-Score: 0.979


**Acknowledgements**\
•	Dataset from Kaggle\
•	SMOTE implementation from imbalanced-learn\
•	Flask for deployment

