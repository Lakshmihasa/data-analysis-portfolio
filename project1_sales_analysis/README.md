* Retail Sales Data Analysis
End-to-End Business Intelligence Project using Python & SQL
* Project Overview

This project performs a complete end-to-end retail sales data analysis using the Sample Superstore dataset.

The objective is to:

Analyze sales performance

Identify profit drivers and loss areas

Evaluate discount impact

Segment high-value customers

Generate actionable business insights

This project simulates a real-world business analytics case study.

* Tech Stack

Python 3.12

Pandas – Data manipulation

NumPy – Numerical operations

Matplotlib & Seaborn – Visualization

SQLite – SQL-based analysis

Jupyter Notebook – Analysis workflow

Git & GitHub – Version control

* Project Structure
project1_sales_analysis/
│
├── data/
│   ├── Sample - Superstore.csv
│   └── sales_database.db
│
├── notebooks/
│   └── analysis.ipynb
│
├── visuals/
│   ├── category_sales.png
│   ├── profit_by_subcategory.png
│   ├── discount_vs_profit_scatter.png
│   ├── avg_profit_by_discount.png
│   └── top_10_customers.png
│
└── README.md

* Dataset Information

Rows: 9,994

Columns: 21

Time Period: Multiple years

Key Features:

Sales

Profit

Discount

Category / Sub-Category

Customer Details

Region

* Analysis Performed
1️⃣ Data Cleaning & Preprocessing

Checked for missing values

Verified data types

Converted date columns

Removed inconsistencies

2️⃣ Exploratory Data Analysis (EDA)

Summary statistics

Sales & Profit distribution

Category-level performance

Regional trends

Time-series monthly sales

3️⃣ Business Intelligence Insights
* Category Analysis

Technology generates highest revenue

Furniture has lower profit margins

Office Supplies consistent but moderate growth

* Discount Impact

Higher discounts strongly reduce profit

Some sub-categories show negative profit at >30% discount

* Customer Analysis

Top 10 customers contribute disproportionately to revenue

High-value customers identified using aggregation

* Sub-Category Analysis

Some products generate losses despite high sales

Requires pricing strategy revision

* Visualizations Created

Category-wise Sales Bar Chart

Profit by Sub-Category Chart

Discount vs Profit Scatter Plot

Average Profit by Discount Level

Top 10 Customers Revenue Chart

Monthly Sales Trend

Total Visualizations: 6+

* SQL Integration

The dataset was loaded into SQLite for SQL-based querying.

Example SQL Query:

SELECT Category, SUM(Sales) AS Total_Sales
FROM sales
GROUP BY Category
ORDER BY Total_Sales DESC;


This demonstrates integration of Python + SQL workflow.

* Key Business Recommendations

Reduce deep discount strategies (>30%)

Focus marketing efforts on Technology category

Re-evaluate unprofitable sub-categories

Build loyalty program for top customers

Improve pricing strategy for Furniture products

* What This Project Demonstrates

Strong data manipulation skills

Advanced EDA techniques

Data storytelling ability

SQL integration with Python

Business-focused thinking

Clean project structuring

Version control usage

* How to Run This Project
git clone <https://github.com/Lakshmihasa/data-analysis-portfolio>
cd project1_sales_analysis
pip install -r requirements.txt
jupyter notebook


Open:

notebooks/analysis.ipynb

* Future Improvements

Predictive sales forecasting

Customer segmentation using clustering

Dashboard using Power BI or Streamlit

Automated reporting pipeline

Machine Learning Forecasting

A baseline linear regression model initially performed poorly (R² = 0.03).

After adding seasonality features (Month), the improved seasonal regression model achieved:

R² Score: 0.49

MAE: ₹11,599

This demonstrates the importance of feature engineering in time-series forecasting.
