# Introduction

## Overview

This module serves as a general introduction to relational databases and the Relational Database Management Systems (RDBMS) used to access them.

## Databases

A ***database*** is an organised collection of data. 
All web applications need some kind of database for data storage and retrieval.

Consider a website like Amazon, which serves millions of customers; it's impossible to store all of that information in the website or code - we need a database to do this!

If we think of the actual Website we see as the front-end, and the bit that does the heavy lifting in the background as the back-end, a database hooks into the back-end code for data. 
Requested data is sent from the back-end code to the database, and the database sends the appropriate data back.

Databases are generally made up of two distinct areas:
* the data - the actual information it stores
* the schema - the way that information is stored (the layout the data takes)

## Data

Data stored in a database is organised into tables (also known as entities), which are modelled on real-life objects that we would store information on, such as customers, products or orders.

These tables then contain one or more records - each record is an instance, or set, of complete data.

For example, a record in the customer table would be 1 set of completed data, with all information we need to be filled for a customer.

## Schema

A database schema defines the structure and relationships between data.

For example, the customer table would most likely link, or relate, in some way to the order table, as customers typically place orders in real life.

Therefore, we can model this relationship within our database through the schema!

## Queries

Varying types of statements are used to access the data stored in databases. 
The type of statement used will differ, depending on the task you are trying to achieve. For instance, to select specific records within a database, you'd use a query.

From there, the statement is run against the database and its data, and the database will respond to the query with the information you require.

For example, we could write a query asking to see all of the customers over the age of 35 - the database would take this query, look at the relevant tables and data, and present said information to the user.






