# **CUSTOMER LIFETIME VALUE PREDICTION**
By: Kenshi Poneva 

I developed machine learning models to predict customers' CLV, enabling a marketing team in the online retail company to make data-driven decisions in generating marketing campaigns provided with customer segmentation aiming for efficient budget allocations.

## 1. Problem Understanding and Problem Statement

A company's marketing team is planning a new campaign and needs to allocate their budget effectively. To optimise their campaign, they need to identify customers who are likely to spend the most and those with the lowest values. This targeted approach ensures that marketing strategies are used efficiently and avoids alienating customers who are not interested.

Therefore, this project aims to develop a Machine Learning model for forecasting customers' CLV. The model's predictions will inform marketing decisions, focusing on customer retention and acquisition efforts.

## 2. Machine Learning Task

This project aims to develop a Machine Learning model to support the company's marketing efforts:

1. CLV forecasting: This model will predict the total amount of money each customer is likely to spend over a given period of time. This information can be used to allocate marketing budgets effectively.

2. Customer segmentation: This model will categorise customers into high-value, medium-value, and low-value groups based on their predicted CLV. This information can be used to develop targeted marketing strategies for each customer segment.

## 3. Analytics Approach

The following analytics approach will be used to develop the CLV forecasting model:

1. Data cleaning & preparation.
2. Feature engineering to capture customer behavior and purchase patterns.
3. Evaluate different machine learning models to find the best performing one. 
4. Hyperparameter tuning to improve model performance.
5. Evaluate and interpret the model to understand the most important factors that influence CLTV.

## 4. Expected Outcomes
The expected outcomes of this project are as follows:

1. A Machine Learning model that can predict CLV with high accuracy and group customers into correct segments.
2. A clear understanding of the most important factors that influence CLTV.
3. Concrete recommendations on how businesses can use the model to acquire and retain valuable customers.

## 5. Metric Analysis

The best metric for evaluating the performance of a machine learning model for predicting CLV is the Median Absolute Error (MedAE). Since we have a large amount of data with over 1,000,000 rows and 8 features, and the data distribution is probably not normal, MedAE is the more robust metric. This means that MedAE is less affected by outliers or large errors.
MedAE measures how close the model's predictions are to the actual CLV values. A lower MedAE indicates a better model. In this case, we are forecasting the lifetime value of customers for marketing decisions, which is a numerical value.
Note: MedAE is also aligned with our goal to minimize the error for the most valuable customers. This is because MedAE is less sensitive to large errors, which are more likely to occur for high-value customers.

## 6. Data Understanding
I am using a public dataset from the UCI Machine Learning Repository, which can be found here:  https://archive.ics.uci.edu/ml/datasets/Online+Retail+II#. 

This is a transactional data set that contains all the transactions occurring from  2009 to 2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## 7. Key Features
Here is a summary of the key features for predicting CLV:

1. The features that I will use to predict CLV are: `avgOrderValue`, `profitMargin`, `custValue`, `customerLoyalty`.
2. Since the numerical data is not normally distributed and contains outliers, I will normalise it using Robust scaler. Robust scaler is a good choice for this task because it is less sensitive to outliers.
3. I will encode the categorical features using ordinal encoding for customerLoyalty. Ordinal encoding assigns integer labels to categories in a specified order.
4. Multicollinearity is a potential concern for linear regression models. To minimize the impact of multicollinearity, I will also explore two ensemble models, Random Forest and XGBoost, which are less sensitive to multicollinearity.

## 8. Result Overview
Based on the performance of the machine learning models that have been developed, it is found that the RandomForestRegressor model performs remarkably well, producing a Median Absolute Error (MedAE) value of approximately 61,000. This signifies a very small error, especially when considering that the nominal range in the target CLV spans up to 46,177,957,508. The model's prediction speed typically ranges from 2 to 3 seconds for 2000-5000 data points, indicating fast processing.
