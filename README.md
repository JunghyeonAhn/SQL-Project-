# SQL-Project
Welcome to my SQL portfolio.  
In this project, I analyzed a shopping trends dataset using **MySQL** in the **DBeaver environment**.  

The analysis covers the entire workflow:
- **Data Cleaning**: handling missing values, checking duplicates, and validating business logic.  
- **Key Business KPIs**: calculating order count, total revenue, AOV, ARPU, repeat purchase rates, and subscription ratios.  
- **Segmentation Analysis**: breaking down purchase behaviors by age group, product categories, payment methods, discount sensitivity, and review satisfaction.  
- **Actionable Insights**: identifying which customer groups contribute the most revenue, which age segments are price sensitive, and where marketing strategies can be optimized.  

This work demonstrates my ability to use SQL for **discovering consumer purchase insights through retail data analysis**, from raw data exploration to generating insights that can inform marketing and product decisions.


Feel free to connect with me via: 
LinkedIn [Junghyeon Ahn](https://www.linkedin.com/in/junghyeon-ahn/), Email: ro033026@gmail.com


## Tools Used:
- **MySQL**: For querying and analyzing data across various projects.

## Datasets:
- **Kaggle**: [Customer Shopping Trends Dataset](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset/discussion?sort=hotness)


## Table of Contents
- [Projects](#projects)
  - [Project 1: Cleaning the data](#project-1-cleaning-the-data)
  - [Project 2: Key Business KPIs](#project-2-key-business-kpis)
  - [Project 3: Age Group Purchase Characteristics](#project-3-age-group-purchase-characteristics)
  - [Project 4: Purchase Patterns by Subscription Status](#project-4-purchase-patterns-by-subscription-status)
  - [Project 4: Metrics Calculation and UTM Campaign Tracking with SQL](#project-4-metrics-calculation-and-utm-campaign-tracking-with-sql)
  - [Project 5: Data Preparation for BI Reporting using Google BigQuery](#project-5-data-preparation-for-bi-reporting-using-google-bigquery)
  - [Project 6: Conversion Calculation by Date and Traffic Channel using Google BigQuery](#project-6-conversion-calculation-by-date-and-traffic-channel-using-google-bigquery)
  - [Project 7: Comparison of Conversion Rates Between Different Landing Pages using Google BigQuery](#project-7-comparison-of-conversion-rates-between-different-landing-pages-using-google-bigquery)
  - [Project 8: Correlation Analysis Between User Engagement and Purchases using Google BigQuery](#project-8-correlation-analysis-between-user-engagement-and-purchases-using-google-bigquery)
- [Skills Demonstrated](#skills-demonstrated)
- [Contact](#contact)


# Projects:
## Project 1: Cleaning the data

[View SQL query](https://github.com/AndreasHutmann/SQL-Project-/blob/main/SQL-script%20-%201.%20Data%20cleaning)

**1. Preview the data**
<br><br>
<img width="1470" alt="Preview the data" src="https://github.com/user-attachments/assets/7cece1f1-1a85-4265-ac24-dffaad25dfbc">

**2. Null Value check**
<br><br>
<img width="1470" alt="Null Value check" src="https://github.com/user-attachments/assets/4551dfd2-f5b9-41b2-91e9-1482a273f73d">

**3. Duplicate row check**
<br><br>
<img width="1470" alt="Duplicate row check" src="https://github.com/user-attachments/assets/c20d3eb6-a352-4243-a8ff-402db913a6c7">

**4. Numeric range & outlier scan**
<br><br>
<img width="1470" alt="Numeric range & outlier scan" src="https://github.com/user-attachments/assets/cbfb78e1-cab2-4082-a532-4e67f0093b73">

**5. Categorical value sanity checks**
<br><br>
<img width="1470" alt="Categorical value sanity checks" src="https://github.com/user-attachments/assets/6e23cd3c-4e46-4e8f-9cde-2bb45a99a284">

**6. Business logic validation**
<br><br>
<img width="1470" alt="Business logic validation" src="https://github.com/user-attachments/assets/1a91706e-c2cc-47f9-9098-88cad42523bd">


## Project 2: Key Business KPIs

[View SQL query](https://github.com/AndreasHutmann/SQL-Project-/blob/main/SQL-script%20-%20%202.%20Key%20Business%20KPIs)


**1. Customer & Revenue KPIs** 
<br><br>
![Preview the data](https://github.com/user-attachments/assets/6ddb6fdf-811b-4691-b681-b0d26ed2288f)

**2. Purchase Behavior KPIs**
2.1 Max, Min Purchase
<br><br>
![Preview the data](https://github.com/user-attachments/assets/a778e54f-57bf-4ba8-9a48-b5cc2ec05ee7)

2.2 Repeat Purchase Ratio by Frequency
<br><br>
![Preview the data](https://github.com/user-attachments/assets/1f938652-8522-4d73-b456-3f7c0965427b)

**4. Total Revenue and Ratio by Category** 
<br><br>
![Preview the data](https://github.com/user-attachments/assets/557f3a7c-0833-41fe-a52e-38ccda1b3fa5)

**5. Revenue ratio by Subscriptions**  
<br><br>
![Preview the data](https://github.com/user-attachments/assets/78b3f922-ad1e-494c-a6ec-c332c239dee0)



## Project 3: Age Group Purchase Characteristics

[View SQL query](https://github.com/AndreasHutmann/SQL-Project-/blob/main/SQL-script%20-%203.%20Age%20Group%20Purchase%20Characteristics)


**1. Orders and Revenue by Age Group**
<br><br>
![Preview the data](https://github.com/user-attachments/assets/87b30d99-4965-42cb-bac9-bfd4d635fc70)



**2. Category Preference by Age Group** 
<br><br>
   ![Preview the data](https://github.com/user-attachments/assets/2e73d6a5-7ab8-4bac-a80f-9768a533334e)


**3. Payment Method Analysis by Age Group**
<br><br>
![Preview the data](https://github.com/user-attachments/assets/380532d0-2434-466b-b90b-b622a17748dd)


**4. Price Sensitivity by Age Group**
<br><br>
![Preview the data](https://github.com/user-attachments/assets/1a973507-0238-4bb0-9871-ef1bf336631a)



**5. Customer Satisfaction and AOV by Age Group** 
<br><br>
![Preview the data](https://github.com/user-attachments/assets/d6097ef4-9e51-4370-b299-89e165a7ef4a)


**6. ARPU by Age Group**
<br><br>
![Preview the data](https://github.com/user-attachments/assets/d75d9ee2-0260-42a6-b466-3c6a86172825)



## Project 4: Purchase Patterns by Subscription Status

[View SQL query](https://github.com/AndreasHutmann/SQL-Project-/blob/main/Project%204%20%3A%20Purchase%20Patterns%20by%20Subscription%20Status)


**1. KPI by Subscription (Orders, AOV, Revenue)**
<br><br>
![Preview the data](https://github.com/user-attachments/assets/87b30d99-4965-42cb-bac9-bfd4d635fc70)








