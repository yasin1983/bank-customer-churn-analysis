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

2.   **Python & Colab Modeling**

Data preprocessing and dummy encoding

Model training with Logistic Regression, Random Forest, and XGBoost

Evaluation using Accuracy, Precision, Recall, F1, and AUC

Feature importance extracted for each model

3. **Power BI Dashboard**

KPI cards: Accuracy, AUC, F1, Churn Rate, Exited Customers

Model performance comparison (bar chart + table)

Feature importance visualization

Segment-based churn analysis (Age, Geography)

Business actions section with recommendations
