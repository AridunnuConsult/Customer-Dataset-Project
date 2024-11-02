# Customer-Dataset-Project

## Project Title: Customer Data Analysis 
---
## Project Outlines

[Project Overview for sales data](#project-overview-for-sale-data)

[Data source](#data-source)

[Tool used](#tool-used)

[Data cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

---
### Project Overview for sales data
The purpose of this documentation is to analyze the customer data set for a subscription service by calculating some metric such as the subscription duration, the most popular subscription type, the average subscriptin duration etc. To also display some visuals with the use of pivot table and power Bi visulisation.

### Data source
The data used for this analysis was downloaded from my canvas learning management system account (Lita Capstone Dataset.xlsx)

### Tool used  
- Microsoft Excel- This tool was used to clean the dataset 
- SQL Server Management Studio-for querying of the dataset 
  Power BI- for creating dashboard to visual some insights
- GitHub- this is used to build my portfolio as well as document my project

### Data cleaning and Preparation
After opening the dataset, we perform some data cleaning such as
- Adjusting the dataset
- Add another column to the dataset
- Removing some duplicates in the dataset
- Perform some calculation using the excel funtions
- Data formatting
- Perform some visuals using pivot table etc

### Exploratory Data Analysis 
I provide answer to some questions on the dataset such as 
- Find the subscription Duration
- Average subscription Duration
- The most popular subscription type
- Total Number of customers from each region
- Total revenue for each subscription type etc

### Data analysis
These are some of the code and queries used to achieve our analysis
```Excel
=AVG(I5:133791)
=COUNTIF(Table1[SubscriptionType],D33782)
```

```SQL
SELECT REGION, COUNT(CUSTOMERID) AS TOTAL_NO_OF_CUSTOMER
FROM [DBO].[LITA CUSTOMER DATA 2]
GROUP BY REGION
ORDER BY 2 DESC

SELECT TOP 1 SUBSCRIPTION TYPE, COUNT(CUSTOMERID)
AS [THE MOST POPULAR SUBSCRIPTION] FROM [DBO].[LITA CUSTOMER DATA 2]
GROUP BY SUBSCRIPTION TYPE
ORDER BY 2 DESC

SELECT CUSTOMERID, AVG(SUBSCRPTION_DURATION)
AS AVERAGE_SUBSCRIPTION FROM [DBO].[LITA CUSTOMER DATA 2]
GROUP BY CUSTOMERID

SELECT CUSTOMERID, COUNT(CANCELED) FROM [DBO].[LITA CUSTOMER DATA 2]
WHERE CANCELED='TRUE'
GROUP BY CUSTOMERID

SELECT CUSTOMERID, COUNT(CANCELED) FROM [DBO].[LITA CUSTOMER DATA 2]
WHERE CANCELED='FALSE'
GROUP BY CUSTOMERID

SELECT SUBSCRIPTION TYPE, SUM(REVENUE) AS TOTAL_REVENUE FROM [DBO].[LITA CUSTOMER DATA 2]
GROUP BY SUBSCRIPTION TYPE
ORDER BY DESC

---
```

### Data Visualization
This preview some of the analyses done so far
  - Excel calculation for the Customer Data

    ![Calculation for customer data](https://github.com/user-attachments/assets/e33b41b0-520a-401b-be20-c6c5693ab38e)


![Pivot table for Customer data](https://github.com/user-attachments/assets/ddf51c19-5256-4eb1-9364-4b780d6e06d7)

- some queries written on SQL for analysis
![Total number of customer per region](https://github.com/user-attachments/assets/e71cf2db-5143-49af-a5be-7f0bba264d3a)


![The Most popular subscription type](https://github.com/user-attachments/assets/857147ab-2d56-4d05-a269-90c758b12907)


![Customer who canceled subscription within 6months](https://github.com/user-attachments/assets/530bf0db-ab20-4496-8b4d-950a648e18b3)


![Avg  Subscrip for all customer](https://github.com/user-attachments/assets/29499161-520c-413a-a26c-91ac3c7636cb)


![Total Revenue for Subscription Type](https://github.com/user-attachments/assets/38ca70be-d5dd-433c-a7db-62672d654f6d)


![Top 3 region  by subscrip  cancellation](https://github.com/user-attachments/assets/b8ae2aa3-9cf4-4f7b-91a9-4d080c739c87)


![Active   Canceled subscription](https://github.com/user-attachments/assets/851606cd-f892-4bc4-bf0e-7c7471d2f2ee)
