# Show How many databases are in your system

```SQL 
SHOW DATABASES;
```
# Output:

![[Pasted image 20240513104334.png]]


# Create Database 

```SQL
CREATE DATABASE book_library;
```

# Output

![[Pasted image 20240513105819.png]]


# Delete / Drop Database

```SQL 
DROP DATABASE database_Name;
```


# Create Table 

```SQL
CREATE TABLE book_table (
    book_id INT PRIMARY KEY,
    title VARCHAR(50),
    genre VARCHAR(50)
);

```

# Insert values into the table

```SQL
INSERT INTO book_table VALUES
	(101, "H.P", "Fantasy"), 
    (102, "T.L.W", "Novel"), 
    (103, "Gospel", "Religious"), 
    (104, "S.Jobs", "Biography");
```

# Output

![[Pasted image 20240513111012.png]]

# Author table

```SQL 
CREATE TABLE author_table (
    author_id INT PRIMARY KEY,
    author VARCHAR(50),
    book_id INT,
    FOREIGN KEY (book_id) REFERENCES book_table(book_id)
);

```

#  Insert values into the author table
```SQL
INSERT INTO author_table VALUES 
	(301, "J.K.R", 101),
    (302, "L.M.A", 102),
    (303, "Jhon", 103),
    (304, "W.I", 104);
```


# Library table

```SQL
CREATE TABLE library_table(
    
	library_id INT PRIMARY KEY,
    library_name VARCHAR(100),
    library_manager VARCHAR(100),
    book_id INT,
    author_id INT,
    
    FOREIGN KEY (book_id) REFERENCES book_table(book_id),
    FOREIGN KEY (author_id) REFERENCES author_table(author_id)
);
```

# Insert values into the Library table

```SQl
INSERT INTO library_table VALUES 
	(401, "city.L", "David", 101, 301),
    (402, "T.H.L", "Ashley", 102, 302),
    (403, "M.C.L", "Rose", 103, 303),
    (404, "T.C.L", "Rachel", 104, 304);
```


# Borrower Table
```SQl
CREATE TABLE borrower_table (
	
    borrower_id INT PRIMARY KEY,
    book_id INT,
    library_id INT,
    
    FOREIGN KEY (book_id) REFERENCES book_table(book_id),
    FOREIGN KEY (library_id) REFERENCES library_table(library_id)

);
```

# Insert values into the Borrower table

```SQl

```
