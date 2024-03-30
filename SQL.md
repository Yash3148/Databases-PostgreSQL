C -> CREATE
R -> READ
U -> UPDATE
D -> DELETE

SQL Playgroud --> https://sqliteonline.com/

# Create a table 

CREATE TABLE products (
  id INT NOT NULL,
  name STRING,
  price MONEY,
  PRIMARY KEY (id)
)

# To show table 

SELECT *  FROM 'products';

# To insert values in table 

INSERT INTO products
VALUES (1, "Pen", 1.20)

# To add specific values in table 

INSERT INTO products(id, name)
VALUES (2, "Book")

# To read specific values/ element  from the table 

SELECT name, price FROM products;  

# To read a specific row 

SELECT * FROM products WHERE id=1;

# Update data of a particular column for a particular row 

UPDATE products
SET price = 0.80
WHERE id=2;   (This will update the id name as 2 for price of it.)

# Adding a column in existing table 

ALTER TABLE products
ADD stock INT

# But it is in null state we have to add values in it.

UPDATE products
SET stock = 32
WHERE id=1

UPDATE products
SET stock = 12
WHERE id=2

# Delete 

DELETE FROM products
WHERE id = 2

DELETE FROM products
WHERE name = "Pen"