
# SQL Basics for Manual QA

This document contains basic SQL queries used in manual testing to retrieve, filter, sort, and verify database records.

## 1. SELECT — Retrieve Data

Retrieve all users:

```sql
SELECT * FROM users;
```

Retrieve specific columns:

```sql
SELECT name, email
FROM users;
```

## 2. WHERE — Filter Data

Find users from Shenzhen:

```sql
SELECT *
FROM users
WHERE city = 'Shenzhen';
```

## 3. ORDER BY — Sort Data

Sort users by name:

```sql
SELECT *
FROM users
ORDER BY name ASC;
```

## 4. COUNT — Count Records

Count all users:

```sql
SELECT COUNT(*)
FROM users;
```

## 5. GROUP BY — Group Records

Count users in each city:

```sql
SELECT city, COUNT(*)
FROM users
GROUP BY city;
```

## 6. JOIN — Combine Tables

Retrieve orders together with customer names:

```sql
SELECT users.name, orders.order_id
FROM users
JOIN orders
ON users.id = orders.user_id;
```

## QA Application

SQL can help manual QA engineers:
- Verify that data is correctly saved.
- Check whether records are updated or deleted.
- Find specific records using filters.
- Compare application data with database records.
- Validate relationships between database tables.
