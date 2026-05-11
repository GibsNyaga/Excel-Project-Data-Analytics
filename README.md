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

# 1️⃣ Do more skills get you better pay?  

## 🔍 Skill: Power Query (ETL) 

### 📥 Extract  

- I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:  
    - 🗃️ First one with all the data jobs information.  
    - 🔧 The second listing the skills for each job ID.
 
### 🔄 Transform  

- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

    - 📊 data_jobs_all  
 
      <img width="504" height="608" alt="data_jobs_all" src="https://github.com/user-attachments/assets/577e72b8-9dd5-4274-8c16-bf84c49e1510" />
 
    - 🛠️ data_job_skills  
  
      <img width="379" height="583" alt="data_job_skills" src="https://github.com/user-attachments/assets/4bebe47c-c053-4592-8525-6616dcd6f8b2" />
  
  ### 🔗 Load
- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.  

    - 📊 data_jobs_all
    <br>
    <img width="1920" height="1080" alt="data_jobs_all (2)" src="https://github.com/user-attachments/assets/0efa5d56-a3b4-4a48-b019-42f594775732" />  

    <br> 
    
    - 🛠️ data_job_skills
  
    <br>
    <img width="1920" height="1080" alt="data_job_skills (2)" src="https://github.com/user-attachments/assets/473c74d5-65e7-4dd8-9334-1aa139c07110" />  
    <br>
