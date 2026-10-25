Delivery Performance Analysis Findings

Finding 1: Delivery Volume by Region
Business Question
Which region handled the most deliveries?

SQL Query
SELECT region, COUNT(*) AS delivery_count FROM deliveries GROUP BY region ORDER BY delivery_count DESC;

Results
South: 13

North: 13

West: 12

East: 12

Insight
Delivery volume is distributed evenly across all regions.

Finding 2: Delivery Status Performance
Business Question
How many deliveries were completed on time versus late?

SQL Query
SELECT status, COUNT(*) AS delivery_count FROM deliveries GROUP BY status;

Results
Late: 25

On Time: 25

Insight
Delivery performance is evenly split between late and on-time deliveries.

Operational Observation
With 50% of deliveries arriving late, improving delivery timeliness is likely to be a key operational opportunity.

Finding 3: Driver Delivery Volume
Business Question
Which driver completed the most deliveries?

SQL Query
SELECT driver, COUNT(*) AS delivery_count FROM deliveries GROUP BY driver;

Results
Jamie: 3

Jordan: 3

All other drivers: 2

Insight
Jamie and Jordan completed the highest number of deliveries in the dataset.

Operational Observation
Driver workload appears evenly distributed, with only minor differences between drivers.

Finding 4: Average Delivery Time by Region
Business Question
Which region has the longest average delivery time?

SQL Query
SELECT region, AVG(delivery_time_minutes) AS average_time FROM deliveries GROUP BY region ORDER BY average_time DESC;

Results
South: 65.69 minutes

West: 63.83 minutes

North: 42.54 minutes

East: 30.58 minutes

Insight
The South region recorded the longest average delivery time at 65.69 minutes.

Operational Observation
Although delivery volumes are evenly distributed across regions, delivery times vary significantly. The South region may benefit from further investigation to identify causes of slower delivery performance.

Follow-up Investigation

South region has both the longest average delivery time and longest average delivery distance.

Further analysis is required to determine whether longer delivery times are explained by distance alone or whether operational inefficiencies exist.

Next metric: delivery time per km by region.