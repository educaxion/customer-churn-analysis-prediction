# Customer-Churn-Analysis-Prediction
End-to-End Customer Churn Analytics using SQL, Python EDA, and Random Forest Machine Learning.

# End-to-End Customer Churn Analytics & Predictive Modeling

An end-to-end data project designed to analyze customer behavior, identify key churn drivers, and build a predictive machine learning model to mitigate customer attrition.

---

## Project Overview
This project simulates an industry-standard data science workflow to solve a critical business problem: **Customer Churn**. It combines relational database analysis (SQL), visual data storytelling (Python EDA), and predictive analytics (Machine Learning) to deliver actionable insights for the business and marketing teams.

## Tech Stack & Skills Demonstrated
* **Data Manipulation:** Python (`Pandas`, `NumPy`)
* **Database Analytics:** Advanced SQL (Aggregations, Joins, Grouping)
* **Data Visualization:** `Seaborn`, `Matplotlib` (Custom annotations, styled bar plots, confusion matrix)
* **Machine Learning:** `Scikit-Learn` (`RandomForestClassifier`, `LabelEncoder`, `get_dummies`, `train_test_split`)
* **Model Evaluation:** Precision, Recall, F1-Score, Confusion Matrix, Feature Importance

---

## Key Business Insights & Findings

### 1. The Power of Discounts vs. Return Rates (SQL & EDA)

<img width="784" height="484" alt="Impactdiscount" src="https://github.com/user-attachments/assets/cc1b90fe-08ea-4d9e-a0b8-2a1c28a6c13f" />

* Through conditional SQL segmentation, we found a clear pattern between high discount usage and product return rates. Customers hunting for heavy discounts (>30%) showed higher return behavior compared to low-discount segments.

### 2. Main Drivers of Customer Churn (Machine Learning)

<img width="884" height="484" alt="top10" src="https://github.com/user-attachments/assets/855a61c4-131e-44d8-9768-1c34ede53890" />

After training the **Random Forest Classifier** model, the system revealed the top 3 behavioral features that heavily influence customer churn:
1.  **Days Since Last Purchase (Importance Score: ~0.598):** The most dominant factor. Customers who haven't made a purchase in a while have an extremely high probability of turning into churned users.
2.  **Customer Satisfaction Score (Importance Score: ~0.081):** Low ratings (1-2 stars) act as an immediate trigger for customer attrition.
3.  **Customer Lifetime Days (Importance Score: ~0.044):** Newer users are more fragile and prone to churn compared to mature, long-term loyal members.

---

## Business Recommendations
* **Automated Retargeting:** Deploy an automated email or push-notification marketing funnel triggered when a user's `days_since_last_purchase` hits a specific threshold (e.g., 14 or 30 days).
* **Proactive Customer Success:** Flag any user giving a satisfaction score below 3 stars and alert the customer support team to resolve their issues immediately before they permanently leave the platform.
* **Onboarding Optimization:** Improve the introductory experience and offer tailored benefits for customers with a low `customer_lifetime_days` score to increase initial retention.

---

## Project Structure
* `Customer_Churn_Analytics.ipynb`: The complete Google Colab containing data cleaning, SQL queries via pandasql/sqlite, custom data visualizations, preprocessing, and the finalized Random Forest model.
