📚 Online Bookstore Database Project
✨ Project Overview
This repository contains the complete SQL schema, data population scripts, and analytical queries for an Online Bookstore database. This project was designed to demonstrate advanced proficiency in database design, normalization, data integrity, and complex SQL querying.

The database models a fully functional e-commerce platform for books, tracking customers, authors, orders, inventory, and sales transactions.

🎯 Key Objectives
The primary goals of this project were:

Database Normalization: Design a highly normalized database schema (up to 3NF) to ensure data integrity and minimize redundancy.

Referential Integrity: Implement PRIMARY KEY and FOREIGN KEY constraints to establish clear relationships between entities (e.g., ensuring every Order is linked to an existing Customer).

Complex Querying: Develop a suite of analytical SQL queries to extract meaningful business intelligence, such as calculating best-selling authors, identifying popular genres, and determining average order values.

Stored Procedures and Views: (If applicable) Utilize advanced SQL features to simplify common operations and provide secure access to complex data structures.


Tool,Purpose
DBMS,PostgreSQL (or MySQL/SQL Server - Adjust as necessary)
SQL,"Schema creation (DDL), data manipulation (DML), and querying."
DBeaver / pgAdmin,Management and execution of SQL scripts.
GitHub,Version control for scripts and documentation.

📁 Repository Structure
The project files are organized into dedicated folders to separate schema logic from data population and analytical queries.

├── sql_scripts/
│   ├── 01_schema_creation.sql       # CREATE TABLE statements with constraints (DDL)
│   ├── 02_data_population.sql       # INSERT statements to populate the tables (DML)
│   └── 03_analytical_queries.sql    # Complex SELECT queries for analysis
├── data/
│   └── mock_data_source.csv         # (Optional) Source file used for bulk data loading
└── README.md                        # This file
📖 Database Schema Design (Conceptual Model)
The database consists of the following key tables:


Table Name,Description,Key Relationships
Customers,"Stores customer profile information (Name, Email, Address).",
Authors,"Tracks author details (Name, Biography).",One-to-Many with Books
Books,"The core inventory (Title, ISBN, Price, Publication Date).",Many-to-Many with Authors (via BookAuthors)
Orders,"Records each customer transaction (OrderDate, Status, TotalAmount).",One-to-Many with OrderItems
OrderItems,"Details the books included in a specific order (Quantity, Price at time of order).",Many-to-One with Books and Orders
Genres,"Categorizes books (Fiction, Science, History).",Many-to-Many with Books (via BookGenres)



🔎 Analytical Queries & Insights
The 03_analytical_queries.sql file contains complex queries designed to answer key business questions, including:

Query Focus,Example Insight Provided,SQL Techniques Demonstrated
Sales Performance,Calculate the Total Revenue and Profit Margin per month.,"Window Functions, Aggregation (SUM), Date Functions."
Top Sellers,Identify the top 5 best-selling books and their respective authors.,"JOIN statements, GROUP BY, ORDER BY, LIMIT."
Customer Behavior,Determine the average dollar value of an order for high-value vs. low-value customers.,"Subqueries, Conditional Aggregation (CASE WHEN)."
Inventory Status,"List books with low stock (e.g., less than 10 units) that need reordering.","WHERE clauses, LEFT JOIN (to find missing data)."

🚀 How to Run the Project
To recreate and explore this database:

Install/Setup PostgreSQL (or your chosen DBMS).

Create a New Database:
CREATE DATABASE bookstore_db;

some insights in my SQL:
![Alt Text](https://github.com/sumansamantapku-rgb/SQL-project-on-Online_Bookstore/blob/main/Screenshot%202025-11-08%20114747.png?raw=true)
![Alt Text](https://github.com/sumansamantapku-rgb/SQL-project-on-Online_Bookstore/blob/main/Screenshot%202025-11-08%20114807.png?raw=true)
![Alt Text](https://github.com/sumansamantapku-rgb/SQL-project-on-Online_Bookstore/blob/main/Screenshot%202025-11-08%20114825.png?raw=true)




🤝 Contribution
Feedback and suggestions are welcome! If you spot any potential schema improvements or complex query challenges, please feel free to open an issue.
