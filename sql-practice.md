# SQL Practice For Manual QA

Manual testers often use SQL to confirm that frontend actions are saved correctly in the backend database.

## Example Tables

Assume an e-commerce database has these tables:

- users
- products
- orders
- order_items
- payments

## Practice Queries

```sql
-- Find a user by email
SELECT id, first_name, last_name, email, status
FROM users
WHERE email = 'test@example.com';

-- Check all orders for one user
SELECT id, user_id, order_status, total_amount, created_at
FROM orders
WHERE user_id = 101
ORDER BY created_at DESC;

-- Verify items in an order
SELECT oi.order_id, p.name, oi.quantity, oi.unit_price
FROM order_items oi
JOIN products p ON oi.product_id = p.id
WHERE oi.order_id = 5001;

-- Check if order total matches item totals
SELECT order_id, SUM(quantity * unit_price) AS calculated_total
FROM order_items
WHERE order_id = 5001
GROUP BY order_id;

-- Find failed payments
SELECT id, order_id, payment_status, failure_reason, created_at
FROM payments
WHERE payment_status = 'FAILED'
ORDER BY created_at DESC;

-- Count orders by status
SELECT order_status, COUNT(*) AS total_orders
FROM orders
GROUP BY order_status;
```

## QA Interview Talking Point

"I use SQL to validate that UI actions are correctly reflected in the database. For example, after placing an order, I would check the order table, order items table, payment status, and calculated totals."

