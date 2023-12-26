# Introduction Into SQL
## 📌 1.0 Overview
This project is a simple SQL database called `CS_101` that stores information about students in an introductory computer science class. The database contains a single table called `students`

## Table  Diagram
![SQL 101 (1)](https://github.com/Ebenmars/SQL-Journey/assets/76241509/933fe8fd-10b0-4910-b7bd-da29883a6894)

- `NN` stands for `NOT NULL` which means that a field can not be null their has to be information in the field.
- The `🔑` next to the `id` mean `PRIMARY KEY`

## 🤿 Deep Dive
This is where the magic happens
```sql
CREATE TABLE students(
    id INT PRIMARY KEY AUTO_INCREMENT, 
    name VARCHAR(50) NOT NULL, 
    age INT NOT NULL
);
