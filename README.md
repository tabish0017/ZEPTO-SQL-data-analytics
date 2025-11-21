# ZEPTO-SQL-data-analytics
SQL-based analysis of Zepto’s product data, including data cleaning, exploration, and insights on pricing, discounts, stock levels, and category-wise revenue.


📌 Project Overview

This project focuses on analyzing Zepto’s product and inventory dataset using SQL only.
The goal is to explore the dataset, clean inconsistent entries, and generate meaningful business insights related to pricing, discounts, stock availability, revenue estimation, and product value comparison.

The project demonstrates:

SQL table creation & schema design

Data exploration and validation

Data cleaning techniques

Business insights through advanced SQL queries

Real-world retail & inventory analysis

📁 Dataset Overview

The dataset contains product-level information for items listed on Zepto, including:

Column Name	Description
sku_id	Unique SKU identifier
category	Category of the product
name	Product name
mrp	Maximum Retail Price (in paise before cleaning)
discountPercent	Discount percentage applied
availableQuantity	Stock level
discountedSellingPrice	Effective selling price (in paise before cleaning)
weightInGms	Product weight in grams
outOfStock	Whether the product is out of stock
quantity	Package quantity information
Key Issues Identified

✔ MRP and selling price were in paise, requiring conversion to rupees
✔ Some products had MRP = 0, and were removed
✔ Duplicates and repeating product names were analyzed
✔ Missing values were checked and validated

🛠 Project Workflow
1️⃣ Table Creation

A SQL table zepto was created with appropriate datatypes and constraints.

2️⃣ Data Exploration

Counting rows

Checking for missing values

Extracting unique categories

Evaluating products in stock vs out-of-stock

Identifying duplicate product names

Finding products priced incorrectly

3️⃣ Data Cleaning

Removing entries with MRP = 0

Converting mrp and discountedSellingPrice from paise → rupees

Validating fields like weightInGms and availableQuantity

4️⃣ Business Insights (SQL Queries)

Key insight queries include:

🔹 Top 10 highest discount products

Identifies best-value items based on discount%.

🔹 High-MRP out-of-stock products

Useful for understanding demand–supply gaps.

🔹 Category-wise estimated revenue

Calculated using:
discountedSellingPrice × availableQuantity

🔹 High-value items with low discounts

Filters premium products offering minimal price cuts.

🔹 Top 5 categories with highest average discount

Shows categories with aggressive pricing strategies.

🔹 Best price-per-gram products

Helps analyze true value of quantities.

🔹 Weight-based product grouping

Products categorized into:

Low (<1000 g)

Medium (1000–5000 g)

Bulk (>5000 g)

🔹 Total inventory weight per category

Helps assess inventory load & category strength.



🚀 How to Use This Project
1️⃣ Import the Dataset

Load zepto_v2.csv into your SQL database (PostgreSQL recommended).

2️⃣ Create the Table

Run the table creation script from the SQL file.

3️⃣ Insert the Data

Insert all rows from the CSV into the table.

4️⃣ Run Data Exploration Queries

Understand the dataset structure and identify issues.

5️⃣ Run Data Cleaning Queries

Ensure the dataset is clean and analysis-ready.

6️⃣ Run Insight Queries

Execute the analytical queries to generate business insights.

📈 Skills Demonstrated

SQL data modeling

Complex query writing

Retail & inventory analysis

Data quality verification

Business insight generation
