# Aggregate Functions

An aggregate or aggregation function is a function where the values of multiple rows are grouped together to form a single summary value.

There are a number of aggregate functions supported in MySQL, all of which aim to get a single result from several records:
* **COUNT** – counts the number of Records
* **SUM** – gets the sum total of a field
* **MIN/MAX/AVG** – gets the minimum/maximum/average value from a field

## COUNT

The **COUNT()** function returns the number of records that match specified criteria:
```sql
SELECT COUNT(field_name1) FROM table_name;
```

For example, if we wanted to count the number of orders placed:
```sql
SELECT COUNT(order_id) FROM orders;
```

## SUM

The SUM() function returns a calculated total from a numeric field:
```sql
SELECT SUM(field_name1) FROM table_name;
```

For example, if we wanted to count the number of items in the order line:
```sql
SELECT SUM(quantity) FROM order_line;
```

## MIN, MAX, and AVG

The MIN() function returns the smallest value in a field:
```sql
SELECT MIN(price) FROM product;
```

The MAX() function returns the largest value in a field:
```sql
SELECT MAX(price) FROM product;
```

The AVG() function returns the average value in a field:
```sql
SELECT AVG(price) FROM product;
```
