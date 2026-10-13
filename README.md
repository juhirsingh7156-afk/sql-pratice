# SQL Sales Data Analysis

A beginner-to-intermediate SQL portfolio project that explores sales transactions, product performance, customer spending, and monthly revenue using **MySQL 8.0+**.

## Project objective

Use SQL to answer business questions such as:
- What is the total revenue from completed orders?
- Which products and categories generate the most revenue?
- Which customers spend the most?
- How does revenue change month to month?
- Which regions have the most completed orders?
- What is the average order value?

## Tools and skills

- MySQL 8.0+
- Joins, filtering, aggregation, `GROUP BY`, `ORDER BY`
- Common table expressions (CTEs)
- Window functions: `DENSE_RANK()` and `LAG()`
- Data modeling with primary and foreign keys

## Repository structure

```text
sql-sales-analysis/
├── data/
│   ├── customers.csv
│   ├── products.csv
│   ├── orders.csv
│   └── order_items.csv
├── sql/
│   ├── 01_schema.sql
│   └── 02_analysis_queries.sql
└── README.md
```

## Database schema

- `customers`: customer profile and region
- `products`: product names, categories, and reference prices
- `orders`: order dates and statuses
- `order_items`: products, quantities, and transaction unit prices

Relationship overview:

```text
customers 1 ─── many orders 1 ─── many order_items many ─── 1 products
```

## Business rules and assumptions

- Revenue is calculated as `quantity × unit_price` from `order_items`.
- Revenue and customer-spend queries include only orders whose status is `Completed`.
- Cancelled and returned orders are excluded from these completed-order metrics.
- The dataset is fictional and designed for learning; it does not represent a real company.
- The sample contains a limited date range, so insights should not be generalized to real-world markets.

## Key SQL analyses

1. Completed order listing
2. Total revenue
3. Monthly revenue trend
4. Top five products by revenue
5. Revenue by category
6. Top customers by spend
7. Completed orders by region
8. Average order value using a CTE
9. Customers without completed orders
10. Product revenue ranking with `DENSE_RANK()`
11. Month-over-month revenue comparison with `LAG()`

## Possible improvements

- Add profit and cost fields to calculate profit margin.
- Build a Power BI or Tableau dashboard.
- Add more realistic data and more months of history.
- Add indexes and compare query performance with `EXPLAIN`.
- Add automated data-quality checks.

## Author

juhi singh
## License

This project is provided for educational and portfolio use.
