# Super Store Data Cleaning & Profitability Analysis

![Project Cover Image](Project_Image.jpeg) 


## 📌 The Business Problem
A hypothetical Super Store requires comprehensive data cleaning and analysis to optimize its sales strategy. This project focuses on identifying top-performing categories based on profit margins, detecting and imputing missing data values, and isolating the top-performing products within each category to drive inventory and marketing decisions.

## 🗃️ Data Dictionary
The analysis relies on relational data detailing daily transactions and returns. Below is the schema for the primary `orders` table utilized in this project:

| Column | Data Type | Description |
| :--- | :--- | :--- |
| `row_id` | INTEGER | Unique Record ID |
| `order_id` | TEXT | Identifier for each order in the table (Connects to `returned_orders`) |
| `order_date` | TEXT | Date when the order was placed |
| `market` | TEXT | Market the order belongs to |
| `region` | TEXT | Region the customer belongs to |
| `product_id` | TEXT | Identifier of the product bought |
| `sales` | DOUBLE PRECISION | Total Sales Amount for the line item |
| `quantity` | DOUBLE PRECISION | Total Quantity for the line item |
| `discount` | DOUBLE PRECISION | Discount applied to the line item |
| `profit` | DOUBLE PRECISION | Total Profit earned on the line item |

![ERD](SuperStore_ERD.png)

## 🛠️ Tools & Techniques
*   **SQL Dialect:** PostgreSQL / Standard SQL
*   **Querying Techniques:** Common Table Expressions (CTEs), `LEFT JOIN`, `GROUP BY`, Window Functions (Ranking), Data Imputation.
*   **Environment:** DataCamp Workspace / Jupyter Notebook (`.ipynb`)

## 🔬 Methodology
To ensure accurate profitability tracking, the raw data underwent rigorous cleaning and transformation:
1.  **Missing Value Imputation:** Utilized Common Table Expressions (CTEs) to isolate records with missing values and systematically imputed them to maintain dataset integrity without skewing profit metrics.
2.  **Relational Mapping:** Executed `LEFT JOIN` operations to connect the `orders` table with the `returned_orders` data, ensuring refunded or canceled items did not falsely inflate sales figures.
3.  **Profit Margin Aggregation:** Applied `GROUP BY` clauses to aggregate financial metrics and identify the most profitable product categories overall.
4.  **Top Product Ranking:** Extracted the top 5 performing products within each distinct category to provide granular inventory insights.

## 💡 Key Insights & Findings
*(Note to self: Fill in the top 3 actual findings from your SQL notebook here before publishing)*
1.  **[Example Insight 1]:** Office Supplies yielded the highest overall profit margin despite having a lower average order value than Technology.
2.  **[Example Insight 2]:** The top 5 products in the Furniture category accounted for 40% of the category's total revenue.
3.  **[Example Insight 3]:** Imputing missing discount values revealed a hidden correlation between aggressive discounting and higher return rates in the Southern region.

---
## 💻 View the Code
You can view the full SQL queries, data cleaning steps, and analysis in the Jupyter Notebook here: 

[Click here to view the complete notebook.ipynb file](notebook.ipynb)
---
## 📬 Let's Connect
**John Fafiolu O.** | **Data Analyst** 

I specialize in transforming raw datasets into strategic business solutions using SQL, Python, R, and Excel. 
*   **LinkedIn:** [LinkedIn URL](https://www.linkedin.com/in/john-fafiolu-5475b3274/)
