# Bank Customer Churn Prediction

## Overview
This project analyzes customer behavior in banking and predicts churn using Machine Learning techniques. 
The goal is to identify high-risk customers and support business decisions for customer retention.

## Tools & Technologies
- Python (Pandas, NumPy, Scikit-learn)
- SQL
- Power BI
- Git, GitHub

## Folder Structure
/data  
/python  
/sql  
/powerbi  

---

<img src="sql/SQL_Workflow.png" alt="Workflow Diagram" width="500"/>

## Business Questions
- Which segment has the highest churn?
- What factors influence customer churn?
- Can churn be predicted using machine learning?

## Business Insights

### 1. Churn Rate by Geography
```sql
SELECT Geography,
       COUNT(*) AS TotalCustomers,
       SUM(CAST(Exited AS INT)) AS ChurnedCustomers,
       ROUND(100.0 * SUM(CAST(Exited AS INT)) / COUNT(*), 2) AS ChurnRate
FROM customers_new
GROUP BY Geography
ORDER BY ChurnRate DESC;
