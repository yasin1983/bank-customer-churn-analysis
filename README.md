# Customer Churn Prediction Project

## 📌 Overview
This project analyzes customer churn for a retail bank. It combines **SQL exploration**, **machine learning modeling in Python/Colab**, and a **Power BI dashboard** to deliver both technical insights and business actions.

## 🎯 Objectives
- Explore customer data with SQL queries  
- Build and compare machine learning models (Logistic Regression, Random Forest, XGBoost)  
- Visualize KPIs and feature importance in Power BI  
- Provide actionable recommendations to reduce churn  

## 🗂️ Workflow
1. **SQL Exploration**
   - Initial attempts to upload CSV data into SQL Server faced file path and delimiter issues.  
   - Once resolved, queries were used to calculate:
     - Total customers  
     - Number of exited customers  
     - Churn rate  
     - Churn by age group, geography, and gender  

   Example:
   ```sql
   SELECT Geography, AVG(Exited) AS ChurnRate
   FROM Customers
   GROUP BY Geography;
```
