📘 README – Telecom Customer Churn Prediction Analysis
📊 Project Overview

Customer churn is one of the biggest challenges in the telecom industry. This project focuses on analyzing telecom customer behavior, identifying churn patterns, and building a machine-learning model to predict which customers are most likely to leave.

The project combines SQL (data extraction & cleaning), Power BI (data visualization & dashboarding), and Machine Learning (churn prediction) to provide a complete end-to-end data analysis workflow.

🗂️ Tech Stack

SQL – Data cleaning, transformation, and feature preparation

Power BI – Interactive dashboards for churn insights

Python (Machine Learning) – Predictive modeling using scikit-learn

Pandas, NumPy, Matplotlib, Seaborn

Jupyter Notebook

📁 Dataset

Telecom Customer Churn dataset, containing:

Customer demographics

Subscription & service usage patterns

Billing details

Contract and tenure information

Churn label (Yes/No)

Typical columns include:
customerID, gender, tenure, MonthlyCharges, TotalCharges, Contract, PaymentMethod, InternetService, TechSupport, Churn etc.

🔧 Project Workflow
1️⃣ Data Extraction & Cleaning (SQL)

Imported raw telecom data into SQL database

Performed:

Removing duplicates

Handling missing values

Fixing datatype inconsistencies (e.g., TotalCharges)

Creating new features such as tenure groups

Queried and exported cleaned dataset into Power BI and Python for modeling

2️⃣ Exploratory Data Analysis (EDA)

Using SQL + Python:

Distribution analysis of churn vs non-churn customers

Identified churn-driving factors:

Contract type

Monthly charges

Tenure

Internet service type

Technical support availability

Correlation heatmaps & feature importance checks

3️⃣ Power BI Dashboard

Created an interactive dashboard with:

📈 Churn summary

👨‍💼 Customer demographics

📡 Service usage patterns

💳 Billing & payment behavior

🚨 High-risk customer segments

Users can filter by gender, contract type, region, service type, and more.

4️⃣ Machine Learning Model

Built a churn prediction model using Python:

Models Tested

Logistic Regression

Random Forest

XGBoost

Decision Tree

Support Vector Machine

Best Model Performance

(Example, replace with your actual score)

Accuracy: 0.82

Precision: 0.79

Recall: 0.74

F1 Score: 0.76

Key Features Influencing Churn

Monthly Charges

Contract Type

Tenure

Total Charges

Tech Support availability

Internet Service Type

📦 Project Structure
│── README.md  
│── data/  
│   └── telecom_churn_dataset.csv  
│── sql/  
│   └── churn_cleaning_queries.sql  
│── powerbi/  
│   └── churn_dashboard.pbix  
│── machine_learning/  
│   └── churn_model.ipynb  
│── images/  
│   └── dashboard_screenshot.png

🚀 How to Run the Project
Prerequisites

Python 3.8+

Power BI Desktop

MySQL / PostgreSQL / SQL Server

Required Python libraries:

pip install pandas numpy scikit-learn matplotlib seaborn xgboost

Steps

Import dataset into SQL database

Run SQL cleaning queries

Export cleaned data

Load dataset into Power BI → create visuals

Run Jupyter Notebook → train and evaluate model

Use the predictions CSV for business insights

📊 Power BI Dashboard Preview

(Add screenshot image in repo under /images)

🧠 Key Insights

Majority of churn customers are on month-to-month contracts

High monthly charges strongly correlate with churn

Customers without tech support churn more

Long-tenured customers have much lower churn rates

🏆 Business Recommendations

Offer discounts for high monthly charge customers

Push customers toward yearly contracts

Provide proactive technical support

Create retention campaigns for at-risk groups

📬 Contact

Rohit Gupta
LinkedIn: add your link here
Email: (optional)
