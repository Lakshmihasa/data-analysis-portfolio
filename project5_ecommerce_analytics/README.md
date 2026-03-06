E-commerce Analytics: Customer Segmentation & Recommendation System
Project Overview

This project analyzes e-commerce transaction data to understand customer purchasing behavior and product relationships. The analysis focuses on identifying customer segments and building a product recommendation system.

Using RFM analysis, machine learning clustering, and market basket analysis, this project demonstrates how businesses can improve customer targeting, marketing strategies, and cross-selling opportunities.

Objectives

Analyze customer purchasing behavior

Segment customers based on their buying patterns

Identify high-value customers

Discover product associations

Build a recommendation system using purchase patterns

Dataset

The dataset contains online retail transaction data.

Key Features
Column	Description
InvoiceNo	Unique transaction identifier
StockCode	Product identifier
Description	Product name
Quantity	Number of units purchased
InvoiceDate	Date and time of purchase
UnitPrice	Price per product
CustomerID	Unique customer identifier
Country	Customer location
Data Preprocessing

The dataset was cleaned and prepared before analysis.

Steps Performed

Removed missing customer IDs

Removed invalid or negative purchase quantities

Converted transaction dates to datetime format

Created a new feature: TotalPrice

TotalPrice = Quantity × UnitPrice
Customer Segmentation (RFM Analysis)

Customers were analyzed using RFM metrics.

Metric	Description
Recency	Days since last purchase
Frequency	Number of transactions
Monetary	Total spending by customer

These metrics help identify customer engagement and value.

Machine Learning: K-Means Clustering

Customers were segmented using K-Means clustering.

Process

Standardized RFM features using StandardScaler

Applied K-Means clustering algorithm

Grouped customers into behavioral segments

Customer Segments

High-value loyal customers

Frequent buyers

Occasional shoppers

Low engagement customers

This segmentation helps businesses personalize marketing strategies.

Market Basket Analysis

Market basket analysis was used to discover product combinations frequently purchased together.

Algorithm Used

Apriori Algorithm

This algorithm identifies frequent product combinations in transaction data.

Association Rule Mining

Association rules were generated to find relationships between products.

Important metrics used:

Metric	Meaning
Support	Frequency of item combination
Confidence	Probability of purchasing item B if A is purchased
Lift	Strength of relationship between items

Example rule:

If a customer buys Product A → Recommend Product B

This forms the basis of recommendation systems used in e-commerce platforms.

Visualizations

The project includes visual insights such as:

Customer segmentation plots

RFM distribution analysis

Association rule strength visualization

These help interpret customer behavior patterns.

Project Structure
project5_ecommerce_analytics
│
├── data
│   ├── data.csv
│   └── product_recommendations.csv
│
├── notebooks
│   └── 01_customer_segmentation_and_recommendations.ipynb
│
├── visuals
│   └── association_rules.png
│
└── README.md
Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Seaborn

Mlxtend

Jupyter Notebook

Key Business Insights

Identified valuable customer segments

Discovered product combinations frequently purchased together

Developed a recommendation system for cross-selling

Demonstrated how analytics can improve marketing strategies

Outcome

This project demonstrates how data analytics and machine learning techniques can be applied to improve customer understanding and product recommendations in e-commerce businesses.

Author

Lakshmi Hasa
Data Analytics Portfolio
