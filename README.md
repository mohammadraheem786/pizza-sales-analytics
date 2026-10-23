# 🍕 Pizza Palace Sales & Revenue Intelligence

An end-to-end data analytics and business intelligence project using **Python (Pandas)** for ETL/feature engineering and **Power BI (DAX)** for executive dashboarding.

![Dashboard Preview](/Images/Pizza_Sales_Dashboard.png)

---

## 📌 Project Overview
This project analyzes a full year of transactional data (2015) across 358 operating days to uncover peak ordering hours, seasonal revenue trends, category performance, and menu optimization opportunities.

### Key Performance Indicators (Full Year)
* **Total Gross Revenue:** $817.86K
* **Total Pizzas Sold:** ~50K (49,574 units)
* **Total Unique Orders:** ~21K (21,350 orders)
* **Average Order Value (AOV):** $38.31
* **Average Pizzas Per Order:** 2.32

---

## 🛠️ Tech Stack & Workflow
1. **Data Cleaning & ETL (`Pizza_Data_Analysis.ipynb`):**
   * Handled character encoding exceptions (`windows-1252`) across raw relational CSV tables (`orders.csv`, `order_details.csv`, `pizzas.csv`, `pizza_types.csv`).
   * Merged 4 relational tables into a unified analytical dataset (`master.csv` / `master.xlsx`).
   * Engineered calendar sorting keys, 12-hour AM/PM time labels, meal rush buckets (*Lunch Rush*, *Afternoon Lull*, *Dinner Rush*), and expanded size labels.
2. **Data Modeling & Dashboarding (`pizza_sales_dashboard.pbix`):**
   * Authored custom DAX measures for Revenue, Order Volume, AOV, and Basket Size.
   * Configured chronological custom column sorting for months, weekdays, and AM/PM hours.
   * Designed an interactive 16:9 executive view with dynamic slicers (`Category`, `Pizza Size`, `Quarter`, `Meal Period`).

---

## 🔍 Key Business Insights
* **Bimodal Rush Hours:** Order volume peaks sharply during the **Lunch Rush (12:00 PM – 1:00 PM)** and **Dinner Rush (6:00 PM – 7:00 PM)**.
* **Size Revenue Dominance:** **Large** pizzas generate the highest revenue share ($0.38M), followed by **Medium** ($0.25M) and **Small** ($0.18M).
* **Category Balance:** Revenue is well-distributed across categories, led by **Classic ($220.05K)**, **Supreme ($208.2K)**, **Chicken ($195.92K)**, and **Veggie ($193.69K)**.
* **Menu Optimization:** *The Thai Chicken Pizza*, *The Barbecue Chicken Pizza*, and *The California Chicken Pizza* lead top-line sales, while *The Brie Carre Pizza* ($12K) and *The Green Garden Pizza* ($14K) underperform and are candidates for recipe or promotional review.

---

## 📂 Repository Files
* `Pizza_Data_Analysis.ipynb` — Python Jupyter Notebook for data cleaning, merging, and feature engineering.
* `pizza_sales_dashboard.pbix` — Interactive Power BI Desktop file.
* `master.csv` / `master.xlsx` — Cleaned, unified analysis-ready datasets.
* `orders.csv`, `order_details.csv`, `pizzas.csv`, `pizza_types.csv` — Raw relational source tables.