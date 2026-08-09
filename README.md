# Brazilian_e-commerce
End to end data analysis project exploring delivery performance, customer satisfaction, revenue drivers, and fulfillment health using Olist's  public e-commerce dataset.
## Dataset
[Brazilian E-Commerce Public Dataset by Olist](kaggle)
- 6 relational tables(orders, order items, products, customers, payments, reviews) covering 100K orders from 2016-2018.
## Tools
- **Python(pandas)** - data cleaning, data merging, exploratory analysis
- **SQL (SQLite)** - query validation, cross-checking pandas results
- **Power BI** - interactive dashboard
## Data Cleaning
- Merged 6 tables into a single order item level dataset(119K rows)
- Converted data columns to datetime; handled undelivered orders via a boolean flag rather than dropping rows
- Filled missing product metadata and review text appropriately (medians, "unknown" category, empty strings) based on what each null actually meant
- Translated product categories from Portuguese to English
- Verified zero duplicate rows and consistent dtypes across the dataset
## Business Questions & Key Findings
**1: Delivery vs Satisfaction**
 Late deliveries average 2.55 stars vs 4.21 stars for on time deliveries, which shows a steep satisfaction drop, despite late orders being only 8% of deliveries.
**2: Category Revenue vs Rating** 
'health_beauty' leads in both revenue and rating. bed_bath_table is on 3rd spot in revenue but underperforms on satisfaction(only 3.92 stars), popular but a customer experience gap worth investigating.
**3: Payment Methods**
Credit card is used in 74% of orders and has the highest average order value. Installments weakly correlates with price(r=0.28).
**4: Geography**
SP drives the most orders and revenue but, has the lowest avg. orders value. Its a volume driven market rather than a high spend one.
**5: Fulfillment Health**
97.1% delivery success rate. No major state/category red flags, except orders with missing category data(32.8% problem rate, a data quality issue).
All findings were validated independently in both pandas and SQL, with matching results.
