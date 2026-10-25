🌈 SQL Learning & Practice Hub
A portfolio documenting my journey from SQL fundamentals to real-world data analysis projects.

Current Project
📦 Delivery Performance Analysis

Using SQL and SQLite to investigate:

Delivery volumes
Delivery performance
Driver activity
Regional trends
Operational efficiency
Repository Structure
sql-learning/
│
├── Data
├── Docs
├── SQL
└── README.md
Skills Demonstrated
SQL
SQLite
Data Analysis
Business Question Development
Documentation of Findings
Current Progress
✅ Kaggle SQL Certificate completed

✅ First SQL portfolio project underway

✅ SQLite database created and analysed

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
