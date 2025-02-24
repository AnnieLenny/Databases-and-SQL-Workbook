# Workbook: Exploring SQL Queries & Database Relationships

## Overview

In this workbook, I explored various concepts and techniques related to **SQL queries** and **database relationships**. The focus was on understanding **primary** and **foreign keys**, their roles in creating relationships between tables, and how to normalize data to optimize database performance. Through hands-on exercises, I researched and applied different types of joins, query syntax, and learned about the differences between **relational** and **non-relational** databases. 🧑‍💻💡

### Key Concepts Explored:

#### **Primary & Foreign Keys** 🔑:

- **Primary Key**:
  - A **primary key** is a column (or a set of columns) that uniquely identifies each record in a table. It is essential for maintaining the integrity of the data.
  
- **Foreign Key**:
  - A **foreign key** is a column in one table that **links** to the **primary key** of another table, establishing a relationship between the two tables.

#### **Types of Relationships** 🔄:

- **One-to-One Relationship**:  
  - Each record in one table is associated with exactly one record in another table. This relationship is used for linking two related entities that are typically represented in different tables.
  
- **One-to-Many Relationship**:  
  - A record in one table can be linked to multiple records in another table. This is the most common type of relationship in relational databases.
  
- **Many-to-Many Relationship**:  
  - Multiple records in one table can be linked to multiple records in another table. A **junction table** is often used to manage this relationship.

#### **Normalization** 🧹:

- **What is Normalization?**:
  - **Normalization** is the process of breaking down a large, complex table into smaller, simpler tables while maintaining the relationships between the data. This helps improve data integrity and reduces redundancy.
  
- **Importance of Normalization**:
  - **Reduces redundancy**: By eliminating duplicate data, we save space and maintain data consistency.
  - **Improves query performance**: Smaller tables lead to faster queries as there is less data to scan.
  - **Minimizes update anomalies**: Reduces the chances of inconsistencies during updates, deletions, or insertions.

#### **Relational vs Non-Relational Databases** 🗄️:

- **Relational Databases**: Use structured tables with predefined schemas, suitable for handling structured data with complex relationships (e.g., MySQL, PostgreSQL).
  
- **Non-Relational Databases**: Handle unstructured data and are more flexible, allowing for scalable and agile development (e.g., MongoDB, Cassandra).

#### **SQL Query Syntax** 🔍:

- **Simple Queries**:
  - `SELECT * FROM products;`: Retrieves all columns from the **products** table.
  - `SELECT * FROM customers;`: Retrieves all columns from the **customers** table.

#### **Types of SQL Joins** 🔗:

- **Self-Join**: A join between a table and itself, typically used to compare rows within the same table.
- **Right Join**: Includes all records from the right table, and the matched records from the left table.
- **Full Join**:  Combines the results of both **left** and **right joins**, including all records from both tables, with matching rows where available.
- **Cross Join**: Returns the Cartesian product of the two tables (all combinations of rows).
- **Left Join**: Includes all records from the left table, and the matched records from the right table.

### Sample SQL Queries:

```sql
-- Simple SELECT queries
SELECT * FROM products;
SELECT * FROM customers;

-- Join Example: LEFT JOIN
SELECT customers.name, products.product_name 
FROM customers 
LEFT JOIN products ON customers.id = products.customer_id;
