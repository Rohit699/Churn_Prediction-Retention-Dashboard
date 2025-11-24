# 📘 Telecom Customer Churn Prediction

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)]()\
[![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)]()\
[![SQL](https://img.shields.io/badge/SQL-Data%20Cleaning-orange)]()\
[![Machine
Learning](https://img.shields.io/badge/ML-Classification-green)]()\
[![Status](https://img.shields.io/badge/Project%20Status-Completed-brightgreen)]()


## 📊 **Project Goal**

Telecom companies lose millions due to customer churn. This end-to-end
project predicts which customers are most likely to leave. This project
main goal is to create an entire ETL process in a database & a Power BI dashboard
to utilize the Customer Data and acheive below goals:


-   **Analyze Customer Data** → Demographic,Geographic,Payment & Account Info,Services
-   **Study Churner Profile & Identify Areas For Implementing Market Campaigns**
-   **Identify a Method to Predict Future Churners**

The goal is to help businesses identify churn drivers and take action to
improve customer retention.
    
# 🛠️ **Methodology & Tech Stack**
-   **SQL** → ETL, cleaning, transformation\
-   **Power BI** → Interactive churn analysis dashboard\
-   **Machine Learning** → Predictive churn model\Random Forest


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
-  **Customer_Id**
-  **Demographics & Geographics**
- Age
- Gender
- Married
- State
-  **Refferals & Services**
- Number_of_Refferals
- Tenure_in_Months
- Value_Deal
- Phone_service
- Multiple_lines
- Internet_Service
- Internet_Type
- Online_Security
- Online_backup
- Device_Priotection_Plan
- Premium_Support
- Streaming_TV
- Streaming_Movies
- Streaming_Music
- Unlimited_Data
- Contract
- Paperless_Billing
-  **Payment_&_Revenue_Related_Columns**
- Payment_method
- Monthly_Charge
- Total_charges
- Total_Refunds
- Total_extra_Data_Charges
- Total_Long_Distance_Charges
- Total_Revenue
-  **Customer_status_Columns**
- Customer_Status
- Churn_Category
- Churn_Reason

## 🔧 **Workflow**

### **1️⃣ Data Preparation (SQL Server)**
<img width="661" height="596" alt="image" src="https://github.com/user-attachments/assets/5721e381-f87c-417d-8ab0-dcbfbc0bf423" />

Loading the data from the source file. For this purpose, we are using Microsoft SQL Server(Data Warehouse) as it is widely used for solutions across the industry, and  because a full-fledged database system is better at handling recurring data loads and maintaining data integrity compared to an Excel file.
# ** Steps **
Create Database/ Create Table/ Load Data
Extraction of data, performing data cleaning, transformation, and feature engineering.

### **2️⃣ Exploratory Data Analysis**

Analyzed the columns, ie, Strength, demographics, geographics, services, churn drivers, and customer behavior.

### **3️⃣ Power BI Dashboard**

Includes Churn Analysis summary, demographics, billing insights, service
patterns, and churn rate on different parameters.

### **4️⃣ Machine Learning Model**

Tested the machine learning model, i.e, Random Forest to predict future churners

Random Forest model scores :

  Metric      Score
  ----------- ---------
  Accuracy    **85%**
  Precision   **87%**
  Recall      **94%**
  F1 Score    **90%**

### **5️⃣ Churn Prediction Power BI Dashboard**

Includes Future Churners Prediction, risk customers(who are likely to churn in upcoming future),and churn number based on different parameters.
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
├── README.md
├── Churn_Prediction_Report.pdf
│
├── notebooks/                  # Jupyter notebooks
│   ├── Churn_Prediction.ipynb
├── Dataset/                    # Used Dataset
│   ├──Original_dataset.csv
│   ├──Prediction.csv
├── dashboard/                  # Power BI dashboard file
│   └── vendor_performance_dashboard.pbix

## 🚀 **How to Run the Project**

### Install Dependencies

    pip install pandas numpy scikit-learn seaborn matplotlib 

## 📬 **Contact**

**Rohit Gupta**\
Data Analyst  
📧 Email: rohitgupta12380@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/rohitgupta0079/)
