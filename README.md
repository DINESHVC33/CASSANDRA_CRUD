# CASSANDRA_CRUD

Cassandra Query Language (CQL) CRUD Operations

Cassandra Query Language (CQL) is a language that allows users to interact with the Cassandra database. It is a SQL-like language that is used to create, update, and delete data from the Cassandra database.

This README file provides a brief guide on how to perform CRUD (Create, Read, Update, Delete) operations using CQL in Cassandra.

Creating a Table
To create a table in Cassandra, you can use the CREATE TABLE statement. The general syntax for creating a table is as follows:



                  CREATE TABLE table_name (
                    column1 datatype,
                    column2 datatype,
                    column3 datatype,
                    ...
                    PRIMARY KEY (one_or_more_columns)
                       );
