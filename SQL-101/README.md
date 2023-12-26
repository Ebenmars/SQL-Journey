# Introduction Into SQL

## 📌 1.0 Overview

This project is a simple SQL database called `CS_101` that stores information about students in an introductory computer science class. The database contains a single table called `students`.

## Table Diagram

![SQL 101 (1)](https://github.com/Ebenmars/SQL-Journey/assets/76241509/933fe8fd-10b0-4910-b7bd-da29883a6894)

- `NN` stands for `NOT NULL`, which means that a field cannot be null; there has to be information in the field.
- The `🔑` next to the `id` means `PRIMARY KEY`.

## 🤿 Deep Dive

This is where the magic happens.

### Create A Table

```sql
CREATE TABLE students(
    id INT PRIMARY KEY AUTO_INCREMENT, 
    name VARCHAR(100) NOT NULL, 
    age INT NOT NULL
);
```
- `id` is an integer that is set to be a primary key that auto increments.
- `name` is a varchar that has a character limit of 100 and cannot be null.
  - `VARCHAR` is a SQL function that holds characters.
- `age` is an int that cannot be null.
  - `NOT NULL` is a SQL function that says that a field cannot be null. Something has to be inputted into the field.

## Look At How The Table Is Fomratted!

```sql
DESC students
```

| Field | Type        | Null | Key  | Extra          |
|-------|-------------|------|------|----------------|
| id    | INT         | NO   | PRI  | AUTO_INCREMENT |
| name  | VARCHAR(100)| NO   |      |                |
| age   | INT         | NO   |      |                |


## Insert Into Table

```sql
INSERT INTO CS_101 VALUES(‘Mike’,19);
```
- We dont need to add the `id` in this case becuase we set it to auto

## Inserting Multiple Values

```sql
INSERT INTO CS_101 VALUES(‘Jane,20),
(‘James’,18),
(‘Roger’,19);
```




