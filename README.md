# Walmart E-Commerce Analytics Dashboard

## Project Overview
This project analyzes Walmart's e-commerce performance, focusing on sales trends, product categories, and regional performance. I built this using **Power BI Desktop** and utilized the **Power BI Project (.pbip)** format to demonstrate professional version control and code transparency.

## Technical Workflow 
To ensure this project meets professional BI engineering standards, I implemented:
* **Power BI Project Files (.pbip):** I moved away from monolithic .pbix files to human-readable metadata, allowing for granular tracking of DAX and M-code.
* **Git Version Control:** Managed the development lifecycle through GitHub, ensuring clear commit history and logic transparency.
* **Security & Parameterization:** Implemented API security by removing sensitive tokens and using parameters for data connections.

## Key Business Insights
* **Metric 1:** (e.g., Total sales increased by 15% in Q4).
* **Metric 2:** (e.g., Electronics outperformed all other categories by 20%).

## DAX & Logic Highlights
Rather than just "drag-and-drop," I used advanced DAX to solve complex business questions. 

**Example: Year-over-Year Growth**
```dax
YoY Sales = 
VAR CurrentSales = [Total Sales]
VAR PreviousSales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
RETURN
DIVIDE(CurrentSales - PreviousSales, PreviousSales)
