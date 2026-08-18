# Sales Dashboard - Power BI

Interactive sales analysis dashboard built with Power BI, based on the "Sample Superstore" dataset (9,994 rows, 2014-2017, US sales).

## Objective

Enable a manager to explore sales by period, region, product, and customer segment through key KPIs and interactive visuals.

## Project Structure

- `data/`: cleaned dataset structured using a star schema (Fact_Sales + 4 dimension tables)
- `Sales_Dashboard.pbix`: complete Power BI file
- `Sales_Dashboard_Export.pdf`: PDF export of the dashboard
- `DAX_measures.md`: documentation of all DAX measures used

## Data Modeling

Star schema with:

- **Fact_Sales**: fact table containing sales transactions
- **Dim_Customer**, **Dim_Product**, **Dim_Location**, **Dim_Date**: dimension tables
- Dim_Date created using `CALENDAR()` in DAX and marked as the official date table

## KPIs and Measures

- Total Sales, Total Profit, Profit Margin %, Average Order Value, Number of Orders
- Month-over-Month (MoM) and Year-over-Year (YoY) Growth
- Year-to-Date (YTD)

Full details in [DAX_measures.md](./DAX_measures.md).

## Dashboard Pages

**Page 1 - Overview**: Main KPIs, sales evolution over time, top sub-categories, sales by state map, Region/Year filters.

**Page 2 - Details**: Detailed table by category/sub-category (Sales, Profit, Margin), profitability analysis by sub-category.

## Key Insights

- **Tables**, **Bookcases**, and **Supplies** have negative profit despite significant sales, likely due to excessive discounting.
- Sales show strong seasonality, with recurring peaks at the end of the year (November-December).
- **Phones** and **Chairs** are the top-performing sub-categories in terms of revenue.

## Tools Used

Power BI Desktop, Power Query, DAX
