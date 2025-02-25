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
