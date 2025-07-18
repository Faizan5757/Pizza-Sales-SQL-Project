🍕 Pizza Sales Analysis Using SQL

📌 Project Overview
This project focuses on analyzing pizza sales data using SQL to uncover valuable business insights. The analysis includes revenue trends, popular pizza types and sizes, order distribution by time, and category-wise contributions. These insights can help optimize menu offerings and improve decision-making.

🎯 Objective
To analyze pizza sales data and answer key business questions such as:
What is the total revenue generated?
Which is the most popular pizza size?
What are the top-selling pizza types?
When is the peak ordering time?
Which pizzas contribute the most to revenue?

📊 Dataset Details
The dataset consists of four tables:
1. orders
order_id – Unique identifier for each order
date – Date of the order
time – Time of the order
2. order_details
order_id – Foreign key referencing orders
pizza_id – Foreign key referencing pizzas
quantity – Number of pizzas ordered
3. pizzas
pizza_id – Unique identifier for pizza
pizza_type_id – Links to pizza type
size – Pizza size (S, M, L, XL)
price – Price of the pizza
4. pizza_types
pizza_type_id – Unique pizza type identifier
name – Pizza name
category – Category of pizza (Veg, Non-Veg, etc.)
ingredients – Ingredients used

🛠 Tools Used
Database: MySQL
Queries: SELECT, JOIN, GROUP BY, ORDER BY, Aggregate Functions, Window Functions
Optional Visualization: Excel / Power BI (for insights presentation)

✅ Key Analysis Performed
Total Orders & Revenue
Highest Priced Pizza
Most Common Pizza Size
Top 5 Most Ordered Pizza Types
Category-wise Quantity Sold
Distribution of Orders by Hour
Average Pizzas per Day
Top 3 Pizzas by Revenue
Percentage Contribution of Each Pizza Type to Revenue
Cumulative Revenue Over Time
Top 3 Pizzas by Revenue per Category

🔍 Key Insights
✔ Total Orders: 21,350
✔ Total Revenue: $817,860
✔ Most Popular Size: Large
✔ Peak Ordering Time: 12 PM – 1 PM
✔ Top Pizza by Revenue: Thai Chicken Pizza

📌 Questions Covered
✅ Basic Queries
1. Retrieve the total number of orders placed.
2. Calculate the total revenue generated from pizza sales.
3. Identify the highest-priced pizza.
4. Identify the most common pizza size ordered.
5. List the top 5 most ordered pizza types along with their quantities.

✅ Intermediate Queries
6. Join the necessary tables to find the total quantity of each pizza category ordered.
7. Determine the distribution of orders by hour of the day.
8. Join relevant tables to find the category-wise distribution of pizzas.
9. Group the orders by date and calculate the average number of pizzas ordered per day.
10. Determine the top 3 most ordered pizza types based on revenue.

✅ Advanced Queries
11. Calculate the percentage contribution of each pizza type to total revenue.
12. Analyze the cumulative revenue generated over time.
13. Determine the top 3 most ordered pizza types based on revenue for each pizza category.

🧾 SQL Queries
Here are some sample queries used in the project:

✅ 1. Total Number of Orders
SELECT 
    COUNT(order_id) AS total_orders
FROM
    orders;

✅ 2. Total Revenue
SELECT 
    ROUND(SUM(orders_details.quantity * pizzas.price),
            2) AS total_sales
FROM
    orders_details
        JOIN
    pizzas ON pizzas.pizza_id = orders_details.pizza_id;

✅ 3. Highest Priced Pizza
SELECT 
    pizza_types.name, pizzas.price
FROM
    pizza_types
        JOIN
    pizzas ON pizza_types.pizza_type_id = pizzas.pizza_type_id
ORDER BY pizzas.price DESC
LIMIT 1;

(Find all queries in the file: pizza_sales_analysis.sql.)

📂 Project Structure
Pizza-Sales-SQL-Project/
│
├── README.md                
├── pizza_sales_analysis.sql # Combined SQL file (all queries)
├── Questions List.txt       # List of all questions
├── queries/                 # Individual query files
│    ├── Question 1.sql
│    ├── Question 2.sql
│    └── ... Question 13.sql
├── dataset/                 # CSV files
│    ├── orders.csv
│    ├── orders_details.csv
│    ├── pizzas.csv
│    └── pizza_types.csv

▶ How to Run
Install MySQL and create a database.
Import the pizza sales dataset (tables: orders, orders_details, pizzas, pizza_types).
Run queries from pizza_sales_analysis.sql file in MySQL Workbench or any SQL client.

🏷 Tags
#SQL #DataAnalysis #MySQL #PizzaSales #PortfolioProject #BusinessInsights

👤 Author
Faizan Shaikh
📌 [LinkedIn Profile](https://www.linkedin.com/in/faizan-shaikh-fs2004/) | 
📌 [GitHub Profile](https://github.com/Faizan5757)
✅ [Live GitHub Repository](https://github.com/Faizan5757/Pizza-Sales-SQL-Project)
