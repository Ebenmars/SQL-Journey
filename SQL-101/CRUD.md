# CRUD Operations in SQL for a Car Wash Fundraiser

## 📌 1.0 Overview

This project is a simple SQL database called `car_wash` that stores information about people who will be volunteering for a local high school team to raise funds through a car wash fundraiser. The database contains a single table called `volunteers`.

## 🤿 Deep Dive

This is where the magic happens.

## Create

We will create a dataset called `volunteers`.

```sql
CREATE TABLE volunteers(
    ID INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(100) NOT NULL,
    last_name VARCHAR(100) NOT NULL,
    age INT, 
    additional_people INT DEFAULT 0 
);
```
- `additional_people` are the additional people that the volunteers will be bringing with them.

## Look At How The Table Is Formatted!

```sql
DESC volunteers
```

| Field             | Type         | Null | Key  | Extra          |
|-------------------|--------------|------|------|----------------|
| ID                | INT          | NO   | PRI  | AUTO_INCREMENT |
| first_name        | VARCHAR(100) | NO   |      |                |
| last_name         | VARCHAR(100) | NO   |      |                |
| age               | INT          | YES  |      |                |
| additional_people | INT          | YES  |      | DEFAULT 0      |


## Insert Into The Table

```sql
INSERT INTO volunteers (first_name, last_name, age, additional_people) 
VALUES ('John', 'Doe', 16, 1),
       ('Jane', 'Smith', 17, 0), 
       ('Alice', 'Johnson', 15, 2), 
       ('Bob', 'Williams', 17, 0), 
       ('Charlie', 'Brown', 18, 3), 
       ('Emily', 'Davis', 16, 2);

```
| ID | first_name | last_name | age | additional_people |
|----|------------|-----------|-----|-------------------|
| 1  | John       | Doe       | 16  | 1                 |
| 2  | Jane       | Smith     | 17  | 0                 |
| 3  | Alice      | Johnson   | 15  | 2                 |
| 4  | Bob        | Williams  | 17  | 0                 |
| 5  | Charlie    | Brown     | 18  | 3                 |
| 6  | Emily      | Davis     | 16  | 2                 |


## READ

How do we retrieve and search data?

```sql
SELECT * FROM volunteers;
```
| ID | first_name | last_name | age | additional_people |
|----|------------|-----------|-----|-------------------|
| 1  | John       | Doe       | 16  | 1                 |
| 2  | Jane       | Smith     | 17  | 0                 |
| 3  | Alice      | Johnson   | 15  | 2                 |
| 4  | Bob        | Williams  | 17  | 0                 |
| 5  | Charlie    | Brown     | 18  | 3                 |
| 6  | Emily      | Davis     | 16  | 2                 |


What if I only want to see nothing else but their first & last names?

```sql
SELECT first_name, last_name FROM volunteers WHERE additional_people > 0;
```
| first_name | last_name |
|------------|-----------|
| John       | Doe       |
| Alice      | Johnson   |
| Charlie    | Brown     |
| Emily      | Davis     |


## Where Clause

I want to know which people will be bringing additional people, how can i do that? 

```sql
SELECT first_name FROM volunteers WHERE additional_people >  0;
```
  
| id | name  | age |
|----|-------|-----|
| 1  | Mike  | 19  |
| 2  | Jane  | 20  |
| 3  | James | 18  |
| 4  | Roger | 19  |


## Aliases

Let’s say you have an overblown field name and you don’t want to constantly write it down. You can use an alias.

```sql
SELECT additional_people AS people FROM volunteers
```
  


## Update

How do we update existing information?

For example – YAA🥳 Bob is now bringing two people with him to volunteer  


```sql
UPDATE  volunteers SET  additional_people= 2 WHERE first_name= ‘Bob’;
```
  




## ✅ Learning Outcomes

<details>
<summary>
Click to view my learning outcomes!
  
</summary>
<br>


The following SQL skills and concepts will be covered in this section:

- Learning how to create table 
- Learning how to insert into table 
- Learned how to view table 
- Learned how to automae id 
  
</details>
