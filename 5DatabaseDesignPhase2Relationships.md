## Database relationships. Identifying vs non-Identifying, cardinality
### Foregin keys
A relationship is established between two database tables when one table has a foreign key that references the primary key of another table.

### Identifying relationship vs non-identifying relationship

#### Img17.1

### Relationship cardinality
- The degree of relationship (also known as cardinality) is the number of occurrences in one entity which are associated (or linked) to the number of occurrences in another
- There are three different degrees of relationship, known as:
    - one-to-one(1:1)
    - one-to-many(1:M)
    - many-to-many(M:N)

### One to One relationship
- this type of relationship allows only one record on each side of the relationship
- not very common
- Customer - Address(Customer table can have address_id as foreign key)
- to enforce one-to-one relationship, we need to enforce unique constraint on the address_id column

### One to Many relationship
- A one-to-many relationship allows a single record in one table to be related to multiple records in another table
- One-to-many = Many-to-one (depends from which side you look at it)
- the many has the foreign key
- one-to-many -> Product - Items

### Many-to-many relationship
- Products-Categories
- a many-to-many relationship allows multiple records in one table to be related to multiple records in another table 
- for these relationships, we need to create an extra table
- Products - Products_Categories - Categories
- Products_Categories will have one column(Foreign key to the primary key of Products table) and another column(Foreign key to the primary key of Categories table) and together it will form a primary key in Product_Categories table
- Customer-FavoriteProducts

### Many-to-many: why the intermediary table?
