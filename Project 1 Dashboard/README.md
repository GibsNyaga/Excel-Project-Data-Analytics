# **Excel Salary Dashboard**  

<img width="800" height="401" alt="Dashboard_GIF" src="https://github.com/user-attachments/assets/4ac604be-4b65-4896-8743-472c38789e3b" />  

# **Introduction**
I created this data jobs salary dashboard to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  
It was a learning project for me and I give all the credit to [Luke Barousse](https://github.com/lukebarousse)  

# **Dashboard File**  
My final dashboard is in [1_Salary_Dashboard.xlsx](./Project%201%20Dashboard/Salary%20Dashboard.xlsx)  

# **Excell Skills Used**  
I utilized the following Excel skills for analysis:

- 📉 Charts  
- 🧮 Formulas and Functions  
- ❎ Data Validation    

# **Data Job Dataset**  
The dataset I used for this project contains real-world data science job information from 2023. The dataset is available here [Dataset](https://github.com/GibsNyaga/Excel-Project-Data-Analytics/tree/main/Datasets)  
It includes detailed information on:  
- 👨‍💼 Job titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Skills

# **Dashboard Build**  

📉 Charts  

📊 Data Science Job Salaries - Bar Chart   

<img width="1359" height="887" alt="Job_Salaries_Bar_Chart" src="https://github.com/user-attachments/assets/a447fd39-2bfc-4d6b-b4ad-313d40ae23d6" />
<br>

- 🛠️ **Excel Features**: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice**: Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization**: Sorted job titles by descending salary for improved readability.  
- 💡 **Insights Gained**: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.  

🗺️ **Country Median Salaries - Map Chart**  

<img width="800" height="489" alt="Country_GIF" src="https://github.com/user-attachments/assets/e80c28c6-5dfc-4ba1-b175-41300fc62253" />  
<br>  

- 🛠️ **Excel Features**: Utilized Excel's map chart feature to plot median salaries globally.  
- 🎨 **Design Choice**: Used a color-coded map to visually differentiate salary levels across regions.  
- 📊 **Data Representation**: Plotted median salary for each country with the available data.  
- 👁️ **Visual Enhancement**: Improved readability and immediate understanding of geographic salary trends.  
- 💡 **Insights Gained**: Enables quick grasp of global salary disparities and highlights high/low salary regions.  

### 🧮 **Formulas and Functions**  

💰 Median Salary by Job Titles  

```=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering**: Checks job title, country, schedule type, and excludes blank salaries.  
- 📊 **Array Formula**: Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.  
- 🎯 **Tailored Insights**: Provides specific salary information for job titles, regions, and schedule types.  
- 🔢 **Formula Purpose**: This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ **Background Table**  

<img width="429" height="327" alt="Background_Table" src="https://github.com/user-attachments/assets/2f9ed070-7b3e-44e9-b171-3ef66c1abbd4" />
<br>  

📉 **Dashboard Implementation** 

<img width="603" height="756" alt="Dashboard_Implementation" src="https://github.com/user-attachments/assets/d6d23d63-91dd-4d31-ba60-585b7a293b1c" />  
<br>  

⏰ **Count of Job Schedule Type**  
```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
- 🔍 **Unique List Generation**: This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.  
- 🔢 **Formula Purpose**: This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ **Background Table**  

<img width="356" height="201" alt="Background_Table2" src="https://github.com/user-attachments/assets/36b5ff49-c038-46e7-ab8c-d499fe2cbe9b" />  
<br>  

📉 **Dashboard Implementation**  

<img width="503" height="754" alt="Dashboard_Implementation2" src="https://github.com/user-attachments/assets/b2d6b546-75c1-49ab-ac21-b7798b1cb15e" />  
<br>  

❎ **Data Validation**  
🔍 Filtered List  
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:  
    - 🎯 User input is restricted to predefined, validated schedule types.  
    - 🚫 Incorrect or inconsistent entries are prevented.  
    - 👥 Overall usability of the dashboard is enhanced.

<img width="636" height="750" alt="Title_GIF" src="https://github.com/user-attachments/assets/c785a238-db90-4e32-b901-eb312512aa44" />  

# Conclusion  
I created this dashboard alongside [Luke Barousse](https://github.com/lukebarousse) to showcase insights into salary trends across various data-related job titles, and in the process I was learning on how to clean and gain insights from data using MS Excel. This dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.





