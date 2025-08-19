# Churn_Prediction-Retention-Dashboard
Form a dashbord for churn customers and also use Machine Learning to predict the churned customer and formed another dashboard represented future churned customers 

In today’s competitive business environment, retaining customers is crucial for long-term success. Churn analysis is a key technique used to understand and reduce this customer attrition. It involves examining customer data to identify patterns and reasons behind customer departures. By using advanced data analytics and machine learning, businesses can predict which customers are at risk of leaving and understand the factors driving their decisions. This knowledge allows companies to take proactive steps to improve customer satisfaction and loyalty.

Who is the Target Audience

Although this project focuses on churn analysis for a telecom firm, the techniques and insights are applicable across various industries. From retail and finance to healthcare and beyond, any business that values customer retention can benefit from churn analysis. We will explore the methods, tools, and best practices for reducing churn and improving customer loyalty, transforming data into actionable insights for sustained success.

Project Target
Create an entire ETL process in a database & a Power BI dashboard to utilize the Customer Data and achieve below goals:
Visualize & Analyse Customer Data at below levels
Demographic
Geographic
Payment & Account Info
Services
Study Churner Profile & Identify Areas for Implementing Marketing Campaigns
Identify a Method to Predict Future Churners

Metrics Required
Total Customers
Total Churn & Churn Rate
New Joiners

STEP 1 – ETL Process in SQL Server
So the first step in churn analysis is to load the data from our source file. For this purpose we will be using Microsoft SQL server because it is a widely used solution across the industry and also because a full-fledged Database System is better at handling recurring data loads and maintaining data integrity compared to an excel file.

Creating Database

After installation, you will land on the following screen. Do remember to copy paste the server name somewhere because we will need this at a later stage. Also enable the checkbox which says “Trust Server Certificate” and then click on Connect

Once connected, click on NEW QUERY button at the top ribbon and then write below query. This will create a new Database named db_Churn

CREATE DATABASE db_Churn
Import csv into SQL server staging table – Import Wizard
Right click on the newly created database in the explorer window and then go to
Task >> Import >> Flat file >> Browse CSV file

Remember to add customerId as primary key and allow nulls for all remaining columns. This is done to avoid any errors while data load. Also make sure to change the datatype where it say Bit to Varchar(50). We are doing this because while using import wizard I faced issues with the BIT data type, however Varchar(50) works fine.
Data Exploration – Check Distinct Values

SELECT Gender, Count(Gender) as TotalCount,
Count(Gender)  1.0 / (Select Count() from stg_Churn)  as Percentage from stg_Churn Group by Gender
 
SELECT Contract, Count(Contract) as TotalCount,
Count(Contract)  1.0 / (Select Count() from stg_Churn)  as Percentage from stg_Churn Group by Contract
 
SELECT Customer_Status, Count(Customer_Status) as TotalCount, Sum(Total_Revenue) as TotalRev,
Sum(Total_Revenue) / (Select sum(Total_Revenue) from stg_Churn) * 100  as RevPercentage from stg_Churn Group by Customer_Status
 
SELECT State, Count(State) as TotalCount,
Count(State)  1.0 / (Select Count() from stg_Churn)  as Percentage from stg_Churn Group by State Order by Percentage desc

