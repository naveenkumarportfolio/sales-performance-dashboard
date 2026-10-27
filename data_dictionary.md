# Data Dictionary
**Sales Performance & Revenue Growth Dashboard | Excel & AI-Assisted Analytics**

> **Disclaimer:** Nova Retail is a fictional business. All data in this project is illustrative, fictional data created for a learning portfolio. It does not represent real company results or real market conditions.

File: `sales_data.csv` (same data as the `Sales_Data` sheet). One row = one order; 200 rows.

| Column | Type | Business meaning | Rules |
|---|---|---|---|
| Order_ID | Text | Unique identifier of an order, format `NR-2025-0001`. | Unique in this simplified dataset. |
| Order_Date | Date | Date the order was placed. | ISO format `YYYY-MM-DD` in the CSV; shown as `DD-MMM-YYYY` in Excel. All dates fall within 2025-01-01 to 2025-12-31. |
| Product | Text | Product sold. | One of: Wireless Mouse, USB-C Hub, Notebook Set, Desk Organizer. |
| Category | Text | Product group. | Electronics (Wireless Mouse, USB-C Hub), Stationery (Notebook Set), Office Supplies (Desk Organizer). |
| Quantity | Integer | Number of units in the order. | Positive whole number. |
| Unit_Price_INR | Integer | Selling price per unit in Indian Rupees. | Matches catalogue: Mouse 799, USB-C Hub 1,499, Notebook Set 299, Desk Organizer 599. |
| Revenue_INR | Integer | Order revenue in INR. | Quantity × Unit_Price_INR. A formula in Excel. No discounts or taxes. |

**Not included:** costs, margins, taxes, discounts, inventory, customer identifiers, marketing spend.
