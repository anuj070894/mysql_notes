## What is a database?
- organized collection of data
- collection of schemas, tables, queries, reports, views and other objects
- etc. etc

## How do database work and why are they important?
- B-Tree - reduced complexity of O(logn) for searches
- A B-tree is a self balancing tree data structure that keeps data sorted and allows searches, sequential access, insertions and deletions in logarithmic time. It is commonly used in databases and filesystems

### img 4.1

## B-trees indexing power
### img 4.2

B-trees are used to index rows of table

## Why are databases important?
- databases manage data so efficiently
- web applications

## Different types of databases
- relational databases - RDBMS 
- NoSQL databases 
  - "Not only SQL" 
  - mongoDB
  - NoSQL databases are increasingly used in big data and real-time web applications

## What is a relational database?
- tuple or record(row)
- attribute(column)
- relation(table)

### Rules
- each table has a unique name 
- each table contains multiple rows
- each row in a table is unique
- every table has a key to uniquely identify the rows
- each column in a table has a unique attribute name 

### Primary keys
- only one primary key in a table(usually a single attribute, but can be composed of multiple attributes(composite primary key))
- SSN or e-mail for people

### Foreign Keys
- A table(daily_reports) has a column called as (employee_id) that is a foreign key to table employees
