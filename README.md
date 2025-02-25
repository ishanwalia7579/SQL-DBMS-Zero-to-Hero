# 📌 SQL Database Project

## 📖 Description
This project contains SQL scripts for creating and managing a database for [Ishan Walia]. It includes schema definitions, sample queries, and setup instructions.

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
 <h1> ❓ Important SQL Questions</h1>
<h3>Here are some commonly asked SQL interview questions:</h3>

<h3>🏆 Basic SQL Questions</h3>

<li>What is SQL?</li>
<li>What are the different types of SQL commands? (DDL, DML, DCL, TCL)</li>
<li>What is the difference between DELETE, TRUNCATE, and DROP?</li>
<li>What are primary keys and foreign keys?</li>
<li>What is the difference between WHERE and HAVING?</li>

<h3>🚀 Intermediate SQL Questions</h3>
<li>What are JOIN types in SQL? (INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN)</li>
<li>What is the difference between UNION and UNION ALL?</li>
<li>How does indexing work, and why is it important?</li>
<li>What is a stored procedure? Provide an example.</li>
<li>What is normalization? Explain the different normal forms.</li>

<h3>🛠 Advanced SQL Questions</h3>
<li>What is a CROSS JOIN, and when should you use it?</li>
<li>Explain CTE (Common Table Expressions) with an example.</li>
<li>What is the difference between a VIEW and a TABLE?</li>
<li>What is a trigger in SQL? Provide an example.</li>
<li>How do you optimize SQL queries for better performance?</li>

<h3>⚡ Best Practices</h3>
<li>Use Indexing: Speed up queries by indexing frequently searched columns.</li>
<li>Normalize the Database: Reduce redundancy and improve efficiency.</li>
<li>Use Transactions: Ensure data consistency with BEGIN, COMMIT, ROLLBACK.</li>
<li>Secure Your Data: Use prepared statements to prevent SQL injection.</li>
<li>Optimize Queries: Avoid SELECT *, use specific columns for better performance.</li>



<h3>📌 API Integration (Optional)</h3>
You can integrate this database with a backend using Node.js, Python (Flask/Django), Java (Spring Boot), etc..

<h5>Example:</h5> Fetch users in Python (MySQL)

```c
import mysql.connector

conn = mysql.connector.connect(host="localhost", user="root", password="password", database="database_name")
cursor = conn.cursor()
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())

```
