# 🛒Online Retail Transaction Analysis
In this project, I analyzed a shopping trends dataset using **MySQL** in the **DBeaver environment**.  

The analysis covers the entire workflow:
- **Data Cleaning**: handling missing values, wrong product name, and product Name standardisation and categorisation  
- **Product-Centric Analysis**: 
- **Time Series Analysis**:
- **Actionable Insights**: 

This work demonstrates my ability to use SQL for **discovering consumer purchase insights through retail data analysis**, from raw data exploration to generating insights that can inform marketing and product decisions.


Feel free to connect with me via: 
LinkedIn [Junghyeon Ahn](https://www.linkedin.com/in/junghyeon-ahn/), Email: ro033026@gmail.com


## Tools Used:
- **MySQL**: For querying and analyzing data across various projects.

## Datasets:
- **Kaggle**: [E-Commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data/data)


## Table of Contents
- [Project 1: Cleaning the data](#project-1-cleaning-the-data)
- [Project 2: Product-Centric Analysis](#project-2-product-centric-analysis)
- [Project 3: Time Series Analysis](#project-3-time-series-analysis)

# Projects:
## Project 1: Cleaning the data

[View SQL query](https://github.com/JunghyeonAhn/SQL-Project-/blob/main/Online%20Retail%20Transaction%20Analysis/SQL-script%20-%201.%20Data%20cleaning%20%26%20EDA)

### 1. Preview the data
Before cleaning the data, check the row count.<br><br>
<img width="182" height="143" alt="image" src="https://github.com/user-attachments/assets/5ed6baa9-2020-4bca-a5cb-fb085be171c4" />


### 2.Numeric Outlier Value
Firstly, I examine the distribution of Price and Quantity using the Min, Median, and Max values. The results indicate significant negative outliers in both the Price and Quantity columns.<br><br>
<img width="532" height="223" alt="image" src="https://github.com/user-attachments/assets/1e831a99-51cd-4e5b-a44b-2c0f06086470" />
<br><br>
The table contains 10,626 negative transactions, which accounts for 1.96% of the total dataset. <br><br>
<img width="290" height="148" alt="image" src="https://github.com/user-attachments/assets/bb4454b8-bbb6-4cec-881d-315a0f0d1553" />
<br><br>
Furthermore, some negative transactions contain empty strings in the 'Description' column (the item name).<br><br>
<img width="377" height="241" alt="image" src="https://github.com/user-attachments/assets/9da656fd-9053-4eec-a3df-fd1494489a19" />
<br><br>
 The next step is to check all remaining missing values, including both NULLs and empty strings, across each column.<br><br>

### 3. Missing Values(NULL & Empty Strings)
There are not NULL Value in each column. But I'm tried to find empty value, just in case. <br><br>
<img width="539" height="238" alt="image" src="https://github.com/user-attachments/assets/8526de4e-4ef0-4181-89c0-02765fbdeb98" />
<br><br>
In this dataset, there are 135,080 empty cells and according to results, there are many empty cells in Customer ID. <br><br>
<img width="206" height="243" alt="image" src="https://github.com/user-attachments/assets/323dba5d-7f1d-4595-b81e-07280882d3e7" />
<br><br>
To see in detail, aggregate each coulumn having empty cells.<br><br> 
<img width="502" height="240" alt="image" src="https://github.com/user-attachments/assets/3566882f-e31f-4678-a570-bdb0d60e8b97" />
<br><br>
<br><br>
<img width="547" height="434" alt="image" src="https://github.com/user-attachments/assets/e29bd06c-dde4-4d20-996f-b6a632a1f28a" />
<br><br>

### 4. Date/Time Range and Format Validation
<br><br>
<img width="344" height="182" alt="image" src="https://github.com/user-attachments/assets/3d546f5b-5509-4f82-921b-0da477ceafc9" />
<br>

### 5. Product Description Noise Filtration
<br><br>
<img width="283" height="461" alt="image" src="https://github.com/user-attachments/assets/09519679-bc86-4902-92ba-6a2962b27993" />
<br>
<img width="273" height="452" alt="image" src="https://github.com/user-attachments/assets/204083fd-58b6-47ea-8d95-98f9719f78ad" />
<br>
<img width="280" height="275" alt="image" src="https://github.com/user-attachments/assets/44f98fad-300c-4442-b9c9-b78f62966341" />
<br>
<img width="650" height="635" alt="image" src="https://github.com/user-attachments/assets/0841fa41-83e8-4ced-9546-8ee9fdab8095" />


### 6. Product Name Standardization and Categorization
<br><br>


## Project 2: Product-Centric Analysis

[View SQL query](-)

<br><br>
![Preview the data](-)



## Project 3: Time Series Analysis

[View SQL query](-)
























