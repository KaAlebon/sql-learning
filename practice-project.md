## 🧪 SQL Practice Project Template

### 📂 Project Title  
Short, descriptive name for your practice project.  
Example: *Delivery Performance Analysis*

---

### 🎯 Objective  
What question or problem are you solving with SQL?  
Example: *Analyse delivery times to identify slow regions and late‑delivery patterns.*

---

### 🗃 Dataset Description  
Describe the tables you’re using.  
Example:

**deliveries**  
- id  
- region  
- delivery_time_minutes  
- delivery_status  

**drivers**  
- driver_id  
- name  
- region  

---

### 🔍 Key Questions  
List the queries you plan to write.

- How many deliveries were late?  
- What is the average delivery time per region?  
- Which drivers have the highest late‑delivery rate?  
- What regions consistently perform above/below average?

---

### 🧠 SQL Queries  
Add your actual SQL queries here as you complete them.

```sql
SELECT COUNT(*) AS late_deliveries
FROM deliveries
WHERE delivery_status = 'Late';


SELECT region, AVG(delivery_time_minutes) AS avg_time
FROM deliveries
GROUP BY region;


📊 Findings & Notes
Summarise what you discovered:



🧱 Improvements / Next Steps
What would you explore next?
