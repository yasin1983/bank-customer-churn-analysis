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

- Data preprocessing and dummy encoding
- Model training with Logistic Regression, Random Forest, and XGBoost
- Evaluation using Accuracy, Precision, Recall, F1, and AUC
- Feature importance extracted for each model

3. **Power BI Dashboard**

- KPI cards: Accuracy, AUC, F1, Churn Rate, Exited Customers
- Model performance comparison (bar chart + table)
- Feature importance visualization
- Segment-based churn analysis (Age, Geography)
- Business actions section with recommendations

4. ## 📊 Models Used
- Logistic Regression  
- Random Forest  
- XGBoost  

5. ## 📈 Model Performance
| Model              | Accuracy | Precision | Recall | F1   | AUC  |
|--------------------|----------|-----------|--------|------|------|
| Logistic Regression| 0.79     | 0.29      | 0.06   | 0.10 | 0.74 |
| Random Forest      | 0.87     | 0.75      | 0.46   | 0.57 | 0.85 |
| XGBoost            | 0.87     | 0.72      | 0.49   | 0.59 | 0.84 |

6. ## 🔑 Key Features (Feature Importance)
- **Age** → most critical factor (especially for Random Forest)  
- **NumOfProducts** → strongest predictor in XGBoost  
- **IsActiveMember** → significant impact on churn  
- **Geography_Germany** and **Gender_Male** → appear due to dummy encoding  

7. ## 📊 Dashboard Highlights
- KPI cards: Accuracy, AUC, F1, Churn Rate, Exited Customers  
- Model performance comparison charts  
- Feature importance visualization  
- Segment-based churn analysis (Age groups, Geography)  
- Business actions: identify high-risk segments, implement loyalty programs, cross-sell strategies  

8. ## ⚙️ Technologies
- Python (EDA, modeling)  
- Scikit-learn (machine learning)  
- Power BI (dashboard visualization)  
- Google Colab (development environment)  

9. ## 🚀 How to Run
   1. Open `notebooks/model_comparison.ipynb` in Colab or Jupyter Notebook.  
   2. Load the dataset from `data/churn_data.csv`.  
   3. Train and evaluate the models.  
   4. Explore the Power BI dashboard (`powerbi/dashboard.pbix`).  

10. ## 📌 Business Insights
- Churn rate: **20.37%**  
- Total exited customers: **2037**  
- Best performing models: Random Forest / XGBoost (Accuracy ≈ 0.87, AUC ≈ 0.85)  
- Recommended actions: loyalty programs for high-risk segments, encourage product diversification, promote active membership.  

---

👨‍💻 Author: **Yasin Karadag**  
📍 Vienna, Austria  

