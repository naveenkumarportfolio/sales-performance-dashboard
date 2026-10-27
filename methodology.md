# Methodology
**Sales Performance & Revenue Growth Dashboard | Excel & AI-Assisted Analytics**

> **Disclaimer:** Nova Retail is a fictional business. All data in this project is illustrative, fictional data created for a learning portfolio. It does not represent real company results or real market conditions.

## Data generation
The 200 transactions were generated with a Python script using a fixed random seed. Order counts per month were set to vary (12–24 orders) so the data has ups and downs. Product, quantity and date were chosen randomly within the rules in `data_dictionary.md`. Nothing is based on real sales.

## KPI definitions
| KPI | Definition | Excel approach |
|---|---|---|
| Total Revenue | Sum of Revenue_INR | `=SUM(Sales_Data!G:G)` |
| Total Orders | Count of transaction rows (each row is one unique order) | `=COUNTA(Sales_Data!A:A)-1` |
| Total Units Sold | Sum of Quantity | `=SUM(Sales_Data!E:E)` |
| Average Order Value | Total Revenue ÷ Total Orders | `=IF(orders=0,"N/A",revenue/orders)` |

## Monthly analysis
Each month row has a first-of-month date. Revenue, orders and units use date-window formulas:
- Revenue: `=SUMIFS(Sales_Data!G:G, Sales_Data!B:B, ">="&start, Sales_Data!B:B, "<"&EDATE(start,1))`
- Orders: `COUNTIFS` with the same date window.
- Units: `SUMIFS` on Quantity with the same date window.
- Month-on-month growth: `(Current − Previous) ÷ Previous`, written as `=IF(previous=0,"N/A",(current-previous)/previous)`. January is the text "N/A" because December 2024 is not provided.

## Product and category analysis
- Revenue and units: `SUMIFS` by product or category.
- Transactions: `COUNTIFS` by product or category.
- Revenue share: item revenue ÷ total revenue (`IFERROR` guards against division by zero).
- Rank: `RANK` on revenue, highest = 1.

## Charts
Line chart (monthly revenue), horizontal bar (product revenue), column (category revenue), and a growth column chart. The growth chart uses two helper columns (growth ≥ 0 and growth < 0) so positive values are navy and negative values are red.

## Quality checks performed
- Revenue recalculated independently in Python and compared with the workbook: ₹3,82,704 in both.
- Monthly, product and category totals each reconcile to total revenue (checks are also built into the workbook).
- Growth percentages recalculated in Python and compared with Excel.
- Workbook recalculated with 0 formula errors; charts and the Excel Table (`tblSales`) preserved.
- Row count (200), product names, price match, positive integer quantities, and Revenue = Quantity × Price validated on the CSV.

## Not included
Slicers and macros are not used. Filtering is available through the Excel Table filter arrows on `Sales_Data`. The workbook does not contain an AI model; AI assistance was used only to help build and document the project.
