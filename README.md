# SQL_Asset4
💻Task 4: Aggregate Functions and Grouping.
This repository contains SQL code for Task 4 of the SQL Developer Internship. The task demonstrates the use of aggregate functions and grouping in SQL to analyze employee data.


📋 Task Objective
Use aggregate functions and GROUP BY to:
Summarize employee data by department.
Calculate total salary, average salary, employee count, highest salary.
Use filtering with HAVING clause.


🛠 Tools Used
DB Browser for SQLite
You can also run these queries in MySQL Workbench


📊 SQL Queries Used
This project contains simple SQL queries using the employees_01 table to practice important SQL functions like:

SUM() 	- to calculate Total value (e.g., total salary),
AVG()   - to calculate	Average value (e.g., average salary),
COUNT()	- Count of rows (e.g., number of employees),
MAX() 	- Highest value (e.g., top salary),
GROUP BY -	To group data by department,
HAVING	 - To filter grouped results.

🛠️ Sample Queries

 --Total Salary by Department
SELECT department, SUM(salary) AS total_salary
FROM employees_01
GROUP BY department;

--Average Salary by Department

SELECT department, AVG(salary) AS avg_salary
FROM employees_01
GROUP BY department;

--Total Number of Employees per Department
SELECT department, COUNT(*) AS total_employees
FROM employees_01
GROUP BY department;

--Departments with Average Salary > 55000
SELECT department, AVG(salary) AS avg_salary
FROM employees_01
GROUP BY department
HAVING AVG(salary) > 55000;

-- Highest Salary by Department
SELECT department, MAX(salary) AS highest_salary
FROM employees_01
GROUP BY department;




