
# Predicting Customer Attrition for strategic Retention
![download](https://github.com/user-attachments/assets/f229867b-20ba-4922-a46d-4ba294cd3ad8)\
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
The data is in .xlsx format with the following features:

| Feature Name               | Description                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| CustomerID                 | Unique customer ID                                                                 |
| Churn                      | Flag indicating whether the customer churned (1) or not (0)                        |
| Tenure                     | Tenure of the customer in the organization                                          |
| PreferredLoginDevice       | The preferred device used by the customer to log in (e.g., mobile, web)            |
| CityTier                   | City tier classification (e.g., Tier 1, Tier 2, Tier 3)                            |
| WarehouseToHome            | Distance between the warehouse and the customer’s home                             |
| PreferredPaymentMode       | Preferred payment method used by the customer (e.g., credit card, debit card, cash on delivery) |
| Gender                     | The gender of the customer                                                         |
| HourSpendOnApp             | Number of hours spent on the mobile application or website                         |
| NumberOfDeviceRegistered   | Total number of devices registered to the customer’s account                       |
| PreferedOrderCat           | Preferred order category of the customer in the last month                         |
| SatisfactionScore          | Customer’s satisfaction score with the service                                     |
| MaritalStatus              | Marital status of the customer                                                     |
| NumberOfAddress            | Total number of addresses added to the customer’s account                          |
| OrderAmountHikeFromlastYear| Percentage increase in order value compared to last year                           |
| CouponUsed                 | Total number of coupons used by the customer in the last month                     |
| OrderCount                 | Total number of orders placed by the customer in the last month                    |
| DaySinceLastOrder          | Number of days since the customer’s last order                                     |
| CashbackAmount             | Average cashback received by the customer in the last month                        |

[Dataset source](https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction/data)

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

Metrics used:\
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

#### Application Input Interface
<img width="894" alt="app_index" src="https://github.com/AllanOuko/customer-churn-prediction-application/assets/83907520/e5be6059-f61b-4bf2-88c5-d3da29734bc9">

#### Application Results Interface
<img width="863" alt="app_results" src="https://github.com/AllanOuko/customer-churn-prediction-application/assets/83907520/e967352b-fc5f-4f34-8baa-1dc867d57f4c">
