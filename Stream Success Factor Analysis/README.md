# 🎧 Stream Success Factor Analysis
In this project involved the comprehensive cleaning and analysis of an 2023 Spotify dataset, utilising MySQL in the DBeaver environment.

#### Key Phases:

**🔶Data Cleaning:** Managing missing values, deleting noise/outlier in diverse columns. <br> 
**🔶Hit Song Recipe:** Identifying Key Success Drivers: Comparative analysis of audio features (e.g., energy, danceability, acousticness) between Top 50 hit tracks and the overall dataset average to define the 2023 Hit Song Recipe. Correlation Analysis to uncover relationships among successful audio attributes. <br> 
**🔶Quantifying Platform Influence:** Analysing the dependency ratio of Top 50 hits across Spotify, Apple Music, and Deezer playlist inclusion to quantify Spotify's market dominance.<br>

**Actionable Insights:**




Feel free to connect with me via: 
LinkedIn [Junghyeon Ahn](https://www.linkedin.com/in/junghyeon-ahn/), Email: ro033026@gmail.com


## Tools Used:
- **MySQL**: For querying and analyzing data across various projects.

## Datasets:
- **Kaggle**: [E-Commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data/data)


## Table of Contents
- [Project 1: Data Cleaning](#project-1-Data-Cleaning)
- [Project 2: Product-Centric Analysis](#project-2-product-centric-analysis)
- [Project 3: Customer-Centric Analysis](#project-3-Customer-Centric-Analysis)
- [Key Insights](#%EF%B8%8Fkey-insights)

# Projects:
## Project 1: Data Cleaning

[View SQL query]()

### 1. Preview the data
Before cleaning the data, check the row count.<br><br>
<img width="167" height="179" alt="image" src="https://github.com/user-attachments/assets/e1364ef4-4524-428d-9cb6-11360eb8ddfc" />


### 2.Numeric Outlier Value & Noises
Firstly, I examine the distribution of Price and Quantity using the Min, Median, and Max values. The results indicate significant negative outliers in both the Price and Quantity columns.<br><br>
<img width="788" height="365" alt="image" src="https://github.com/user-attachments/assets/8127e4d0-57df-4b5f-ac32-eb6b7667c4ac" />
<br><br>
<img width="275" height="65" alt="image" src="https://github.com/user-attachments/assets/7fe9fc80-331c-4c7c-b1a4-52086e71659d" />
<br><br>
<img width="401" height="154" alt="image" src="https://github.com/user-attachments/assets/3b1ac1dd-f82b-4181-8a00-643149cce1fb" />
<br><br>
Cousticness&  <br><br>
<img width="905" height="402" alt="image" src="https://github.com/user-attachments/assets/048de8db-6f9c-46c6-8779-189966d5d335" />
<br><br>
<img width="134" height="200" alt="image" src="https://github.com/user-attachments/assets/8f469b1a-8dd5-4d9a-95c3-6aa069b316e7" />
<br><br>
Furthermore, some negative transactions contain empty strings in the 'Description' column (the item name).<br><br>
<img width="953" height="275" alt="image" src="https://github.com/user-attachments/assets/cd886e0d-a0ea-45cf-b7a4-2cf3a770c22c" />
<br><br>
There was one outlier in streams column<br><br>
<img width="770" height="238" alt="image" src="https://github.com/user-attachments/assets/208d0014-b784-45ad-ad32-67f6a128acef" />
<br><br>
In addition to there are some noises in track name, but that seems japanese word 
<img width="361" height="311" alt="image" src="https://github.com/user-attachments/assets/9b6f20b6-f272-475b-856c-3ffc6a19da21" />
<br><br>

<br><br>
 The next step is to check all remaining missing values, including both NULLs and empty strings, across each column.<br><br>

### 3. Missing Values(Empty Strings)
An initial data quality check was performed to confirm the integrity of the dataset. The query below specifically verifies the presence of NULL values across all key columns. <br><br>
<img width="797" height="500" alt="image" src="https://github.com/user-attachments/assets/68327466-63e0-4eaa-ab15-cac7ddf1c03a" />
<br><br>
While the dataset contained no explicit NULL values, a proactive check for empty strings ('') was executed, as they can also indicate missing data. This analysis revealed a significant finding: 135,080 empty cells across the dataset. <br><br>
<img width="720" height="568" alt="image" src="https://github.com/user-attachments/assets/b7b3ec0c-e06a-4781-8a65-808fc134bb62" />
<br><br>


<br><br>
As a result, customer ID colunn confirmed for all 135,080 missing datas. Seperately, 1454 duplicates in entries were also indentifued with the Descriotion column. 
However, missing data is **24.93%** of total records. With **24.93%** deletion is impractical. Instead, the non missing and smiliar data will be retained and analyzed by utilizing Invoice Column.<br><br> 



## Project 2: Hit Song Recipe

[View SQL query](https://github.com/JunghyeonAhn/SQL-Project-/blob/main/Online%20Retail%20Transaction%20Analysis/SQL-script%20-%202.%20Product-Centric%20Analysis)

### 1. Overview - Total revenue 
<img width="533" height="411" alt="image" src="https://github.com/user-attachments/assets/42833da5-4bc0-439a-a0da-dd6e7b2d3289" />
<br><br>

#### 1.1. Top 10 Purchased items
<img width="550" height="395" alt="image" src="https://github.com/user-attachments/assets/5dbe4b4e-8810-4d6e-925e-b3d9f459a66e" />
<br><br>

### 2. TOP 3 Sales items by country 
<img width="486" height="578" alt="image" src="https://github.com/user-attachments/assets/746dd38c-8383-450f-aefa-c71e0fba6761" />
<br><br>

### 3. Top3 sales items by months
<img width="506" height="565" alt="image" src="https://github.com/user-attachments/assets/7c95b695-7f30-46ac-82fb-63c058e91d8d" />
<br><br>




## Project 3: Quantifying Platform Influence

[View SQL query](https://github.com/JunghyeonAhn/SQL-Project-/blob/main/Online%20Retail%20Transaction%20Analysis/SQL-script%20-%203.%20%20Customer-Centric%20Analysis)

### 1. Overview - Customer 
<img width="599" height="409" alt="image" src="https://github.com/user-attachments/assets/703ae8e3-1c5f-402a-b360-8bace9799f28" />
<br><br>

### 2. Repurchase_Rate_Percentage
<img width="514" height="314" alt="image" src="https://github.com/user-attachments/assets/ed50f5e4-2052-48b0-b38e-b79ab10c30d3" />
<br><br>

### 3. Purchase pattern by Country 
<img width="444" height="414" alt="image" src="https://github.com/user-attachments/assets/f788068a-e161-4d46-8a18-eeae3f2bfdf5" />
<br><br>

### 4. TOP 10 Customer
#### 4.1 Over 2 items
<img width="528" height="400" alt="image" src="https://github.com/user-attachments/assets/81c077bd-964c-4613-9d68-773767779df1" />
<br><br>

#### 4.2 Less 2 items
<img width="527" height="362" alt="image" src="https://github.com/user-attachments/assets/0502d839-f36c-42c2-bd17-4fb6890cc6da" />
<br><br>

### 5. Purchased items by CustomerID
<img width="522" height="418" alt="image" src="https://github.com/user-attachments/assets/1235becb-7754-481f-8b7d-d43ab7584cdf" />
<br><br>

### 6. Purchases by Months
<img width="606" height="392" alt="image" src="https://github.com/user-attachments/assets/a66f4cb1-bbe2-4304-96cd-36488ae18e55" />
<br><br>




## 🗝️Key Insights
### Summary






















