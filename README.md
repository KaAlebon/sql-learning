# sql-learning
A structured record of my SQL learning journey using free resources.
📌 Overview
This document tracks my progress as I learn SQL using free, high‑quality resources including SQLBolt, Kaggle Learn, freeCodeCamp, Khan Academy, and SQLZoo.
These notes include explanations, examples, practice queries, and reflections.

“A great free SQL resource depends on how you prefer to learn, but the strongest all‑round options are freeCodeCamp, Khan Academy, SQLBolt, Kaggle Learn, and SQLZoo.”

🧭 Learning Path
1. SQLBolt — Foundations
Short, interactive lessons covering the essentials:

SELECT

WHERE

ORDER BY

JOINs

GROUP BY

Aggregations

2. Kaggle Learn — Real Datasets
Notebook‑style learning with practical exercises.

3. freeCodeCamp — Deep Practice
Relational Database Certification using PostgreSQL.

4. SQLZoo — Challenge‑Based Practice
Progressively harder exercises to build confidence.

🧱 Core Concepts & Examples
🔹 SELECT
sql
SELECT *
FROM customers;
🔹 WHERE
sql
SELECT *
FROM orders
WHERE status = 'Late';
🔹 ORDER BY
sql
SELECT customer_id, total_spend
FROM customers
ORDER BY total_spend DESC;
🔹 JOIN
sql
SELECT o.order_id, c.customer_name
FROM orders o
JOIN customers c
  ON o.customer_id = c.customer_id;
🔹 GROUP BY & Aggregation
sql
SELECT region, COUNT(*) AS total_deliveries
FROM deliveries
GROUP BY region;
🧪 Practice Queries (My Own Work)
1. Count total deliveries
sql
SELECT COUNT(*) AS total_deliveries
FROM deliveries;
2. Count late deliveries
sql
SELECT COUNT(*) AS late_deliveries
FROM deliveries
WHERE delivery_status = 'Late';
3. Average delivery time
sql
SELECT AVG(delivery_time_minutes) AS avg_delivery_time
FROM deliveries;
📊 Portfolio Project Notes
Project: Delivery Performance SQL Analysis
Dataset: Logistics delivery dataset
Focus areas:

Late delivery rates

Average delivery time

Performance by region

Performance by courier

This project ties directly to my transport & logistics background.

📝 Reflections
SQLBolt gave me a fast, confidence‑building start.

Kaggle helped me apply SQL to real datasets.

freeCodeCamp is deeper and more structured — ideal for long‑term mastery.

SQLZoo is excellent for strengthening problem‑solving skills.

“SQLBolt is the fastest hands‑on start; Kaggle Learn gives real‑world datasets; SQLZoo builds problem‑solving skill.”

🎯 Next Steps
Complete SQLBolt

Finish Kaggle SQL course

Build full SQL case study

Add queries + documentation to GitHub

Move into Power BI + Python projects
