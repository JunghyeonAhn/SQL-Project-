# 🎧 Stream Success Factor Analysis
In this project involved the comprehensive cleaning and analysis of an 2023 Spotify dataset, utilising MySQL in the DBeaver environment.

#### Key Phases:

**🔶Data Cleaning:** Managing missing values, deleting noise/outlier in diverse columns. <br> 
**🔶Hit Song Recipe:** Identifying Key Success Drivers: Comparative analysis of audio features (e.g., energy, danceability, acousticness) between Top 50 hit tracks and the overall dataset average to define the 2023 Hit Song Recipe. Correlation Analysis to uncover relationships among successful audio attributes. <br> 
**🔶 Platform effeciency:** Analysing the dependency ratio of Top 50 hits across Spotify, Apple Music, and Deezer playlist inclusion to quantify Spotify's market dominance.<br>

**Actionable Insights:**




Feel free to connect with me via: 
LinkedIn [Junghyeon Ahn](https://www.linkedin.com/in/junghyeon-ahn/), Email: ro033026@gmail.com


## Tools Used:
- **MySQL**: For querying and analyzing data across various projects.

## Datasets:
- **Kaggle**: [Most Streamed Spotify Songs 2023](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023/data)


## Table of Contents
- [Project 1: Data Cleaning](#project-1-Data-Cleaning)
- [Project 2: EDA & Hit Song Recipe](#project-2-EDA-&-Hit-Song-Recipe)
- [Project 3: Platform effeciency](#project-3-Platform-effeciency)
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

### 4. DELETE Value
<img width="308" height="253" alt="image" src="https://github.com/user-attachments/assets/3feed0b2-a345-4ea6-94e8-c67869b42ccb" />
<br><br>



<br><br>
As a result, there are some missing value in key, charts coulmn including 0 value in charts and some noise in trackname.However it is not the critical issue for analysing except one noise in streams column, so I will remove it. Then I'm going to analyse the data excepting "Cousticness&" coulumn.   <br><br> 



## Project 2: EDA & Hit Song Recipe

[View SQL query]()

### EDA. 1.Overview 
<img width="625" height="270" alt="image" src="https://github.com/user-attachments/assets/1ec76a06-0ff1-42e0-816b-d3492433a853" />

<br><br>

### EDA. 2.Song counts by released year
<img width="203" height="323" alt="image" src="https://github.com/user-attachments/assets/1f6ad403-6e2c-4984-a47c-17edfd388c95" />
<br><br>

### EDA. 3.TOP 10 Tracks by total streams
<img width="416" height="353" alt="image" src="https://github.com/user-attachments/assets/ec78b9eb-655b-4981-b619-e74e44ce7d06" />
<br><br>

### EDA. 4.TOP 10 Artists by total streams
<img width="249" height="329" alt="image" src="https://github.com/user-attachments/assets/96bdfdc4-7657-44f9-8580-587f0dcb7b7a" />
<br><br>

### A Comparative Analysis of Audio Features (Top 50 vs. Total)
#### Total_audio features
<img width="704" height="415" alt="image" src="https://github.com/user-attachments/assets/c3c99f6e-d433-49e8-829e-2f90a4151143" />
<br><br>

#### Top50_audio features
<img width="707" height="428" alt="image" src="https://github.com/user-attachments/assets/b29bf191-0016-4da9-94a3-fa93a8e66cc2" />
<br><br>

### Comparative Analysis of Hit Track Playlist Acquisition
#### Total_number of playlist by platforms
<img width="601" height="275" alt="image" src="https://github.com/user-attachments/assets/b09a34c6-6951-41d4-a65f-28da1951a4ec" />
<br><br>

#### Top50_number of playlists by platforms
<img width="602" height="391" alt="image" src="https://github.com/user-attachments/assets/e6f46dba-52ee-469f-ba81-fa4e4ada2bcc" />
<br><br>


## Project 3: Platform effeciency
[View SQL query]()

### 1. Platform effeciency - spotify vs apple 
#### Total - 1.3%
<img width="560" height="179" alt="image" src="https://github.com/user-attachments/assets/272e8f2e-98b8-4df5-bdb2-c4edfc82f0e9" />
<br><br>

#### Top50 - 1.2%
<img width="653" height="331" alt="image" src="https://github.com/user-attachments/assets/febc9d53-6aa5-4eee-9dae-321a3ee3ad97" />
<br><br>

### 2. Platform effeciency - spotify vs deezer 
#### Total - 1.9%
<img width="578" height="167" alt="image" src="https://github.com/user-attachments/assets/51d4a72a-9dda-4464-9182-5e1d0647713f" />
<br><br>

#### Top50 - 0.7%
<img width="373" height="342" alt="image" src="https://github.com/user-attachments/assets/de374138-39ad-4774-ac3e-6e920416a333" />
<br><br>






## 🗝️Key Insights
### Summary






















