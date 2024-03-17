# Data Query Language

**Data Query Language (DQL)** allows us to read data, it contains a single command - **SELECT**, which allows us to retrieve information from a database.

Arguably, **SELECT** is the most powerful command within SQL, due to its versatility.

## Reading with SELECT

The **SELECT** statement is used to read data from a database.

We can use this in a very simplistic way by selecting all records from a table, or add a number of different clauses, grouping and sorting options.

The syntax for a SELECT statement is similar to the below;
```sql
SELECT field_name1, field_name2 FROM table_name;
```

If you want to see all of the records from a table, we can run the below;
```sql
SELECT * FROM table_name;
```

## SELECT DISTINCT

We can add a number of other keywords to our SELECT statement to make the data returned more specific to what we need.

One way of doing this is by using the DISTINCT keyword, which will only return unique values from a particular column.

For instance, perhaps we want to see all of the cities which customers live in.

We could run something similar to the below and manually find all unique entries;
```sql
SELECT city FROM customers
```

For a case like this, we can use the DISTINCT keyword which, when attached to a field, will find all of the unique values in that column.
```sql
SELECT DISTINCT city FROM customers
```

## The WHERE clause

If we wish to add further specifics and criteria to what we want to read from a table, we can use the **WHERE** clause in our **SELECT** statement.
```sql
SELECT fields FROM table_name WHERE condition;
```

For example, if we wanted to see all of the products that are over £50;
```sql
SELECT * FROM products WHERE price > 50;
```

## WHERE clause operators

The WHERE clause can also use several different operators for comparisons:
* = (equal to), != (not equal to)

```sql
SELECT * FROM products WHERE product_name = 'Stevens Watch';

SELECT * FROM customers WHERE city != 'Manchester';
```

* < and > (less and greater than), <= and >= (less than or equal, greater than or equal)

```sql
SELECT * FROM products WHERE price < 10;

SELECT * FROM customers WHERE age >= 18;
```

* BETWEEN – within an inclusive range
```sql
SELECT * FROM orders WHERE datePlaced BETWEEN '2019-01-01' AND '2019-12-31';
```

* LIKE – searching for a pattern
```sql
SELECT * FROM customers WHERE name LIKE '%son';
```

## Aliasing

We can use the aliasing keyword AS to present our data differently. 
It is commonly used for renaming columns on which some kind of arithmetic has been done:
```sql
SELECT field_name1 AS name, field_name2 FROM table_name;
```

For example, if we wanted to calculate a price within a query, we could use the below as an example;
```sql
SELECT title, quantity, price, quantity*price AS stock_value FROM products;
```

## Ordering Data

The **ORDER BY** keyword allows us to sort our records upon retrieval.

ORDER BY will, by default, present selected data in ascending order unless specified within the query;
```sql
SELECT field_name1, field_name2 FROM table_name ORDER BY field_name2 DESC;
```

If you wish to specify for MySQL to order ascending, you can do so with the below;
```sql
SELECT field_name1, field_name2 FROM table_name ORDER BY field_name2 ASC;
```

To do so for descending order, use the **DESC** keyword instead.
