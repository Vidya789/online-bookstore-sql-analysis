
# Online Bookstore Analysis with PostgreSQL

## About this project

This is a SQL practice and portfolio project using PostgreSQL. I created three related tables for books, customers, and orders. I use SQL queries to explore the book catalog and answer basic questions about sales and customers.

The dataset appears to be sample data. I have not confirmed its original source, so the figures below should not be treated as results from a real bookstore.

## Tables and data

The project uses three CSV files:

- `Books.csv`: book title, author, genre, publication year, price, and stock.
- `Customers.csv`: customer name and contact and location fields.
- `Orders.csv`: customer, book, order date, quantity, and order amount.

The current files each contain 500 rows. In the supplied orders file, there are 2,697 book units and 307 customers with at least one order. The order dates range from December 2022 to December 2024. These are only descriptive totals from the sample files.

## Questions explored

The SQL script includes queries to explore questions such as:

- How many books are in each genre?
- Which books have the highest prices?
- How many books were sold in each genre and by each author?
- Which customers have placed multiple orders?
- Which customers and cities have higher order amounts?
- How does order activity vary by date?

## Tools and SQL skills

- PostgreSQL
- SQL joins and foreign keys
- Filtering with `WHERE`
- Aggregation with `COUNT`, `SUM`, and `AVG`
- Grouping with `GROUP BY` and filtering groups with `HAVING`
- Sorting, date filters, and subqueries

## Project files

```text
.
├── README.md
├── project_fiel.sql
├── Books.csv
├── Customers.csv
└── Orders.csv
```

## How to run

1. Install PostgreSQL and open SQL Shell (psql) or pgAdmin.
2. Keep the three CSV files in a folder on your computer.
3. Before running the SQL script, update the three CSV file paths in its `COPY` commands to match your computer.
4. The script uses the psql command `\\c OnlineBookstore` to connect to the database after creating it. This command works in SQL Shell (psql). If you use pgAdmin, create the database first, open it, and run the table and query parts there; pgAdmin does not use `\\c`.
5. Run the table creation and data import sections, then run the analysis queries.

The file paths in the current script are specific to my computer. They must be changed before another person can load the CSV files.

## Current limitations and next improvements

- The original source and license for the CSV files still need to be confirmed. If they are generated practice data, I will label them as synthetic data.
- The currency for `Price` and `Total_Amount` is not specified.
- The meaning of `Stock` needs to be confirmed before calculating remaining inventory.
- I am correcting and checking some joins and customer-spending queries before using their results.
- The SQL script currently uses local Windows file paths, so the import steps are not yet portable.

## Author

Vidya Nakade
