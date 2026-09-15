# Customer-Churn-Predict Using Machine Learning
# 📊 Customer Churn Prediction & Analysis

An end-to-end **Customer Churn Prediction and Analysis** project using **Python, SQL, Machine Learning, and Power BI**.

The project focuses on analyzing customer behavior, identifying factors associated with churn, predicting customers who are likely to churn, and presenting business insights through an interactive Power BI dashboard.

---

## 🎯 Project Objective

The main objectives of this project are:

- Analyze customer churn patterns
- Identify important factors affecting customer churn
- Perform data cleaning and exploratory data analysis
- Use SQL for customer and churn analysis
- Build a Machine Learning model to predict customer churn
- Evaluate the ML model using appropriate performance metrics
- Create an interactive Power BI dashboard
- Generate actionable business insights for customer retention

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **SQL**
- **Power BI**
- **DAX**
- **Jupyter Notebook**

---

# 🔄 Project Workflow

```text
Raw Customer Data
       ↓
Data Cleaning using Python
       ↓
Exploratory Data Analysis
       ↓
SQL Data Analysis
       ↓
Feature Engineering
       ↓
Machine Learning
       ↓
Churn Prediction
       ↓
Power BI Dashboard
       ↓
Business Insights

# 🐍 1. Python – Data Cleaning & EDA

Python was used for:
Loading the dataset
Understanding the data
Handling missing values
Converting data types
Removing/handling inconsistent values
Exploratory Data Analysis
Data visualization
Feature preparation
Libraries used:
Pandas
NumPy
Matplotlib
Seaborn
## 🗄️ 2. SQL – Customer Churn Analysis

SQL was used to perform:
Total customer analysis
Churned customer analysis
Churn rate calculation
Contract-wise churn analysis
Internet-service-wise churn analysis
Payment-method-wise churn analysis
Average monthly charges analysis
Average total charges analysis
Example Query
        SELECT
            Contract,
            COUNT(*) AS Total_Customers,
            SUM(
                CASE
                    WHEN Churn = 'Yes' THEN 1
                    ELSE 0
                END
            ) AS Churned_Customers
        FROM customer
        GROUP BY Contract;
## 🤖 3. Machine Learning – Churn Prediction

Machine Learning was used to predict whether a customer is likely to churn.
ML Workflow
Cleaned Data
     ↓
Feature Selection
     ↓
Categorical Encoding
     ↓
Train-Test Split
     ↓
Feature Scaling
     ↓
Model Training
     ↓
Prediction
     ↓
Model Evaluation

## Features Used

Important customer attributes include:
Tenure
Contract
Internet Service
Payment Method
Monthly Charges
Total Charges
Online Security
Tech Support
Partner
Dependents
Senior Citizen
Models
The project can use and compare:
Logistic Regression
Decision Tree
Random Forest
Example
        from sklearn.model_selection import train_test_split
        from sklearn.linear_model import LogisticRegression

        X_train, X_test, y_train, y_test = train_test_split(
            X, y,
            test_size=0.2,
            random_state=42
        )
        
        model = LogisticRegression(max_iter=1000)
        
        model.fit(X_train, y_train)
        
        y_pred = model.predict(X_test)

## Model Evaluation

The model is evaluated using:
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Accuracy
Precision
Recall
F1-Score

## Confusion Matrix

The final model should be selected based on the business objective and model performance rather than accuracy alone.

📊 4. Power BI Dashboard
Power BI was used to create an interactive dashboard for customer churn analysis.

Dashboard KPIs
Total Customers
Churned Customers
Churn Rate %
Average Monthly Charges
Dashboard Visuals
Churn by Contract
Churn by Internet Service
Churn by Payment Method
Gender-wise Churn
Customer tenure analysis
Monthly Charges analysis
Interactive slicers
Slicers
Contract
Internet Service
Payment Method
Gender
Senior Citizen
📈 DAX Measures
Total Customers
Total Customers =
COUNTROWS('customer')
Churned Customers
Churned Customers =
CALCULATE(
    COUNTROWS('customer'),
    'customer'[Churn] = "Yes"
)
Churn Rate
Churn Rate % =
DIVIDE(
    [Churned Customers],
    [Total Customers],
    0
)
Average Monthly Charges
Avg Monthly Charges =
AVERAGE('customer'[MonthlyCharges])

💡 Business Insights
The project helps businesses understand:
Which contract types have higher churn
Which payment methods are associated with higher churn
How internet services relate to churn
Whether monthly charges differ between churned and retained customers
How customer tenure affects churn
Which customers may require retention strategies
Machine Learning adds a predictive layer by identifying customers who may be at higher risk of churn.

🎓 Skills Demonstrated
Python | SQL | Machine Learning | Power BI | DAX | Pandas | NumPy | Scikit-learn | Data Cleaning | EDA | Data Visualization | Predictive Analytics | Business Analysis
👩‍💻 Author
Poonam Rajora
B.Tech | Aspiring Data Analyst
