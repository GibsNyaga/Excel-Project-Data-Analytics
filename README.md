# Project 2 Analysis  

## Introduction  

As job seeker, I was surprised by the lack of data exploring the most optimal jobs and skills in the data science market. I set out to understand what skills top employers request and how to land more pay.  

## Questions to Analyze  

To understand the data science job market, I asked the following:

1. Do more skills get you better pay?  
2.  What’s the salary for data jobs in different regions?  
3.  What are the top skills of data professionals?  
4.  What’s the pay for the top 10 skills?

## Excel Skills Used  

The following Excel skills were utilized for analysis:  

- 📊 Pivot Tables  
- 📈 Pivot Charts  
- 🧮 DAX (Data Analysis Expressions)  
- 🔍 Power Query  
- 💪 Power Pivot

## Data Jobs Dataset  

The dataset used for this project contains real-world data science job information from 2023.  

It includes detailed information on:

- 👨‍💼 Job titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Skills

## 1️⃣ Do more skills get you better pay?  

## 🔍 Skill: Power Query (ETL) 

### 📥 Extract  

- I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:  
    - 🗃️ First one with all the data jobs information.  
    - 🔧 The second listing the skills for each job ID.
 
### 🔄 Transform  

- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

    - 📊 data_jobs_all  
 
      <img width="400" alt="data_jobs_all" src="https://github.com/user-attachments/assets/577e72b8-9dd5-4274-8c16-bf84c49e1510" />
 
    - 🛠️ data_job_skills  
  
      <img width="400" alt="data_job_skills" src="https://github.com/user-attachments/assets/4bebe47c-c053-4592-8525-6616dcd6f8b2" />
  
  ### 🔗 Load
- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.  

    - 📊 data_jobs_all
    <br>
    <img width="800" alt="data_jobs_all (2)" src="https://github.com/user-attachments/assets/0efa5d56-a3b4-4a48-b019-42f594775732" />  

    <br> 
    
    - 🛠️ data_job_skills
  
    <br>
    <img width="800" alt="data_job_skills (2)" src="https://github.com/user-attachments/assets/473c74d5-65e7-4dd8-9334-1aa139c07110" />  
    <br>

    ## 📊 Analysis
  ####<img width="793" height="481" alt="Analysis3" src="https://github.com/user-attachments/assets/dc0fcb48-bc8e-455a-a57a-d039500d0028" />
 💡 Insights
  - 📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.  

- 💼 Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.

<img width="800" alt="Analysis" src="https://github.com/user-attachments/assets/2da288e2-3651-487d-be68-c40db0a15021" />

### 🤔 So What?  
This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.  

## 2️⃣ What’s the salary for data jobs in different regions?  

### 🧮 Skills: PivotTables & DAX.

📈Pivot Table.  

🔢 I created a PivotTable using the Data Model I created with Power Pivot.  
📊 I moved the `job_title_short` to the rows area and `salary_year_avg` into the values area.  
🧮 Then I added new measure to calculate the median salary for United States jobs.  

```
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States")
```
🧮 DAX  
- To calculate the median year salary I used DAX.
```
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

### 📊 Analysis  
#### 💡 Insights  
- 💼 Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.  

- 💰 The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.  

<img width="1000" alt="Analysis2" src="https://github.com/user-attachments/assets/b78b3a5d-bef5-449f-b8ee-85d3a94f1228" />  

#### 🤔 So What?
These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering geographical variations.  

## 3️⃣ What are the top skills of data professionals?  

### 🔧 Skill: Power Pivot  
#### 💪 Power Pivot  

- 🔗 I created a data model by integrating the `data_jobs_all` and `data_jobs_skills` tables into one model.  
- 🧹 Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.

#### 🔗 Data Model  
- I created a relationship between my two tables using the job_id column.  

<img width="800" alt="Power_Pivot_model" src="https://github.com/user-attachments/assets/5609d5c7-d973-461f-9484-936c31f863c9" />  


#### 📃 Power Pivot Menu  
- The Power Pivot menu was used to refine my data model and makes it easy to create measures.

<img width="1000" alt="Pivot_Menu" src="https://github.com/user-attachments/assets/dceb5b8c-2647-4680-adab-c4efdfc83cb5" />  

### 📊Analysis

#### 💡Insights

- 💻 SQL and Python dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.  

- ☁️ Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.

<img width="793" height="481" alt="Analysis3" src="https://github.com/user-attachments/assets/62e3053e-685f-4ff6-aa36-ba63bee6c4cd" />  

#### 🤔So What
- Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.  

## 4️⃣ What’s the pay of the top 10 skills?  
### 📊 Skill: Advanced Charts (Pivot Chart)  
#### 📈 PivotChart
- I created a combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.
    - 🪙 Primary Axis: Median Salary (as a Clustered Column)
    - 👍 Secondary Axis: Skill Likelihood (as a Line with Markers)
To customize the chart, I added a title axis title, removed the lines (skill likelihood), and changed the markers to diamonds.

### 📊 Analysis
- 💰 Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.
- 📉 Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicating less specialization and demand in high-salary sectors.

<img width="804" height="480" alt="Analysis4" src="https://github.com/user-attachments/assets/b5703902-694c-40f7-9ab1-88080edc9c4f" />  

#### 🤔So What?
- This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.  

## Conclusion  

As a data enthusiast and former job seeker, I embarked on this Excel-based project to uncover valuable insights about the data science job market. Using a dataset I've curated from real-world job postings, I analyzed job titles, salaries, locations, and essential skills. By leveraging Excel features like Power Query, PivotTables, DAX, and charts, I discovered key correlations between multiple skills and higher salaries, particularly in Python, SQL, and cloud technologies.  

I hope this project serves as a practical guide for data professionals and provides an overview of the skills needed for higher-paying roles.
 





