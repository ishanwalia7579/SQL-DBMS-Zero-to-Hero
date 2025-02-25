# 📌 SQL Database Project

## 📖 Description
This project contains SQL scripts for creating and managing a database for [Project Name]. It includes schema definitions, sample queries, and setup instructions.

## 🏗 Database Schema
The database consists of the following tables:

- **users** (id, name, email, created_at)
- **orders** (id, user_id, product, amount, order_date)
- **products** (id, name, price, stock)

### 🔗 Relationships:
- `users.id` is a **foreign key** in the `orders` table.
- `products.id` is linked with `orders.product`.

## 🚀 Installation & Setup
1. Install a database management system (MySQL/PostgreSQL/SQLite).
2. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/sql-project.git
   cd sql-project

   ```
   ❓ Important SQL Questions
Here are some commonly asked SQL interview questions:

🏆 Basic SQL Questions
What is SQL?
What are the different types of SQL commands? (DDL, DML, DCL, TCL)
What is the difference between DELETE, TRUNCATE, and DROP?
What are primary keys and foreign keys?
What is the difference between WHERE and HAVING?
🚀 Intermediate SQL Questions
What are JOIN types in SQL? (INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN)
What is the difference between UNION and UNION ALL?
How does indexing work, and why is it important?
What is a stored procedure? Provide an example.
What is normalization? Explain the different normal forms.
🛠 Advanced SQL Questions
What is a CROSS JOIN, and when should you use it?
Explain CTE (Common Table Expressions) with an example.
What is the difference between a VIEW and a TABLE?
What is a trigger in SQL? Provide an example.
How do you optimize SQL queries for better performance?

