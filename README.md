#  Customer Churn Analysis & Insights (Telco Dataset)

##  Project Overview

I built this project to understand why customers leave a service and to practice turning raw data into business decisions.

The focus is on identifying high-risk segments and generating actionable insights rather than just predicting churn.
---

##  Business Objective

* Identify **key drivers of churn**
* Detect **high-risk customer segments**
* Provide **data-driven recommendations** to improve retention

---

##  Dataset Details

* Dataset: Telco Customer Churn (IBM Sample Dataset)
* Source: Kaggle
* Records: **7043 customers**
* Features: **21 columns** including:

  * Customer demographics
  * Service usage (Internet, Streaming, etc.)
  * Account information (tenure, contract type)
  * Billing details (monthly & total charges)
  * Target variable: **Churn (Yes/No)**

---

##  Tech Stack

* **Python**
* **Pandas & NumPy** – data manipulation
* **Matplotlib & Seaborn** – data visualization
* **Jupyter Notebook**

---

##  Data Cleaning & Preparation

* Converted `TotalCharges` from string → numeric
* Handled missing values using coercion + filling
* Created **Churn_Binary (1/0)** for analysis
* Engineered readable features like:

  * `SeniorCitizen_Label`

---

##  Exploratory Data Analysis (EDA)

###  Overall Churn

* **26.5% customers churned (1869 out of 7043)**
* Indicates a significant business problem

---

###  Tenure Analysis

* Avg tenure (Churned): **18.0 months**
* Avg tenure (Retained): **37.6 months**
*  **Insight:** Highest churn occurs in the **first 1–5 months**

---

###  Pricing Impact

* Avg monthly charge (Churned): **$74.44**
* Avg monthly charge (Retained): **$61.27**
*  **Insight:** Higher-paying customers are more likely to churn

---

###  Contract Type

* Month-to-month customers have **highest churn rate**
* Long-term contracts significantly reduce churn
*  **Insight:** Contract commitment improves retention

---

###  Internet Service

* **Fiber optic users churn the most (~42%)**
*  **Insight:** High price or service expectations may not be met.
  
 One interesting observation was that fiber optic users had the highest churn (~42%), which initially seemed counterintuitive since it's a premium service. This suggests a gap between pricing and perceived value.

---

###  Customer Demographics

* Senior citizens churn at **~2x higher rate**
* Gender shows **no significant impact**

---

##  Key Findings Summary

High-risk segments:

* Customers with **tenure < 6 months**
* **Month-to-month contracts**
* **Fiber optic users**
* **Senior citizens**

Overall churn rate: **26.5%**

---

##  Business Recommendations

1. Encourage **long-term contracts** with discounts
2. Improve **early-stage onboarding (first 3 months)**
3. Introduce **pricing optimization / mid-tier plans**
4. Investigate **fiber optic service quality & support**
5. Provide **dedicated support for senior citizens**

---

##  Key Learning Outcomes

* Real-world data cleaning challenges
* Feature engineering for analysis
* Business-driven EDA approach
* Translating data insights into actionable strategies

---

## Challenges Faced

* The `TotalCharges` column was stored as text and required careful conversion to numeric while handling missing values.
* Interpreting business meaning from raw patterns (not just plotting graphs) was a key learning step.

---

##  How to Run

```bash
git clone https://github.com/your-username/customer-churn-analysis.git
cd customer-churn-analysis
jupyter notebook
```

---

##  Project Highlights

* End-to-end data analysis workflow
* Strong focus on **business insights (not just code)**
* Uses real-world telecom dataset
* Clear storytelling with data

---

##  Author

**Tanishq Soni**
Aspiring Data Scientist
