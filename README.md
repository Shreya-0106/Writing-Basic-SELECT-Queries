-- Create a sample table
CREATE TABLE Customers (
    CustomerID INTEGER PRIMARY KEY,
    FirstName TEXT,
    LastName TEXT,
    Country TEXT,
    Age INTEGER
);

-- Insert some sample data
INSERT INTO Customers (CustomerID, FirstName, LastName, Country, Age) VALUES (1, 'Liam', 'Smith', 'USA', 23);
INSERT INTO Customers (CustomerID, FirstName, LastName, Country, Age) VALUES (2, 'Sophia', 'Miller', 'USA', 21);
INSERT INTO Customers (CustomerID, FirstName, LastName, Country, Age) VALUES (3, 'Akira', 'Tanaka', 'Japan', 24);
INSERT INTO Customers (CustomerID, FirstName, LastName, Country, Age) VALUES (4, 'Carlos', 'Hernandez', 'USA', 21);
INSERT INTO Customers (CustomerID, FirstName, LastName, Country, Age) VALUES (5, 'Isabella', 'Rossi', 'Italy', 22);

-- Select specific columns from all records
SELECT FirstName, LastName FROM Customers;

-- Select records with a WHERE condition
SELECT * FROM Customers WHERE Age = 21;

-- Select records with multiple conditions using AND and OR
SELECT * FROM Customers WHERE Country = 'USA' AND Age > 21;

-- Use LIKE to find records where LastName starts with 'M'
SELECT * FROM Customers WHERE LastName LIKE 'M%';

-- Select records with BETWEEN condition on Age
SELECT * FROM Customers WHERE Age BETWEEN 22 AND 24;

-- Sort results by Age in descending order
SELECT * FROM Customers ORDER BY Age DESC;



Output:

+-----------+-----------+
| FirstName | LastName  |
+-----------+-----------+
| Liam      | Smith     |
| Sophia    | Miller    |
| Akira     | Tanaka    |
| Carlos    | Hernandez |
| Isabella  | Rossi     |
+-----------+-----------+
+------------+-----------+-----------+---------+------+
| CustomerID | FirstName | LastName  | Country | Age  |
+------------+-----------+-----------+---------+------+
|          2 | Sophia    | Miller    | USA     |   21 |
|          4 | Carlos    | Hernandez | USA     |   21 |
+------------+-----------+-----------+---------+------+
+------------+-----------+----------+---------+------+
| CustomerID | FirstName | LastName | Country | Age  |
+------------+-----------+----------+---------+------+
|          1 | Liam      | Smith    | USA     |   23 |
+------------+-----------+----------+---------+------+
+------------+-----------+----------+---------+------+
| CustomerID | FirstName | LastName | Country | Age  |
+------------+-----------+----------+---------+------+
|          2 | Sophia    | Miller   | USA     |   21 |
+------------+-----------+----------+---------+------+
+------------+-----------+----------+---------+------+
| CustomerID | FirstName | LastName | Country | Age  |
+------------+-----------+----------+---------+------+
|          1 | Liam      | Smith    | USA     |   23 |
|          3 | Akira     | Tanaka   | Japan   |   24 |
|          5 | Isabella  | Rossi    | Italy   |   22 |
+------------+-----------+----------+---------+------+
+------------+-----------+-----------+---------+------+
| CustomerID | FirstName | LastName  | Country | Age  |
+------------+-----------+-----------+---------+------+
|          3 | Akira     | Tanaka    | Japan   |   24 |
|          1 | Liam      | Smith     | USA     |   23 |
|          5 | Isabella  | Rossi     | Italy   |   22 |
|          2 | Sophia    | Miller    | USA     |   21 |
|          4 | Carlos    | Hernandez | USA     |   21 |
+------------+-----------+-----------+---------+------+
+------------+-----------+----------+---------+------+
| CustomerID | FirstName | LastName | Country | Age  |
+------------+-----------+----------+---------+------+
|          1 | Liam      | Smith    | USA     |   23 |
|          2 | Sophia    | Miller   | USA     |   21 |
|          3 | Akira     | Tanaka   | Japan   |   24 |
+------------+-----------+----------+---------+------+

-- Limit results to 3 records
SELECT * FROM Customers LIMIT 3;
