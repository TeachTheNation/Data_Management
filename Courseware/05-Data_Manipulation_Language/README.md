# Data Manipulation Language (DML)

Data Manipulation Language (DML) is a subset of SQL that is used to manipulate the content of the database.

This is different to DDL, which is used to manipulate the schema rather than the data.

DML is arguably the most widely-used subtype of MySQL, and is often integrated into applications to read/write data to/from databases.

The most well-used operations we’d expect to use in DML are:
* Inserting data into, and deleting data from, tables
* Reading data from tables based on various criteria
* Updating the existing records in a table

## CRUD operations

You may see applications and operations being referred to as CRUD applications/operations. 

**CRUD** stands for:
* **C**reate
* **R**ead
* **U**pdate
* **D**elete

* In MySQL syntax, there are a few ways that we can use CRUD functionality:

| Operation | SQL         |
|:---------:|:------------|
|  create   | INSERT INTO |
|   read    | SELECT      |
|  update   | UPDATE      |
|  delete   | DELETE      |

## Inserting Data

The syntax for inserting records into a table breaks down into the following:
* Specify the table and columns that you want to insert data into
* Specify the values that we want to enter, in the same order that we used to identify the columns

If we are inserting into specific fields in a table, we must specify them:
```sql
INSERT INTO table_name (column_1, column_4, column_5)
VALUES (value_1, value_2, value_3);
```

However, if we're inserting into all fields, there is no need to specify them:
```sql
INSERT INTO table_name
VALUES (value_1, value_2, value_3, value_4, value_5);
```

## Deleting Records

Deleting records from a table uses the **DELETE** keyword.

If you don't specify any criteria, MySQL will delete all records, so be very careful!
```sql
DELETE FROM customer_archive;
```

To delete a specific record, you should specify criteria; this is done with the WHERE keyword.
```sql
DELETE FROM orders WHERE status='Cancelled';
```

# Updating Records

The syntax for updating records in a table breaks down into the following:
* Outline the table that the record exists in
* Specify the value for the changed field
* Outline any conditions

```sql
UPDATE table_name
SET column1=value1, column2=value2
WHERE field=value;
```

# Viewing records

We can view the records within a table with the SELECT keyword:
```sql
SELECT * FROM table_name;
```

**SELECT** is technically its own language - **Data Query Language** - and is covered in ***the Data Query Language module***.
