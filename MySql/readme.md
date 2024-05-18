# Interview Preparation on MySql

## Index
- [Interview Preparation on MySql](#interview-preparation-on-mysql)
  - [Index](#index)
  - [🚀 Topics covered from w3schools](#-topics-covered-from-w3schools)
    - [🍂 what is sql?](#-what-is-sql)
    - [🍂 SELECT statement.](#-select-statement)
    - [🍂 SELECT DISTINCT statement.](#-select-distinct-statement)
    - [🍂 SELECT \* statement.](#-select--statement)
    - [🍂 WHERE clause.](#-where-clause)
    - [🍂 AND, OR, NOT operators.](#-and-or-not-operators)
    - [🍂 ORDER BY clause.](#-order-by-clause)

## 🚀 Topics covered from w3schools

### 🍂 what is sql?
SQL is the standard language for dealing with **Relational Databases**. It is used to insert, search, update, and delete database records. It is not case sensitive.

a table that we will use in the whole tutorial:
```sql
CREATE TABLE Customers (
    CustomerID int,
    CustomerName varchar(255),
    ContactName varchar(255),
    Address varchar(255),
    City varchar(255),
    PostalCode varchar(255),
    Country varchar(255)
);

INSERT INTO Customers (CustomerID, CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES
(1, 'Alfreds Futterkiste', 'Maria Anders', 'Obere Str. 57', 'Berlin', '12209', 'Germany'),
(2, 'Ana Trujillo Emparedados y helados', 'Ana Trujillo', 'Avda. de la Constitución 2222', 'México D.F.', '05021', 'Mexico'),
(3, 'Antonio Moreno Taquería', 'Antonio Moreno', 'Mataderos 2312', 'México D.F.', '05023', 'Mexico'),
(4, 'Around the Horn', 'Thomas Hardy', '120 Hanover Sq.', 'London', 'WA1 1DP', 'UK'),
(5, 'Berglunds snabbköp', 'Christina Berglund', 'Berguvsvägen 8', 'Luleå', 'S-958 22', 'Sweden'),
(6, 'Blauer See Delikatessen', 'Hanna Moos', 'Forsterstr. 57', 'Mannheim', '68306', 'Germany'),
(7, 'Blondel père et fils', 'Frédérique Citeaux', '24, place Kléber', 'Strasbourg', '67000', 'France'),
(8, 'Bólido Comidas preparadas', 'Martín Sommer', 'C/ Araquil, 67', 'Madrid', '28023', 'Spain'),
(9, 'Bon app', 'Laurence Lebihan', '12, rue des Bouchers', 'Marseille', '13008', 'France'),
(10, 'Bottom-Dollar Marketse', 'Elizabeth Lincoln', '23 Tsawassen Blvd.', 'Tsawassen', 'T2F 8M4', 'Canada'),
```

output:
| CustomerID | CustomerName             | ContactName     | Address             | City      | PostalCode | Country |
|------------|--------------------------|-----------------|---------------------|-----------|------------|---------|
| 1          | Alfreds Futterkiste      | Maria Anders    | Obere Str. 57       | Berlin    | 12209      | Germany |
| 2          | Ana Trujillo Emparedados | Ana Trujillo    | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico  |
| 3          | Antonio Moreno Taquería  | Antonio Moreno  | Mataderos 2312      | México D.F. | 05023      | Mexico  |
| 4          | Around the Horn          | Thomas Hardy    | 120 Hanover Sq.     | London    | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp       | Christina Berglund | Berguvsvägen 8   | Luleå     | S-958 22   | Sweden  |
| 6          | Blauer See Delikatessen  | Hanna Moos      | Forsterstr. 57      | Mannheim  | 68306      | Germany |
| 7          | Blondel père et fils     | Frédérique Citeaux | 24, place Kléber | Strasbourg | 67000      | France  |
| 8          | Bólido Comidas preparadas | Martín Sommer  | C/ Araquil, 67      | Madrid    | 28023      | Spain   |
| 9          | Bon app                  | Laurence Lebihan | 12, rue des Bouchers | Marseille | 13008      | France  |
| 10         | Bottom-Dollar Marketse   | Elizabeth Lincoln | 23 Tsawassen Blvd. | Tsawassen | T2F 8M4    | Canada  |

<br>

### 🍂 SELECT statement.
The SELECT statement is used to select data from a database. The data returned is stored in a result table, called the result-set.
```sql
SELECT column1, column2, ...
FROM table_name;
```
<br><br>

### 🍂 SELECT DISTINCT statement.
The SELECT DISTINCT statement is used to return only **distinct (different)** values.
```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```
<br><br>

### 🍂 SELECT * statement.
The SELECT * statement is used to select all columns from a table.
```sql
SELECT * FROM table_name;
```
<br><br>

### 🍂 WHERE clause.
The WHERE clause is used to filter records. This clause is used to extract only those records that fulfill a specified condition.
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

real example:
```sql
SELECT * FROM Customers
WHERE Country='Mexico';
```
it will return all the customers from Mexico.
<br><br><br>

### 🍂 AND, OR, NOT operators.
The AND, OR, and NOT operators are used to filter records based on more than one condition.
- The AND operator displays a record if all the conditions separated by AND are TRUE.
- The OR operator displays a record if any of the conditions separated by OR is TRUE.
- The NOT operator displays a record if the condition(s) is NOT TRUE.

and operator example:
```sql
SELECT * FROM Customers
WHERE Country='Germany' AND City='Berlin';
```
it will return all the customers from Germany and Berlin.

or operator example:
```sql
SELECT * FROM Customers
WHERE Country='Germany' OR Country='France';
```
it will return all the customers from Germany and France.

not operator example:
```sql
SELECT * FROM Customers
WHERE NOT Country='Germany';
```
it will return all the customers except Germany.
<br><br><br>

### 🍂 ORDER BY clause.