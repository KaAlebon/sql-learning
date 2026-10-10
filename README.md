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

__________________________________________________________
   🌈 SQL FUNDAMENTALS CHEATSHEET 🌈
__________________________________________________________


🌈 SQL Cheatsheet
A clean, colourful, modern reference for SQL fundamentals.

📘 Overview
This cheatsheet provides a concise, professional summary of essential SQL concepts, including filtering, sorting, joining, grouping, and common interview patterns. It is designed to support portfolio projects, technical documentation, and interview preparation.

🎓 Skills Demonstrated
Writing clean, readable SQL queries

Filtering and sorting data

Joining relational tables

Aggregating and summarising data

Using conditional logic

Understanding interview‑ready SQL patterns

Documenting technical knowledge professionally

Creating portfolio‑ready developer documentation

🌈 SQL Cheatsheet
🌈 SELECT — Your First Move
SELECT column1, column2
FROM table;

SELECT * — select all columns

SELECT DISTINCT column — remove duplicates

💛 WHERE — Filter What Matters
SELECT *
FROM employees
WHERE role = 'Engineer';

Operators: =, !=, >, <, LIKE, IN, BETWEEN

💙 ORDER BY — Sort Your Results
SELECT *
FROM deliveries
ORDER BY delivery_time DESC;

💜 LIMIT — Keep It Focused
SELECT *
FROM customers
LIMIT 10;

💚 JOIN — Connect Your Data
SELECT e.name, d.region
FROM employees e
INNER JOIN deliveries d
  ON e.id = d.employee_id;

LEFT JOIN
SELECT e.name, d.delivery_time
FROM employees e
LEFT JOIN deliveries d
  ON e.id = d.employee_id;

🧡 GROUP BY — Summarise Your Data
SELECT role, COUNT(*) AS total_employed
FROM employees
GROUP BY role;

Aggregations: COUNT, SUM, AVG, MIN, MAX

💗 HAVING — Filter Groups
SELECT role, COUNT(*) AS total
FROM employees
GROUP BY role
HAVING COUNT(*) > 5;

💙 CASE — Conditional Output
SELECT
  delivery_id,
  CASE
    WHEN delivery_time > 5 THEN 'Late'
    ELSE 'On Time'
  END AS status
FROM deliveries;

💛 Aliases — Make It Readable
SELECT name AS employee_name
FROM employees e;

📊 Quick Reference Table
Concept	Keyword	Example
Select	SELECT	SELECT name FROM employees;
Filter	WHERE	WHERE role='Engineer'
Sort	ORDER BY	ORDER BY age DESC
Limit	LIMIT	LIMIT 5
Join	JOIN	INNER JOIN deliveries d ON …
Group	GROUP BY	GROUP BY role
Filter groups	HAVING	HAVING COUNT(*) > 5
Logic	CASE	CASE WHEN … THEN … END


⚠️ Common Mistakes
Using WHERE instead of HAVING

Forgetting GROUP BY

Using = instead of LIKE

Joining tables without an ON condition

Using SELECT * in production

🎯 SQL Interview Prep
Common Questions
Find duplicates

Top N queries

Percentage calculations

JOIN differences

Aggregation logic

Patterns to Know

Find duplicates
SELECT email, COUNT(*)
FROM customers
GROUP BY email
HAVING COUNT(*) > 1;

Top N

SELECT *
FROM orders
ORDER BY total DESC
LIMIT 5;

Percentage

SELECT
  COUNT(*) * 100.0 / (SELECT COUNT(*) FROM orders) AS pct
FROM orders
WHERE status = 'Late';

Tips
Explain your reasoning

Build queries step‑by‑step

Use aliases for clarity

Ask clarifying questions