Data Exploration – Check Nulls
SELECT 
SUM(CASE WHEN Customer_ID IS NULL THEN 1 ELSE 0 END) AS Customer_ID_Null_Count,
SUM(CASE WHEN Gender IS NULL THEN 1 ELSE 0 END) AS Gender_Null_Count,
SUM(CASE WHEN Age IS NULL THEN 1 ELSE 0 END) AS Age_Null_Count,
SUM(CASE WHEN Married IS NULL THEN 1 ELSE 0 END) AS Married_Null_Count,
SUM(CASE WHEN State IS NULL THEN 1 ELSE 0 END) AS State_Null_Count,
SUM(CASE WHEN Number_of_Referrals IS NULL THEN 1 ELSE 0 END) AS Number_of_Referrals_Null_Count,
SUM(CASE WHEN Tenure_in_Months IS NULL THEN 1 ELSE 0 END) AS Tenure_in_Months_Null_Count,
SUM(CASE WHEN Value_Deal IS NULL THEN 1 ELSE 0 END) AS Value_Deal_Null_Count,
SUM(CASE WHEN Phone_Service IS NULL THEN 1 ELSE 0 END) AS Phone_Service_Null_Count,
SUM(CASE WHEN Multiple_Lines IS NULL THEN 1 ELSE 0 END) AS Multiple_Lines_Null_Count,
SUM(CASE WHEN Internet_Service IS NULL THEN 1 ELSE 0 END) AS Internet_Service_Null_Count,
SUM(CASE WHEN Internet_Type IS NULL THEN 1 ELSE 0 END) AS Internet_Type_Null_Count,
SUM(CASE WHEN Online_Security IS NULL THEN 1 ELSE 0 END) AS Online_Security_Null_Count,
SUM(CASE WHEN Online_Backup IS NULL THEN 1 ELSE 0 END) AS Online_Backup_Null_Count,
SUM(CASE WHEN Device_Protection_Plan IS NULL THEN 1 ELSE 0 END) AS Device_Protection_Plan_Null_Count,
SUM(CASE WHEN Premium_Support IS NULL THEN 1 ELSE 0 END) AS Premium_Support_Null_Count,
SUM(CASE WHEN Streaming_TV IS NULL THEN 1 ELSE 0 END) AS Streaming_TV_Null_Count,
SUM(CASE WHEN Streaming_Movies IS NULL THEN 1 ELSE 0 END) AS Streaming_Movies_Null_Count,
SUM(CASE WHEN Streaming_Music IS NULL THEN 1 ELSE 0 END) AS Streaming_Music_Null_Count,
SUM(CASE WHEN Unlimited_Data IS NULL THEN 1 ELSE 0 END) AS Unlimited_Data_Null_Count,
SUM(CASE WHEN Contract IS NULL THEN 1 ELSE 0 END) AS Contract_Null_Count,
SUM(CASE WHEN Paperless_Billing IS NULL THEN 1 ELSE 0 END) AS Paperless_Billing_Null_Count,
SUM(CASE WHEN Payment_Method IS NULL THEN 1 ELSE 0 END) AS Payment_Method_Null_Count,
SUM(CASE WHEN Monthly_Charge IS NULL THEN 1 ELSE 0 END) AS Monthly_Charge_Null_Count,
SUM(CASE WHEN Total_Charges IS NULL THEN 1 ELSE 0 END) AS Total_Charges_Null_Count,
SUM(CASE WHEN Total_Refunds IS NULL THEN 1 ELSE 0 END) AS Total_Refunds_Null_Count,
SUM(CASE WHEN Total_Extra_Data_Charges IS NULL THEN 1 ELSE 0 END) AS Total_Extra_Data_Charges_Null_Count,
SUM(CASE WHEN Total_Long_Distance_Charges IS NULL THEN 1 ELSE 0 END) AS Total_Long_Distance_Charges_Null_Count,
SUM(CASE WHEN Total_Revenue IS NULL THEN 1 ELSE 0 END) AS Total_Revenue_Null_Count,
SUM(CASE WHEN Customer_Status IS NULL THEN 1 ELSE 0 END) AS Customer_Status_Null_Count,
SUM(CASE WHEN Churn_Category IS NULL THEN 1 ELSE 0 END) AS Churn_Category_Null_Count,
SUM(CASE WHEN Churn_Reason IS NULL THEN 1 ELSE 0 END) AS Churn_Reason_Null_Count
FROM stg_Churn;
 

 

Remove null and insert the new data into Prod table

SELECT 
    Customer_ID,Gender,Age,Married,State,Number_of_Referrals,Tenure_in_Months,ISNULL(Value_Deal, 'None') AS Value_Deal,Phone_Service,ISNULL(Multiple_Lines, 'No') As Multiple_Lines,
Internet_Service,ISNULL(Internet_Type, 'None') AS Internet_Type,ISNULL(Online_Security, 'No') AS Online_Security,ISNULL(Online_Backup, 'No') AS Online_Backup,ISNULL(Device_Protection_Plan, 'No') AS Device_Protection_Plan,ISNULL(Premium_Support, 'No') AS Premium_Support,ISNULL(Streaming_TV, 'No') AS Streaming_TV,ISNULL(Streaming_Movies, 'No') AS Streaming_Movies,ISNULL(Streaming_Music, 'No') AS Streaming_Music,ISNULL(Unlimited_Data, 'No') AS Unlimited_Data,Contract,
Paperless_Billing,Payment_Method,Monthly_Charge,Total_Charges,Total_Refunds,Total_Extra_Data_Charges,Total_Long_Distance_Charges,Total_Revenue,Customer_Status,ISNULL(Churn_Category, 'Others') AS Churn_Category,ISNULL(Churn_Reason , 'Others') AS Churn_Reason
INTO [db_Churn].[dbo].[table_name]
FROM [db_Churn].[dbo].[table name];
   

 Create View for Power BI

