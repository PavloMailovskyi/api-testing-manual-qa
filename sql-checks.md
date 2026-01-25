# SQL Checks – DummyJSON API

## Overview
DummyJSON API does not provide access to a real database.
The SQL queries below are theoretical backend validation checks
that a QA engineer could perform if database access were available.

These checks demonstrate:
- Understanding of database validation
- API ↔ Database consistency
- Data integrity verification

---

## Authentication Checks

### Verify user exists
SELECT id, username
FROM users
WHERE username = 'emilys';

Expected:
- User record exists
- id is not NULL

---

### Verify invalid user is not created
SELECT *
FROM users
WHERE username = 'wronguser';

Expected:
- No records returned

---

## Product Checks

### Verify product exists by ID
SELECT id, title, price
FROM products
WHERE id = 1;

Expected:
- Product exists
- Price > 0

---

### Verify all products have valid price
SELECT id, price
FROM products
WHERE price <= 0;

Expected:
- No records returned

---

### Verify product creation (logical check)
SELECT id, title, price
FROM products
WHERE title = 'QA Test Product';

Expected:
- Product exists
- Data matches API request payload

Note:
DummyJSON does not persist data, check is conceptual.

---

## Update Validation

### Verify full update (PUT)
SELECT id, title, price
FROM products
WHERE id = 1;

Expected:
- All fields updated correctly

---

### Verify partial update (PATCH)
SELECT id, title, price
FROM products
WHERE id = 1;

Expected:
- Only updated fields changed
- Other fields unchanged

---

## Delete Validation

### Verify product deletion
SELECT *
FROM products
WHERE id = 1;

Expected:
- No records returned

Note:
DummyJSON simulates delete, data may still appear.

---

## Negative Data Scenarios

### Detect invalid price values
SELECT id, price
FROM products
WHERE price < 0;

Expected:
- No records returned
- If records exist → data validation bug

---

## Notes for Reviewers
- Queries are theoretical and demonstrate backend validation knowledge
- API used: DummyJSON (mock, stateless backend)
- Focus: test logic, SQL validation, API-to-DB consistency
