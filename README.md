# (Jumia) Retail Sales Analysis – Power BI

## Overview
Built a 3-page interactive Power BI dashboard analyzing $2.3M in sales across 4 years, 4 customer segments, and 3 product categories. A big part of this project was solving data relationship problems to make sure every number on the dashboard is accurate.

## Questions Answered
- How did revenue and profit change year over year?
- Which regions and states drive the most sales?
- How do discounts affect profit?
- Which product categories perform best and worst?
- How long does shipping take across categories and regions?

## Tools Used
- Power BI: Designed the dashboard and interactive visuals.
- Power Query: Merged 4 yearly Excel files and cleaned the data.
- DAX: Created calculated measures like Total Sales, Profit Margin, and Total Orders.
- Data Modeling: Built a Star Schema and solved relationship issues between tables.

## What I Did
1. Imported and Cleaned the Data (Power Query)
- Merged 4 Excel files (one per year) into one dataset using folder-based import.
- Applied 12 cleaning steps: removed duplicates, fixed data types, cleaned text columns, and handled outliers.
- Found and fixed a shipping date that showed -358 days (caused by a wrong year entry).
- Removed unwanted text characters stuck inside the Sales and Profit columns so they could be read as numbers.

2. Built the Data Model
- Organized the tables into a Star Schema: one central fact table (Orders) connected to dimension tables (Products, Customers, Locations, Calendar).
- The Product ID column had duplicates, so I created a new unique key by combining Category + Sub-Category + ID. This gave every product its own identity and fixed the relationship.
- The Zip Code column also had duplicates across the Customers and Locations tables. I solved this by creating a separate Zip Code Bridge Table that connects both tables cleanly.
- Built a custom Calendar table using DAX for time-based analysis (Year, Quarter, Month, Day).

3. Created Measures (DAX)
- Total Sales, Total Profit, Profit Margin, Total Orders, Number of Customers, Average Shipping Duration.
- Also created helper measures for the dashboard experience: a filter counter that shows how many filters are active, and dynamic button colors that change based on user interaction.

4. Designed the Dashboard (3 Pages)
- Overview: KPI cards, sales by region, yearly trends, shipping duration by category.
- Market Analysis: Top 5 states, how discounts affect profit margins, most profitable customer segment, shipping method distribution.
- Segments & Categories: Sales and profit by segment, best sellers with the ability to drill into sub-categories, average discount by category.
- Interactive Features: Buttons that switch between Sales and Profit charts in the same space, pop-up tooltips with extra details on hover, drill-down into deeper levels, side navigation menu, and a one-click reset button to clear all filters.

## Key Insights
- Discounts above 30% consistently turn profit negative. At 80% discount, the margin drops to around -200%.
- The Consumer segment drives 46.8% of total profit, making it the most valuable customer group.
- The West region has the highest sales ($764K), but Ontario is more efficient at turning sales into profit ($321K).
- Furniture has $5.2M in sales but only $117K in profit — the weakest margin of all categories, signaling a pricing problem.
- Profit dropped steadily from $434K in 2009 to $342K in 2012, suggesting rising costs need attention.

## Dashborad 
<img width="1240" height="655" alt="image" src="https://github.com/user-attachments/assets/922f97dd-b327-46a9-ba5b-46746eaf4b9e" />

<img width="1236" height="655" alt="image" src="https://github.com/user-attachments/assets/a12b8444-4808-49f4-9186-75a7fae8d67d" />

<img width="1241" height="656" alt="image" src="https://github.com/user-attachments/assets/24f452ce-986c-4a85-844e-cc3d95aa0e41" />

<img width="1238" height="660" alt="image" src="https://github.com/user-attachments/assets/a223a0bc-de68-46fb-89ca-f7c2028bf855" />

<img width="1242" height="672" alt="image" src="https://github.com/user-attachments/assets/fc97d36f-735d-4685-841c-ebf331da66c5" />




