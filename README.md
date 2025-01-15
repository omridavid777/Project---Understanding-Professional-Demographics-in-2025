**Project - Understanding Professional Demographics in 2025**
**Background and Objective**
The objective of the project was to analyze demographic and employment data from a survey conducted with 500 participants. The process included data collection, importation to a database (Microsoft SQL Server), data processing, and the creation of an interactive report using Power BI.
**Phase 1 – Data Collection**
I created 10 survey questions:
1.	Age Group: 18-25, 26-35, 36-45, 45+.
2.	Country of Residence.
3.	Native Language.
4.	Years of Experience: 0-2, 3-6, 7-10, 10+.
5.	Profession.
6.	Education.
7.	Work Preference: Work from home, in-office, or hybrid.
8.	Important Job Aspect: Salary, work-life balance, growth opportunities, job security.
9.	Job Satisfaction: Rating 1-5.
10.	Organization Size.
I then requested ChatGPT to generate random dummy data that would match these survey questions, and asked it to create the data in a CSV file format.
**Phase 2 – Importing Data to Microsoft SQL Server**
I imported the data and created the database.
**Phase 3 – Initial Analysis in SQL**
I performed 2 example queries to verify the data integrity:
Age Distribution
SELECT Age_Group, COUNT(*) AS COUNT  
FROM SurveyResponses  
GROUP BY Age_Group;
Data Segmentation by Country
SELECT Country, COUNT(*) AS COUNT  
FROM SurveyResponses  
GROUP BY Country;
After checking the data, I made adjustments to some of the field names.
**Phase 4 – Creating Power BI Report**
Main Steps:
1.	Data Import
The data was imported into Power BI directly from Microsoft SQL Server. During the import process, I noticed an issue with the "Years of Experience" data. I identified that the ranges 03-06 and 07-10 were written incorrectly. I attempted to fix this in SQL Server, but could not make the changes. I then went into Power BI, activated Power Query, selected the "Years of Experience" column, and used the "Replace Values" function to correct the numbers.
2.	Creating Visualizations
•	Age Distribution – The goal was to display the distribution of participants by age group. I created a "Clustered Column Chart" showing the distribution of participants across the age groups.
•	Distribution by Country – The goal was to show the number of participants from each country. I created a "Clustered Column Chart" displaying the number of participants from each country and also added a map for visualization.
•	Job Satisfaction – The goal was to present job satisfaction levels based on a rating scale (1-5). I created a "Pie Chart" that displayed the distribution of satisfaction ratings.
•	Segmentation by Profession – The goal was to show the distribution of participants by profession and allow filters for job satisfaction or age group. I created a "Clustered Column Chart".
3.	Adding Slicers – I added interactive slicers for segmentation by country, age group, profession, years of experience, education, and language.
4.	Report Design
•	I added clear titles for each chart.
•	I used a color scheme.
•	I organized the layout into sections (filters, charts, and key statistics).
**Conclusions from the Report**
1.	Age Group – The largest age group was 18-25, with a relatively equal distribution across the other groups.
2.	Leading Countries – The countries with the most participants were France, Australia, and Israel.
3.	Average Job Satisfaction – The average job satisfaction rating was 3.8 out of 5, with variation across professions.
4.	Work Preferences – The majority of participants preferred hybrid work, followed by work from home.
**Summary**
The project combined SQL analysis with Microsoft SQL Server, Power BI report creation, and interaction with ChatGPT.
If additional improvements or insights are needed, further segmentation and analysis can be added as required.

