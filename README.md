Sales Performance & Revenue Growth Dashboard | Excel & AI-Assisted Analytics

Disclaimer: Nova Retail is a fictional business. All data in this project is illustrative, fictional data created for a learning portfolio. It does not represent real company results or real market conditions.

Project overview

An Excel dashboard analysing 2025 monthly sales, revenue trends, product performance, category performance and growth for Nova Retail, a fictional retail business. Built as a first portfolio project in finance and marketing analytics, with AI assistance used for generating data, building the workbook and drafting documentation.

Business problem

A retail manager wants to know: which months and products drive revenue, where revenue fell, and how to read growth. This project shows how a simple transaction table can answer those questions.

Objectives
Build a working, formula-driven Excel dashboard.
Track monthly revenue, orders, units, average order value and month-on-month growth.
Compare products and categories by revenue and share.
Write insights that agree with the calculated figures.
Dataset
sales_data.csv: 200 fictional orders, 1 Jan – 31 Dec 2025, four products, three categories, prices in INR.
Columns: Order_ID, Order_Date, Product, Category, Quantity, Unit_Price_INR, Revenue_INR. See data_dictionary.md.
Tools

Microsoft Excel (formulas, Tables, charts); Python (openpyxl, pandas) to generate data and build the file; AI assistant for drafting and quality checks.

Features
Dashboard with four KPI cards and four charts (revenue trend, revenue by product, revenue by category, monthly growth).
Excel Table (tblSales) with filter arrows; all analysis uses live formulas (SUMIFS, COUNTIFS, IFERROR, RANK).
Built-in reconciliation checks.
Insights and recommendations sheet.
Key metrics (illustrative data)
Metric	Value
Total revenue	₹3,82,704
Total orders	200
Total units sold	496
Average order value	₹1,914
Highest-revenue month	Nov 2025 (₹48,345)
Lowest-revenue month	Jul 2025 (₹16,975)
Top product	Wireless Mouse
Top category	Electronics
Methodology

Summarised in methodology.md.

How to use the workbook
Open Sales_Performance_Dashboard.xlsx in Excel.
Start on Dashboard, then see Monthly_Analysis and Product_Analysis for the numbers behind the charts.
Use filter arrows on Sales_Data to explore. Edit or add rows inside the table and the analysis sheets update (if you add dates outside 2025, adjust the month start dates).
Read Insights_and_Recommendations. The key-figures table is live; the written text is fixed to the delivered data.
Limitations
Fictional data; no conclusions about real markets.
Revenue only: no costs, margins, inventory, customers or marketing spend, so profitability cannot be assessed.
Dashboard is static (no slicers).
One order per row; no repeat-customer analysis.
Learning outcomes
Structuring transaction data and using Excel Tables.
Conditional aggregation with SUMIFS/COUNTIFS and safe division with IFERROR.
Calculating month-on-month growth and handling the first period.
Designing dashboard charts and checking numbers reconcile.
Separating what the data shows from what it cannot show.
Files

Sales_Performance_Dashboard.xlsx, sales_data.csv, README.md, Insights_and_Recommendations.md, data_dictionary.md, methodology.md
