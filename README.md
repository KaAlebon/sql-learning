# 🌈 SQL Learning & Practice Hub  
### *A clean, colourful, modern space for mastering SQL fundamentals and building portfolio‑ready skills.*

## 📘 Project Description

This repository is a structured, beginner‑friendly hub for learning and practising SQL.  
It contains clear explanations, practical examples, interview‑style patterns, and a growing collection of real SQL exercises designed to build confidence and job‑ready skills.

The goal of this project is to provide a clean, organised space where I can:

- Learn SQL fundamentals step‑by‑step  
- Practise real queries using realistic datasets  
- Build a portfolio of SQL mini‑projects  
- Track progress and document learning  
- Prepare for data analyst interviews and technical screens  

This repo evolves as I learn — new notes, examples, and practice tasks are added regularly.


## 📑 Table of Contents

1. 🎯 Why SQL Matters  
2. 🧭 Recommended Learning Path  
3. 🚀 SQL Goals (Weeks 1–4)  
4. 🌈 SQL Cheatsheet  
   - SELECT  
   - WHERE  
   - ORDER BY  
   - Aggregations  
   - GROUP BY  
   - HAVING  
   - JOINs  
   - CASE  
   - Data Cleaning  
5. 🗂 Useful Patterns for Interviews  
6. 🧱 Notes Section (Optional)


🌟 SQL Learning Overview — Section 1

🎯 Why SQL Matters
SQL is the backbone of data analysis. It’s used in almost every analytics role — especially remote roles — to query databases, clean data, join tables, and build reports.

Your goal:
Become job‑ready in SQL fast enough to pass technical screens and build portfolio projects.

🧭 Your Recommended Learning Path
Based on your learning style (step‑by‑step, structured, hands‑on), these are your strongest free resources:

1. SQLBolt — Fast Foundation
Short, interactive lessons.
Perfect for quickly learning:

SELECT

WHERE

ORDER BY

JOINs

GROUP BY

Aggregations

2. Kaggle Learn — Real‑World Practice
Notebook‑style learning with real datasets.
Great for building confidence and practical skill.

3. freeCodeCamp — Deep Skill Building
Full PostgreSQL training with real projects.
Best free full‑length SQL course available.

🚀 SQL Goals (Weeks 1–4)
By the end of Week 4, you will be able to:

Write SELECT queries confidently

Join multiple tables using INNER, LEFT, and RIGHT JOIN

Filter and aggregate data with WHERE, GROUP BY, HAVING

Clean messy datasets using TRIM, COALESCE, and basic string functions

Build small SQL portfolio projects

Pass junior data analyst SQL screens and practical tests

🌈 SQL Cheatsheet — Portfolio Edition

📘 SELECT — Your First Move
SELECT column_name
FROM table_name;


🔍 Filtering Rows (WHERE)
SELECT *
FROM employees
WHERE role = 'Manager';

🎛 Sorting (ORDER BY)
SELECT name, salary
FROM employees
ORDER BY salary DESC;

📊 Aggregations (COUNT, SUM, AVG, MIN, MAX)
SELECT COUNT(*) AS total_employees
FROM employees;

SELECT AVG(salary) AS avg_salary
FROM employees;

🧮 GROUP BY — Summaries
SELECT role, COUNT(*) AS total_employed
FROM employees
GROUP BY role;

🎯 HAVING — Filters After Grouping
SELECT role, COUNT(*) AS total_employed
FROM employees
GROUP BY role
HAVING COUNT(*) > 10;

HAVING COUNT(*) > 10;

🔗 JOINs — Combining Tables

INNER JOIN
SELECT e.name, d.department_name
FROM employees e
INNER JOIN departments d
ON e.department_id = d.id;

LEFT JOIN
SELECT e.name, d.department_name
FROM employees e
LEFT JOIN departments d
ON e.department_id = d.id;

🧩 CASE — Conditional Logic
SELECT name,
       CASE
           WHEN salary > 50000 THEN 'High'
           ELSE 'Standard'
       END AS salary_band
FROM employees;

🧼 Cleaning Data
SELECT TRIM(name) AS clean_name,
       COALESCE(department, 'Unknown') AS department
FROM employees;

🗂 Useful Patterns for Interviews
Count late deliveries
SELECT COUNT(*) AS late_deliveries
FROM deliveries
WHERE delivery_status = 'Late';

Average delivery time
SELECT AVG(delivery_time_minutes) AS avg_delivery_time
FROM deliveries;

Performance by region
SELECT region, AVG(delivery_time_minutes) AS avg_time
FROM deliveries
GROUP BY region;


🧱 Notes Section (Optional)
Use this space to add your own examples, mistakes, wins, and queries as you learn.
Great places to track progress include:

Queries you struggled with but eventually solved

Real‑world examples from your transport/data work

Patterns you want to remember

Mini‑projects or datasets you plan to explore

Interview questions you’ve practised
