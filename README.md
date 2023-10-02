# HiCounselor-Projects-by-Asad-Kazmi
Live Projects


📊 HiCounselor Live Project Time Series Analysis of Medical Appointments using SQL.

📊 Project Highlights:
- Dataset Exploration: Leveraging the power of Python and Pandas, I analyzed the 'Hospital_patients_datasets.csv' dataset to gain a comprehensive understanding of the data.
- Data Cleansing: Through meticulous data processing, I identified and addressed duplicate values, null entries, and inconsistencies, ensuring the integrity of our analysis.
- Feature Engineering: Innovative techniques were employed to create new features like age groups, transforming raw data into actionable insights.
- SQL Magic: In the realm of SQL, I crafted powerful queries to uncover trends, calculate averages, and reveal hidden patterns within the dataset.
- Database Integration: Seamlessly integrating our cleaned dataset into a MySQL database, I opened the door for in-depth analysis and exploration.

📈 Key Insights Discovered:
- Busiest Days: By analyzing appointment counts per day, I identified the day with the highest number of appointments, shedding light on patient behavior and resource demand.
- Monthly Trends: Utilizing DATE_FORMAT(), I revealed the monthly average number of appointments, enabling a deeper understanding of patient engagement over time.
- Gender Distribution: Through a thoughtful SQL query, I uncovered the distribution of appointments based on gender, providing insights into potential disparities.
- Time Management: Calculating the average time between scheduling and appointment day, I highlighted critical factors influencing patient punctuality.

Edited •

📚 Code Explained: Module 1 - Data Preparation

📂 Data Cleaning and Transformation

🔍 Step 1: Reading and Checking Data
- I started by importing the essential libraries numpy and pandas to manipulate data with efficiency.

- The function `read_csv()` reads the CSV file "Hospital_patients_datasets.csv" using pandas, providing us with a Pandas DataFrame to work with.

🔄 Step 2: Detecting Duplicates and Null Values
- The function `check_duplicates()` performs a crucial task of detecting duplicate rows within the dataset, ensuring data integrity.

- With the function `check_null_values()`, I meticulously scrutinized the dataset for null (missing) values in each column, providing a clear view of data quality.

⏱️ Step 3: Converting Data Types
- Data consistency is paramount. The function `converting_dtype()` takes care of this by converting the 'ScheduledDay' and 'AppointmentDay' columns to datetime objects with date-only information.

📝 Step 4: Renaming Columns
- In the function `rename_columns()`, I ensured column names are accurate and coherent. Notably, I corrected 'Hipertension' to 'Hypertension', 'Handcap' to 'Handicap', 'SMS_received' to 'SMSReceived', and 'No-show' to 'NoShow'.

✨ Key Takeaways from Module 1:
- Data Integrity: By identifying duplicates and missing values, we ensure that our analysis is built on a strong foundation.

- Consistency: Converting data types and standardizing column names streamline further analysis and interpretation.

 Edited •

📚 Code Explained Module 2 - Advanced Data Enhancement 📈

📂 Module 2: Advanced Data Enhancement

🧹 Step 1: Dropping Unnecessary Columns
- Leveraging insights from Module 1, I imported the data through the 'module1' module.

- The function `drop_columns()` drops the columns 'PatientId', 'AppointmentID', and 'Neighbourhood', optimizing our data set for more insightful analysis.

📊 Step 2: Age Group Categorization
- With data decluttered, the function `create_bin()` addresses the intricacies of age. Rows with an age of 0 were removed, ensuring data accuracy.

- Using the Pandas `cut()` function, I divided ages into intervals ('1 - 20', '21 - 40', etc.), creating the 'Age_group' column, which provides valuable age insights at a glance.

🗑️ Step 3: Age Column
- `drop()` method bids farewell to the original 'Age' column, focusing solely on categorized age groups. This empowers us to explore age's impact without redundant data.

⚙️ Step 4: Binary Conversion
- The function `convert()` captures the essence of 'NoShow' values. By converting 'Yes' to 1 and 'No' to 0, we enable intuitive binary analysis, shedding light on patient attendance.

📦 Step 5: Exporting Cleaned Data
- In the grand finale, `export_the_dataset()` brings our refined DataFrame to life. The cleaned data, complete with age categorization and binary 'NoShow', is preserved in a new CSV file named 'patients.csv'.

🔜 Task 6: Database Integration
- I loaded the cleaned 'patients.csv' dataset into the provided database.

✨ Key Takeaways from Module 2:
- Precision Enhancement: Through column drop and age categorization, we've distilled essential insights.

- Data Transformation: Binary conversion streamlines 'NoShow' analysis, bringing clarity to patient attendance dynamics.


📊 Diving into the Depths: Module 3 - SQL Insights 🧠



In this third module of our Healthcare Appointments Analytics project, I explored some important SQL queries.

📋 Module 3: SQL Insights

📈 Query 1: Total Dataset Overview

- Starting strong, I used `SELECT COUNT(*)` to unveil the total number of values within our enriched dataset, offering a fundamental grasp of its scope and size.



🗓️ Query 2: Daily Appointments Count

- Through `SELECT AppointmentDay, COUNT(*)`, I explored the number of appointments for each day, fostering a day-to-day understanding of patient engagement.



📅 Query 3: Average Appointments Per Day

- Harnessing the power of subqueries, `AVG(appointment_count)` computes the average appointments per day, shedding light on the frequency of medical visits.



📊 Query 4: Busiest Appointment Day

- With `ORDER BY` and `LIMIT`, I pinpoint the day with the highest appointment count, uncovering when healthcare services are in highest demand.



📆 Query 5: Monthly Appointment Averages

- Through formatting with `DATE_FORMAT/`, I examined the average appointments per month, deciphering monthly trends in patient appointments.



📈 Query 6: Busiest Month for Appointments

- The month with the highest appointment count, shedding light on peak healthcare activity.



🗓️ Query 7: Weekly Appointments Overview

- Utilizing nested `GROUP BY` clauses, I showcased the yearly and weekly average appointments, providing a detailed understanding of week-to-week patient engagement.



📊 Query 8: Most Active Week

- Through enhanced grouping and sorting, I unearth the week with the highest appointment count, offering insights into the most bustling period.



🚻 Query 9: Appointments by Gender

- `SELECT Gender, COUNT(*)` dissects the distribution of appointments based on gender, contributing to a comprehensive understanding of patient demographics.



📅 Query 10: Appointments Per Weekday

- By extracting weekday names with `DAYNAME()`, I determine the number of appointments per weekday, revealing any day-specific patterns.



⏰ Query 11: Average Time Between Scheduling and Appointments

- Leveraging `DATEDIFF()`, I calculated the average time span between scheduling and the actual appointment, offering insights into patient waiting times.
