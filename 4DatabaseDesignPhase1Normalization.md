### Define conceptual and logical design for an online store

### E-commerce Database design
### Conceptual entities and attributes
- Customers
    - id
    - email
    - name
    - address
    - favorite products
- Products
    - id
    - name
    - about
    - price
    - brand
    - brand description
    - category
- Orders
    - product
    - customer
    - warranty
    - purchase date

### What is database normalization?
- normalization is a database design technique which organizes tables in a manner that reduces redundancy and dependency of data
- redundant data = useless data = same data stored in more than one place

### problems without normalization
- updation anamoly
- insertion anamoly
- deletion anamoly

### First normal form
#### Rules
- each table cell should contain a single ("atomic") value
- each record needs to be unique

#### How to do 1FN?
- split columns to atomic values(address into street, city, state)
- if multiple values can be assigned to a record; move them to a new table

### Second Normal Form - Definition
- A table is in 2NF if it is in 1NF and every non-key attribute of the table is dependent on the whole (every attribute of) composite primary key
- For orders table, our composite primary key consists of (customer, product). We see that purchase_date is actually depending on the composite primary key. But warranty doesn't. It only depends on the product
- Therefore, we can remove warranty out of the orders table and put it in products table
- tables without the composite primary are in 2NF by default

### Third normal form
- A table is in 3NF if and only if both of the following conditions hold:
    - the relation R(table) is in second normal form(2NF)
    - every non-prime attribute of R is non-transitively dependent on every key of R
- third normal form means that every non-prime attribute of table must be dependent on primary key, or we can say that, there should not be the case that a non-prime attribute is determined by another non-prime attribute. So this transitive functional dependency should be removed from the table and also the table must be in 2NF
- the brand_description(attribute) in products(table) depends on the brand and not on the product. Therefore, we can create another table with brand and brand_description as attributes in that table
