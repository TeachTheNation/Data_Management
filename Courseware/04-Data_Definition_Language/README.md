# Data Definition Language

**Data Definition Language (DDL)** is one of the subsets of SQL query types.

It centers around defining the schema for the database, and writing queries to create, alter and delete parts of the schema.

## Creating a database

The SQL statement to create a database is as follows:
```sql
CREATE DATABASE some_database;
```

You can also use the optional **IF NOT EXISTS** command to ensure that your database will only be created if it does not already exist:
```sql
CREATE DATABASE IF NOT EXISTS some_database;
```

From here, if you wish to work with this database, you would run the below:

```sql
USE some_database;
```

## Creating tables

DDL-based SQL statements can be used to create tables.

The syntax for this is similar to the below:
```sql
CREATE TABLE table_name (
  column_name1 data_type(size) constraint_name,
  column_name2 data_type(size) constraint_name,
);
```

* **CREATE TABLE** is used first alongside the name of the table, followed by an open parenthesis to declare table fields.
* We then list the fields in order of field name, data type (with the size in parentheses if relevant) and a constraint we wish to use.
* Make sure you put a comma between different columns and a semi-colon at the end of your command.

## Schema Deletion

Deleting a table can be done with the **DROP TABLE** statement.

You can list multiple tables if more than one needs to be dropped, and table data and definitions are all removed, so use with caution.

If not all the listed tables exist, MySQL will still drop all tables that do exist.

```sql
DROP TABLE IF EXISTS table_that_should_not_be_dropped;
```
