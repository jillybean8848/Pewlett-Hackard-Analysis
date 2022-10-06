# Pewlett-Hackard-Analysis

## Overview
The purpose of this analysis was to analyze data records for a company, "Pewlett Hackard" in order to determine who and how many employees will be retiring in the upcoming years. This analysis is essential for any company so they may be fully prepared to pay out retirement packages, fill positions that will become available, as well as begin a mentorship initiative program. 

To help "Pewlett Hackard" prepare as necessary our analysis focused strongly on criteria such as: identifying retiring employees by their titles and retrieving counts of those employees and grouping them by each title. This is helpful to know how many employees they will need to fill in each specific position. We also identified which employees were eligible for participation in the mentorship program.This is helpful to know how many qualified and retirement-ready employees would be ready to mentor future candidates and we grouped them by title and department as well. 

## Resources
"Pewlett Hackard" was able to provide us with six CSV files from their databases for us to run our analysis. They were as follows:
[departments.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9721961/departments.csv)
[dept_emp.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9721962/dept_emp.csv)
[dept_manager.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9721964/dept_manager.csv)
[employees.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9721965/employees.csv)
[titles.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9721967/titles.csv)
[salaries.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9721970/salaries.csv)

Using the following programs helped us pull these files and complete our task:
PgAdmin4
PostreSQL
QuickBD

QuickBD was useful for creating tables and flowcharts prior to diving in so that we could see the relationships between departments. Here is an example of the tables we were able to create:
![EmployeeDb png](https://user-images.githubusercontent.com/110632671/194234880-a2ae059a-a43d-4f9a-a9a8-f34902e3e783.png)

## Results
Our first query was focused on gathering information on all retiring employees. It is a large dataset with 133,776 rows. This is where an issue arises with this specific query. Because it contains all the titles that employees acquired from the entire span they worked at "Pewlett Hackard" it resulted in duplicates in cases where an employee had multiple job titles throughout their career.
[retirement_titles.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9722050/retirement_titles.csv)

To correct this issue and provide our client with a more effective and efficient list we were able to update our code using the DISTINCTON command to filter out those duplicates. We also used the ORDERBY method in order to display the data by date so that it is much easier to read:
[unique_titles.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9722086/unique_titles.csv)

Finally, so that our Human Resources department can easily look at how many postions need filled for specific titles and departments we filtered those results using GROUPBY again to show us a comprehensive list.
[retiring_titles.csv](https://github.com/jillybean8848/Pewlett-Hackard-Analysis/files/9722102/retiring_titles.csv)

## Summary 
Our data set shows that "Pewlett Hackard" should be expecting more than half of their work force to retire in the next few years. That is no small amount of employees to prepare to replace. Thank goodness for our analysis! With this information they can begin interviewing and hiring new candidates to begin the mentorship initiative program so that those who will be retiring can help train the next generation of employees. 
