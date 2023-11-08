Customer Churn Prediction Project
Overview

This project focuses on predicting customer churn for a telecom company. Using a dataset with various customer features, we conducted exploratory data analysis (EDA), preprocessed the data, and applied machine learning models to identify customers who are at high risk of churning.
Data Description

The dataset for this project comprises several customer attributes, including account details, usage statistics, and charges. Key features include account length (AccountWeeks), contract status (ContractRenewal), data plan subscription (DataPlan), data usage (DataUsage), customer service interaction (CustServCalls), daily usage metrics (DayMins, DayCalls), financial charges (MonthlyCharge, OverageFee), and roaming minutes (RoamMins).
Exploratory Data Analysis (EDA)
Churn Distribution

We analyzed the distribution of churn to understand the proportion of customers who have left the company. This initial analysis showed an imbalance in the dataset, with fewer instances of churned customers.
Customer Service Calls Distribution

A key observation was that customers with more customer service calls tend to churn more often, indicating potential issues with service satisfaction.
Correlation Heatmap

The correlation analysis revealed that certain features such as MonthlyCharge and CustServCalls had a stronger relationship with churn, hinting at their potential as predictive indicators.
Deep Analysis on KPIs

We conducted a deeper analysis by focusing on various KPIs relevant to churn, such as:

    Churn Rate: The overall percentage of customers who have churned.
    Average Revenue Per User (ARPU): A financial metric representing the average monthly revenue generated per user.
    Customer Service Contact Rate: The average number of customer service calls by churn status.
    Customer Lifetime Value (CLV): The total revenue expected from a customer over their tenure with the company.
    Data Usage: The average data consumption by churn status.
    Overage Fee: The average additional fee incurred by customers for exceeding their plan limits.

This analysis provided valuable insights into the factors influencing churn, such as service dissatisfaction and pricing sensitivity.
Predictive Modeling
Logistic Regression Model

We started our predictive modeling with a logistic regression model. The model's performance metrics were as follows:

    Accuracy: Approximately 85.91%, suggesting a relatively high level of overall prediction correctness.
    Precision and Recall: The model had high precision for non-churn predictions but significantly lower for churn predictions.
    ROC-AUC Score: At about 0.58, the model showed moderate ability to distinguish between the churned and retained customers.

Given the modest recall and ROC-AUC score, particularly for identifying churned customers, the logistic regression model was deemed less than ideal.
Random Forest Model

We then moved to a Random Forest model, which yielded a substantial improvement:

    Accuracy: Increased to approximately 93.10%.
    Precision and Recall: Both metrics saw improvements, particularly recall for churned customers, which is crucial for a churn prediction model.
    ROC-AUC Score: Improved to 0.80, indicating a better distinction between churned and retained customers.

Feature Importance Analysis

Feature importance from the Random Forest model highlighted MonthlyCharge, DayMins, and CustServCalls as top predictors. This suggests that financial factors and customer service experience play significant roles in churn.
Key Insights

    Service Calls: A higher number of customer service calls correlates with an increased likelihood of churn.
    Pricing Sensitivity: Monthly charges are a significant predictor of churn, indicating that customers are sensitive to pricing.
    Usage Patterns: Customers with lower data usage are more likely to churn, suggesting underutilization or mismatched service plans.

Recommendations

Based on the insights from the models, we propose the following strategic actions to reduce customer churn:

    Pricing Review: Reevaluate the current pricing plans to ensure competitiveness and consider introducing loyalty discounts.
    Service Improvement: Enhance the quality of customer service to reduce the frequency of service calls related to complaints.
    Custom Data Plans: Offer personalized data plans for low-usage customers to increase the perceived value of services.
    Fee Transparency: Improve communication around overage fees and implement alerts to inform customers before they incur additional charges.

Conclusion

This project provides a comprehensive approach to understanding and predicting customer churn. The insights and recommendations can assist the telecom company in implementing effective retention strategies. For future work, we can explore additional models, feature engineering, and deployment strategies for real-time churn prediction.
Project Structure

    EDA.ipynb: Jupyter notebook containing exploratory data analysis.
    Modeling.ipynb: Jupyter notebook for training and evaluating models.
    dataset.csv: The dataset used for the analysis.
    requirements.txt: Required libraries for reproducing the analysis.
