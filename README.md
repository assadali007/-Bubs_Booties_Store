# Bubs Booties Store Database Management

<img width="853" height="534" alt="Screenshot" src="https://github.com/user-attachments/assets/a758ffab-755c-4f13-afef-4aead22c42e2" />

## Project Overview
This project involves designing a relational database for a retail store to efficiently manage and track customers, employees, products, and customer purchases. The database demonstrates practical SQL skills including table creation, relationships, constraints, and queries.

## Tables and Structure
1. **Customers**
   - `customer_id` (Primary Key)
   - `first_name`
   - `last_name`
   - `email`

2. **Employees**
   - `employee_id` (Primary Key)
   - `first_name`
   - `last_name`
   - `start_date`
   - `position_held`

3. **Products**
   - `product_id` (Primary Key)
   - `product_name`
   - `launched_date`

4. **Customer Purchases**
   - `customer_purchase_id` (Primary Key)
   - `customer_id` (Foreign Key)
   - `product_id` (Foreign Key)
   - `employee_id` (Foreign Key)
   - `purchase_at` (Date)
   - `amount_usd`

## Relationships
- One-to-Many relationship between Customers → Customer Purchases
- One-to-Many relationship between Products → Customer Purchases
- One-to-Many relationship between Employees → Customer Purchases

## Skills Demonstrated
- Database design and schema creation
- Primary and foreign keys
- One-to-many relationships
- SQL constraints
- Writing queries to insert and retrieve data
- Understanding triggers and indexes (optional)

## Sample Queries
```sql
-- Insert a customer
INSERT INTO Customers (customer_id, first_name, last_name, email)
VALUES (1, 'John', 'Smith', 'john.smith@example.com');

-- Retrieve all purchases for a customer
SELECT * FROM Customer_Purchases
WHERE customer_id = 1;
