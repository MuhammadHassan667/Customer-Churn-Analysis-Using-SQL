# Customer-Churn-Analysis-Using-SQL

This project analyzes customer churn patterns using SQL and the Telco Customer Churn dataset. It was built entirely using Python (Pandas, SQLite) in Google Colab, without any external databases or tools. The goal is to identify factors contributing to churn and quantify the potential revenue loss from customer departures.

## 🔍 Dataset
- Source: [Telco Customer Churn – Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Size: ~7,000 rows, 21 columns
- Fields: Customer ID, Contract Type, Monthly Charges, Tenure, Total Charges, Churn (Yes/No), etc.

## 🛠 Tools Used
- Python (Pandas, SQLite3)
- Google Colab
- SQL for data manipulation and analysis

## 🧪 Key SQL Techniques
- `CASE WHEN`, `GROUP BY`, `JOIN`
- `AVG()`, `SUM()`, `ROUND()`, `COUNT()`
- Window functions (optional)
- In-memory database via SQLite

## 📈 Key Insights
- **Churn is highest among Month-to-Month contract users**
- **Customers with higher monthly charges are more likely to churn**
- **Senior citizens churn at a slightly higher rate**
- **Estimated revenue lost due to churn exceeds $2M**

## 📌 Example Queries
```sql
SELECT
  Contract,
  ROUND(AVG(MonthlyCharges), 2) AS avg_monthly_bill,
  ROUND(AVG(TotalCharges), 2) AS avg_total_bill
FROM customers
WHERE Churn = 'Yes'
GROUP BY Contract;


## 📦 How to Run This Project
1. Open [Google Colab] (https://colab.research.google.com/drive/148lU1cs5WCnFDgAl2Rtcn0mZNkzxQWKD?usp=drive_link))
2. Upload `WA_Fn-UseC_-Telco-Customer-Churn.csv`
3. Run the provided `.ipynb` notebook
4. View insights and run additional SQL queries using `pd.read_sql_query(...)`

## 🧾 Business Use Case
- Helps subscription-based companies understand what factors contribute to customer churn.
- Supports customer retention strategies by identifying at-risk segments.
- Can be extended to include churn prediction models using machine learning.

## 👨‍💻 Author
**MUHAMMAD HASSAN** – MSc Data Analytics  
 [muhammad2297hassan@gmail.com](#)

