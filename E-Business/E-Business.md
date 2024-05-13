
### 1. Create Database

```SQL
CREATE DATABASE E_Business;
```

### 2. Create Customer Table

```SQL
CREATE TABLE Customers (
    Customer_ID INT PRIMARY KEY,
    Customer_Name VARCHAR(255) NOT NULL,
    Address VARCHAR(255),
    City VARCHAR(100),
    Postal_Code VARCHAR(20),
    Country VARCHAR(100)
);
```

### 3. Insert  20 row values into the Customer table

```SQL
INSERT INTO Customers VALUES
(1, 'John Doe', '123 Main St', 'New York', '10001', 'USA'),
(2, 'Alice Smith', '456 Elm St', 'Los Angeles', '90002', 'USA'),
(3, 'Bob Johnson', '789 Oak St', 'Chicago', '60603', 'USA'),
(4, 'Emily Williams', '101 Pine St', 'Houston', '77004', 'USA'),
(5, 'Michael Brown', '202 Maple St', 'Phoenix', '85005', 'USA'),
(6, 'Sarah Lee', '303 Cedar St', 'Philadelphia', '19106', 'USA'),
(7, 'David Jones', '404 Birch St', 'San Antonio', '78207', 'USA'),
(8, 'Jennifer Davis', '505 Walnut St', 'San Diego', '92108', 'USA'),
(9, 'Robert Martinez', '606 Cherry St', 'Dallas', '75209', 'USA'),
(10, 'Jessica Rodriguez', '707 Pineapple St', 'San Jose', '95110', 'USA'),
(11, 'William Hernandez', '808 Peach St', 'Austin', '78711', 'USA'),
(12, 'Amanda Nguyen', '909 Lemon St', 'Jacksonville', '32212', 'USA'),
(13, 'Daniel Gonzalez', '1010 Orange St', 'San Francisco', '94113', 'USA'),
(14, 'Laura Wilson', '1111 Grape St', 'Indianapolis', '46214', 'USA'),
(15, 'Steven Anderson', '1212 Banana St', 'Columbus', '43215', 'USA'),
(16, 'Karen Taylor', '1313 Strawberry St', 'Fort Worth', '76116', 'USA'),
(17, 'Christopher Thomas', '1414 Watermelon St', 'Charlotte', '28217', 'USA'),
(18, 'Elizabeth White', '1515 Blueberry St', 'Seattle', '98118', 'USA'),
(19, 'Matthew Martin', '1616 Raspberry St', 'Denver', '80219', 'USA'),
(20, 'Ashley Garcia', '1717 Blackberry St', 'Washington', '20020', 'USA');

```

### 4. Create Products Table

```SQL
CREATE TABLE Products (
    Product_ID INT PRIMARY KEY,
    Product_Name VARCHAR(255) NOT NULL,
    Supplier_ID INT,
    CategoryID INT,
    Unit VARCHAR(50),
    Price DECIMAL(10, 2)
);

```

### 5. Insert  20 row values into the Products table

```SQL

INSERT INTO Products VALUES
(1, 'Shirt M', 101, 201, 'Piece', 19.99),
(2, 'Pant', 102, 202, 'Piece', 29.99),
(3, 'Dress', 103, 203, 'Piece', 39.99),
(4, 'Jacket', 104, 204, 'Piece', 49.99),
(5, 'Jeans', 105, 205, 'Piece', 34.99),
(6, 'Skirt', 106, 206, 'Piece', 24.99),
(7, 'T-shirt', 107, 207, 'Piece', 14.99),
(8, 'Sweater', 108, 208, 'Piece', 39.99),
(9, 'Blouse', 109, 209, 'Piece', 29.99),
(10, 'Coat', 110, 210, 'Piece', 59.99),
(11, 'Shorts', 111, 211, 'Piece', 19.99),
(12, 'Suit', 112, 212, 'Piece', 79.99),
(13, 'Scarf', 113, 213, 'Piece', 9.99),
(14, 'Hat', 114, 214, 'Piece', 14.99),
(15, 'Socks', 115, 215, 'Pair', 4.99),
(16, 'Shoes', 116, 216, 'Pair', 49.99),
(17, 'Sandals', 117, 217, 'Pair', 29.99),
(18, 'Boots', 118, 218, 'Pair', 59.99),
(19, 'Slippers', 119, 219, 'Pair', 19.99),
(20, 'Flip Flops', 120, 220, 'Pair', 9.99);
```

### 6. Create orders Table

```SQL
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    Customer_ID INT,
    Employee_ID INT,
    Order_Date DATE,
    Shipper_ID INT
);

```

### 7. Insert  20 row values into the orders table
```SQL
-- Inserting 20 rows into the orders table
INSERT INTO orders VALUES
(1, 101, 201, '2024-03-01', 301),
(2, 102, 202, '2024-03-02', 302),
(3, 103, 203, '2024-03-03', 303),
(4, 104, 204, '2024-03-04', 304),
(5, 105, 205, '2024-03-05', 305),
(6, 106, 206, '2024-03-06', 306),
(7, 107, 207, '2024-03-07', 307),
(8, 108, 208, '2024-03-08', 308),
(9, 109, 209, '2024-03-09', 309),
(10, 110, 210, '2024-03-10', 310),
(11, 111, 211, '2024-03-11', 311),
(12, 112, 212, '2024-03-12', 312),
(13, 113, 213, '2024-03-13', 313),
(14, 114, 214, '2024-03-14', 314),
(15, 115, 215, '2024-03-15', 315),
(16, 116, 216, '2024-03-16', 316),
(17, 117, 217, '2024-03-17', 317),
(18, 118, 218, '2024-03-18', 318),
(19, 119, 219, '2024-03-19', 319),
(20, 120, 220, '2024-03-20', 320);

```

### 8. Create shippers Table
```SQL
CREATE TABLE Shippers (
    Shipper_ID INT PRIMARY KEY,
    Shipper_Name VARCHAR(255) NOT NULL,
    Phone VARCHAR(20)
);

```


### 9. Insert  20 row values into the shippers table
```SQL
-- Inserting 20 rows into the Shippers table
INSERT INTO Shippers (Shipper_ID, Shipper_Name, Phone) VALUES
(301, 'Shipper 1', '123-456-7890'),
(302, 'Shipper 2', '234-567-8901'),
(303, 'Shipper 3', '345-678-9012'),
(304, 'Shipper 4', '456-789-0123'),
(305, 'Shipper 5', '567-890-1234'),
(306, 'Shipper 6', '678-901-2345'),
(307, 'Shipper 7', '789-012-3456'),
(308, 'Shipper 8', '890-123-4567'),
(309, 'Shipper 9', '901-234-5678'),
(310, 'Shipper 10', '012-345-6789'),
(311, 'Shipper 11', '111-222-3333'),
(312, 'Shipper 12', '222-333-4444'),
(313, 'Shipper 13', '333-444-5555'),
(314, 'Shipper 14', '444-555-6666'),
(315, 'Shipper 15', '555-666-7777'),
(316, 'Shipper 16', '666-777-8888'),
(317, 'Shipper 17', '777-888-9999'),
(318, 'Shipper 18', '888-999-0000'),
(319, 'Shipper 19', '999-000-1111'),
(320, 'Shipper 20', '000-111-2222');

```

