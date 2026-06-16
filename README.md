# Customer Churn Analysis (Telco Dataset)

i did this project to understand why customers leave a telecom company and to get some hands on practice with real data. most tutorials just focus on building models but i wanted to focus more on actually understanding the data and finding patterns that make business sense.

---

## what is this project about

basically the idea is - a telecom company is losing customers and wants to know why. so i took a real dataset (around 7000 customers) and tried to figure out which type of customers are leaving and what might be causing it.

---

## dataset

- Telco Customer Churn dataset from Kaggle (IBM sample data)
- 7043 rows, 21 columns
- has info like how long the customer has been with the company, what plan they are on, monthly charges, whether they use fiber/DSL, and whether they churned or not

---

## tools used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook
- Scikit-learn (for the ml part)

---

## what i did

**data cleaning**
- TotalCharges column was stored as text for some reason, had to convert it to numeric
- 11 rows had blank values in TotalCharges (turned out these were brand new customers with 0 tenure), filled them with 0
- converted Churn column from Yes/No to 1/0 so i could do calculations on it

**EDA**
made charts to answer specific questions like:
- how many customers actually churned? (ans: 26.5%, which is a lot)
- do new customers leave more? yes, avg tenure of churned customers is 18 months vs 37 months for people who stayed
- does contract type matter? massively - month to month customers churn at 43%, 2 year contract customers at just 3%
- do higher charges cause churn? yes, churned customers pay around $74/month vs $61 for retained ones
- senior citizens churn at almost double the rate of younger customers

one thing that surprised me was fiber optic users had the highest churn (~42%) even though its a better service. probably because its also more expensive and people dont feel its worth it.

**machine learning**
tried 4 models to see if we can predict churn:
- Logistic Regression
- Decision Tree (max_depth=5)
- Random Forest
- KNN (k=5)

random forest gave the best results. also the feature importance from RF confirmed what i found in EDA - tenure and monthly charges are the biggest factors.

---
##  Visualizations

### Churn Distribution
![Churn](images/churn_distribution.png)

### Tenure Analysis
![Tenure](images/tenure_analysis.png)

### Contract vs Churn
![Contract](images/contract_type.png)

### Key Segments
![Key_Segments](images/key_segments.png)

## main findings

- month to month contract customers = highest churn risk
- customers in first 6 months = most likely to leave
- higher monthly charges = more likely to churn
- senior citizens churn at nearly 2x rate
- gender has almost no effect on churn

---

## what the company can actually do about it

1. give discounts to push people from monthly to yearly plans
2. check in with new customers in the first 3 months before they decide to leave
3. look into why fiber optic users are unhappy, is it the price or the service quality
4. create simpler plans for senior citizens

---

## how to run

```
git clone https://github.com/your-username/customer-churn-analysis.git
cd customer-churn-analysis
jupyter notebook
```

then open `customer_churn_analysis.ipynb` and run all cells. make sure the CSV file is in the same folder.

---

## what i learned

- raw data is always messy, cleaning takes more time than expected
- accuracy alone is not a good metric when classes are imbalanced, f1 score matters more
- the EDA part is actually more useful than the model sometimes, just looking at the data tells you a lot
- its important to think about what the numbers mean for the business, not just plot graphs

---

made by Tanishq Soni



