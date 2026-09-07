# Customer Churn Prediction Project - NexAfrica ML Internship

## 🏢 1. Business Understanding & Problem Statement (Task 1)
* **What is Customer Churn?** Customer churn represents the business scenario where an existing consumer or subscriber cancels their relationship with a service provider. 
* **Business Importance:** Retaining current consumers is significantly cheaper than standard customer acquisition. High churn erodes profitability and signals issues within pricing models or product-market fit.
* **Goal of the Prediction Model:** To construct a robust binary classification model that accurately predicts individual customer churn probabilities based on account histories, tech configurations, and demographic indicators.
* **Business Utility:** Proactively flags accounts at high risk of departure, allowing customer retention units to intercept them with targeted promotions, service improvements, or contract incentives.

---

## 📊 2. Data Dictionary & Variable Schema (Task 3)
Verified layout across all features in the dataset:

| Feature | Description | Variable Type |
| :--- | :--- | :--- |
| **customerID** | Unique identifier | Categorical |
| **gender** | Consumer gender demographic | Categorical |
| **SeniorCitizen** | Indicator if customer is elderly (1, 0) | Numerical (Binary) |
| **Partner** | Marital status indicator (Yes/No) | Categorical |
| **Dependents** | Family dependency status indicator (Yes/No) | Categorical |
| **tenure** | Total active account age in months | Numerical |
| **PhoneService** | Subscription to telephone features (Yes/No) | Categorical |
| **MultipleLines** | Subscription to secondary telephone lines | Categorical |
| **InternetService** | Internet connectivity technology (DSL, Fiber, No) | Categorical |
| **OnlineSecurity** | Supplemental safety subscription | Categorical |
| **OnlineBackup** | Cloud infrastructure backup subscription | Categorical |
| **DeviceProtection**| Physical device coverage plan status | Categorical |
| **TechSupport** | Premium maintenance line enrollment status | Categorical |
| **StreamingTV** | Multi-media television streaming service status | Categorical |
| **StreamingMovies** | Multi-media cinematic streaming service status | Categorical |
| **Contract** | Customer billing structural duration terms | Categorical |
| **PaperlessBilling**| Statement configuration choice (Yes/No) | Categorical |
| **PaymentMethod** | Customer transaction processing pipeline selection | Categorical |
| **MonthlyCharges** | Regularized standard monthly customer invoice cost | Numerical |
| **TotalCharges** | Net lifetime financial value billed | Numerical |
| **Churn** | **[TARGET]** Label detailing active/left statuses | Target (Binary) |

---

## 🛠️ 3. Data Quality & Cleaning Report (Task 4)
* **Initial Rows/Columns:** 7,043 rows, 21 columns.
* **Duplicate Counts:** 0 duplicate customer IDs discovered.
* **Data Typo Resolution:** `TotalCharges` was fixed from its incorrect string classification (`object`) back into standard float values. Empty whitespaces (`" "`) belonging to 11 new customers with a `tenure` value of `0` were successfully converted to `NaN` elements and safely zeroed out (`0.0`).

---

## 🎯 4. Target Variable Distribution Profile (Task 5)
* **Class 'No' (Retained Users):** 5,174 customers (**73.46%**)
* **Class 'Yes' (Churned Users):** 1,869 customers (**26.54%**)

**Technical Note for Next Week:** Due to this pronounced ~73/27 class imbalance, standard accuracy scores will yield a false sense of model performance. We must actively prioritize optimization around **Recall** and **F1-Score** when training classifiers.

---
🔗 **Raw Dataset Link:** [Kaggle Telco Customer Churn Dataset](https://kaggle.com)
