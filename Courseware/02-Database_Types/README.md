# Database Types

## Overview

This module serves as a general introduction to different kinds of databases.

## Database Types

Typically, databases fall into two distinct types: relational and non-relational.

Relational databases focus on modelling a business structure, as well as implementing strong business rules and constraints on data and the type of information captured. 
Examples include MySQL, Oracle SQL, PostgreSQL, and Microsoft SQL Server.

Non-relational databases focus on the read/write capacity and capability of data, emphasising the speed in which we access data. 
Examples include MongoDB, Amazon's DynamoDB, and Cassandra.

Of the two, a relational database will be easier to model, while a non-relational database is easier to read from and write information to.

## Database objects

Databases need to transform data into information by adding context.

Raw data means nothing; a list of numbers, keywords, or characters may not add any value without interpretation.

```
Jeff 23
Cyrus 24
```

Databases allow for this, by categorising data into tables and adding fields to these data tables for further organising. 
For instance, this might be inside the customers table:

* ***Database*** - a full data set, consisting of a collection of tables
* ***Table*** - an organised set of data objects
* ***Field*** - a way to categorise stored data
* ***Record*** - an instance of fields in a table

## Relationships

Relational databases run on relationships - a way of linking tables together.

Consider a retail-based business; several different tables could be modelled, such as:
* a customers table to store user and account information
* a orders table to keep a log of purchases
* a product table to store data on all of the items available

Naturally, some of these tables will need to link in some way.

Linking tables will allow one record in a table to access another; for example, linking the customer and order table will allow us to check what customers made an order without having to duplicate data across multiple tables.



