# 📘 Telecom Customer Churn Prediction

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)]()\
[![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)]()\
[![SQL](https://img.shields.io/badge/SQL-Data%20Cleaning-orange)]()\
[![Machine
Learning](https://img.shields.io/badge/ML-Classification-green)]()\
[![Status](https://img.shields.io/badge/Project%20Status-Completed-brightgreen)]()\
[![License](https://img.shields.io/badge/License-MIT-red)]()

## 📊 **Project Goal**

Telecom companies lose millions due to customer churn. This end-to-end
project predicts which customers are most likely to leave. This project
main goal is to create an entire ETL process in a database & a Power BI dashboard
to utilize the Customer Data and acheive below goals:

-   **Analyze Customer Data at below levels** -> Demographic\Geographic\Payment & Account Info\Services
-   **SQL** → ETL, cleaning, transformation\
-   **Power BI** → Interactive churn analysis dashboard\
-   **Machine Learning** → Predictive churn model\Random Forest

The goal is to help businesses identify churn drivers and take action to
improve customer retention.

## 🛠️ **Tech Stack**

  Component          Tools Used
  ------------------ ----------------------------------------
  Data Cleaning      SQL Server
  Visualization      Power BI
  Machine Learning   Python (Pandas, Scikit-Learn, XGBoost)
  Notebook           Jupyter
  Plotting           Matplotlib, Seaborn
  Deployment         GitHub

## 🗂️ **Dataset**

Telecom Customer Churn dataset includes 
Customer_Id,demographics:{Age,Gender,Married,State},Refferals & Services:{Number_of_Refferals,Tenure_in_Months,Value_Deal,Phone_service,Multiple_lines,Internet_Service,Internet_Type,Online_Security,Online_backup,Device_Priotection_Plan,
Premium_Support,Streaming_TV,Streaming_Movies,Streaming_Music,Unlimited_Data,Contract,Paperless_Billing},Payment_&_Revenue_Related_Columns:{Payment_method,Monthly_Charge,Total_charges,Total_Refunds,Total_extra_Data_Charges,Total_Long_Distance_Charges,Total_Revenue},Customer_status_Columns:{Customer_Status,Churn_Category,Churn_Reason}.

## 🔧 **Workflow**

### **1️⃣ Data Preparation (SQL)**

Performed data cleaning, transformation, and feature engineering.

### **2️⃣ Exploratory Data Analysis**

Analyzed churn drivers and customer behavior.

### **3️⃣ Power BI Dashboard**

Includes churn summary, demographics, billing insights, and service
patterns.

### **4️⃣ Machine Learning Model**

Tested multiple models like Logistic Regression, Random Forest,
SVM.

Example model scores (replace with your own):

  Metric      Score
  ----------- ---------
  Accuracy    **82%**
  Precision   **79%**
  Recall      **74%**
  F1 Score    **76%**

## 🧠 **Key Insights**

-   High monthly charges strongly correlate with churn\
-   Month-to-month contract users churn the most\
-   Long-tenure customers rarely churn\
-   Lack of tech support increases churn probability

## 🏆 **Business Recommendations**

-   Offer discounts for high-billing customers\
-   Promote annual/long-term plans\
-   Improve tech support accessibility\
-   Improve fiber optic service quality

## 📁 **Project Structure**

    📦 Telecom-Churn-Prediction
    │── README.md
    │── data/
    │── sql/
    │── powerbi/
    │── machine_learning/
    │── images/

## 🚀 **How to Run the Project**

### Install Dependencies

    pip install pandas numpy scikit-learn seaborn matplotlib xgboost

## 📬 **Contact**

**Rohit Gupta**\
Data Analyst  
📧 Email: rohitgupta12380@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/rohitgupta0079/)
