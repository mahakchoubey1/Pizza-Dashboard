# 🍕 Pizza Sales Analytics Dashboard — Power BI Project
📊 End-to-End Business Intelligence Project

This project analyzes real pizza sales data using Power BI, DAX, and data modeling to uncover sales trends, top-performing pizzas, revenue drivers, and customer buying behavior.

🚀 Project Overview

This dashboard delivers actionable insights from a pizza store’s order data.
It covers:

Total revenue

Total orders

Best-selling pizzas

Category-wise performance

Time-based revenue trends

Size-wise sales analysis

Top-N product insights (Top 5, Top 10)

The project follows a complete BI lifecycle:

Data Import

Cleaning & Transformation (Power Query)

Data Modeling (Star Schema)

DAX Measure Creation

Interactive Dashboard Design

Business Insights & Recommendations

🛠️ Tech Stack Used

Power BI Desktop

Power Query (ETL)

DAX (Data Analysis Expressions)

Star Schema Modeling

📁 Dataset Description

The project uses 4 main CSV files:

Table Name	Description
pizzas	Contains pizza size, price, type
pizza_types	Contains pizza category, ingredients
orders	Contains order date & time
order_details	Contains pizza_id, quantity per order

This structure supports a fact–dimension model, ideal for BI reporting.

⭐ Data Model (Star Schema)
pizza_types (Dimension)
        │
     1  │   *
        ▼
pizzas (Dimension)
        │
     1  │   *
        ▼
order_details (Fact)
        │
     *  │   1
        ▼
orders (Dimension)


This model ensures high performance and accurate aggregations.

📐 Key DAX Measures
Total Revenue =
SUMX(order_details, order_details[quantity] * RELATED(pizzas[price]))

Total Quantity Sold =
SUM(order_details[quantity])

Total Orders =
DISTINCTCOUNT(order_details[order_id])

Average Order Value =
[Total Revenue] / [Total Orders]

Total Pizzas Sold =
DISTINCTCOUNT(order_details[pizza_id])

📊 Dashboard Features
📌 1. KPIs

Total Revenue

Total Orders

Total Quantity Sold

Average Order Value (AOV)

Total Unique Pizzas Sold

📌 2. Visual Analysis

Revenue by Pizza Category

Quantity Sold by Pizza Size

Top 5 Pizzas by Revenue

Top 10 Pizzas by Quantity

Revenue Trend Over Time

Orders by Hour of Day

Daily & Monthly Revenue Trend

📌 3. Interactive Slicers

Category

Size

Date

Month & Year

Pizza Name

🔍 Business Insights
✔ Classic pizzas contribute the highest share of revenue
✔ Large (L) size pizzas dominate total sales
✔ Revenue spikes noticeably on weekends
✔ A few pizzas contribute majority of revenue (Pareto principle)
✔ Some pizzas underperform consistently — low demand items
✔ Strong monthly trends can guide marketing & inventory planning
🧠 What I Learned

Building full BI pipelines

Creating star schemas

Writing DAX measures for KPIs & Top-N insights

Designing clean, business-ready dashboards

Applying time intelligence (month/year/day analysis)

Turning raw data into actionable insights

## 📸 Dashboard Screenshots



### Category Analysis
![Category Analysis](https://github.com/mahakchoubey1/Pizza-Dashboard/blob/main/Screenshot%202025-11-18%20163802.png)

### Top Pizzas
![Top Pizzas](https://github.com/mahakchoubey1/Pizza-Dashboard/blob/main/Screenshot%202025-11-18%20163821.png)

### Insights
![Dashboard Insight](https://github.com/mahakchoubey1/Pizza-Dashboard/blob/main/Screenshot%202025-11-18%20163851.png)


🗂️ How to Use This Repo

Download the .pbix file

Open in Power BI Desktop

Explore/modify visuals and DAX calculations

📬 Contact

If you want the .pbix file or want help with your own dashboard, feel free to reach out! 

