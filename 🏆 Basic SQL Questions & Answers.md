# 📌 SQL Guide & FAQs

## 📖 Introduction
This document provides a basic understanding of SQL, including frequently asked questions, important concepts, and examples.

---

## 🏆 Basic SQL Questions & Answers

### ❓ What is SQL?
**SQL (Structured Query Language)** is a language used to interact with relational databases. It allows for inserting, updating, deleting, and retrieving data.

Example:
```sql
SELECT * FROM users;
```

---

### ❓ What are the different types of SQL commands?
SQL commands are divided into four categories:

1. **DDL (Data Definition Language)** – Defines and modifies database structure.
   - Commands: `CREATE`, `ALTER`, `DROP`, `TRUNCATE`
   - Example:
     ```sql
     CREATE TABLE students (id INT PRIMARY KEY, name VARCHAR(50));
     ```

2. **DML (Data Manipulation Language)** – Manages data within tables.
   - Commands: `INSERT`, `UPDATE`, `DELETE`, `SELECT`
   - Example:
     ```sql
     INSERT INTO students (id, name) VALUES (1, 'Ishan Walia');
     ```

3. **DCL (Data Control Language)** – Controls database access.
   - Commands: `GRANT`, `REVOKE`
   - Example:
     ```sql
     GRANT SELECT ON students TO user1;
     ```

4. **TCL (Transaction Control Language)** – Manages transactions.
   - Commands: `COMMIT`, `ROLLBACK`, `SAVEPOINT`
   - Example:
     ```sql
     BEGIN;
     UPDATE students SET name = 'Aryan' WHERE id = 1;
     ROLLBACK;
     ```

---

### ❓ What is the difference between DELETE, TRUNCATE, and DROP?

| Command  | Action | Can Be Rolled Back? | Speed | Keeps Table Structure? |
|----------|--------|---------------------|-------|------------------------|
| **DELETE** | Removes specific rows | ✅ Yes (if inside a transaction) | Slow | ✅ Yes |
| **TRUNCATE** | Removes all rows | ❌ No | Fast | ✅ Yes |
| **DROP** | Deletes the entire table | ❌ No | Fastest | ❌ No |

**Example Queries:**
```sql
DELETE FROM students WHERE id = 1;  -- Deletes a specific row
TRUNCATE TABLE students;  -- Removes all rows, resets auto-increment
DROP TABLE students;  -- Deletes the entire table
```

---

### ❓ What are Primary Keys and Foreign Keys?

#### **Primary Key**
A **Primary Key** uniquely identifies each row in a table. It cannot have `NULL` values and must be unique.

**Example:**
```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(50)
);
```

#### **Foreign Key**
A **Foreign Key** establishes a relationship between two tables. It references a **Primary Key** from another table.

**Example:**
```sql
CREATE TABLE orders (
    id INT PRIMARY KEY,
    user_id INT,
    product VARCHAR(50),
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

---

### ❓ What is the difference between WHERE and HAVING?

| Clause  | Used With | Works On | Condition Type |
|---------|----------|----------|---------------|
| **WHERE**  | `SELECT`, `UPDATE`, `DELETE` | Individual rows | Simple conditions |
| **HAVING** | `SELECT` (with `GROUP BY`) | Groups of rows | Aggregate conditions |

**Example Queries:**
- Using `WHERE`:
```sql
SELECT * FROM orders WHERE amount > 500;  -- Filters individual rows
```
- Using `HAVING`:
```sql
SELECT user_id, SUM(amount)
FROM orders
GROUP BY user_id
HAVING SUM(amount) > 500;  -- Filters based on grouped results
```

---

## 🚀 Best Practices
- **Use Indexing**: Speed up queries by indexing frequently searched columns.
- **Normalize the Database**: Reduce redundancy and improve efficiency.
- **Use Transactions**: Ensure data consistency with `BEGIN`, `COMMIT`, `ROLLBACK`.
- **Secure Your Data**: Use prepared statements to prevent SQL injection.
- **Optimize Queries**: Avoid `SELECT *`, use specific columns for better performance.

---

## 📜 Conclusion
This document provides a basic guide to SQL commands and concepts. Keep practicing queries to strengthen your understanding! 🚀

