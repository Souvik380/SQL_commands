# Structured Query Language(SQL)

## DATABASE
A _database_ is a collection of data that is organized in a manner that facilitates ease of access, as well as efficient management and updating.

A _database_ is made up of tables that store relevant information.

For example, you would use a database, if you were to create a website like YouTube, which contains a lot of information like videos, usernames, passwords, comments

## SQL
Once you understand what a database is, understanding SQL is easy. **SQL** stands for **S**tructured **Q**uery **L**anguage.

**SQL** is used to access and manipulate a **database**.
**MySQL** is a **program** that understands **SQL**.

SQL can:
- _insert_, _update_, or _delete_ records in a database.
- create new _databases_, _tables_, stored procedures and views.
- retrieve data from a database, etc.

## BASICS

#### DDL (Data Definition Language) :
- **Data Definition Language** is used to define the database structure or schema. **DDL** is also used to specify additional properties of the data.

- The storage structure and access methods used by the database system by a set of statements in a special type of **DDL** called a data storage and definition language.

#### Some Commands:
- **_CREATE_**: to create objects in database
- **_ALTER_** : alters the structure of database
- **_DROP_** : delete objects from database
- **_RENAME_** : rename an objects

#### Examples:
    - CREATE TABLE Persons (
            PersonID int,
            LastName varchar(255),
            FirstName varchar(255),
            Address varchar(255),
            City varchar(255)
        );

    - ALTER TABLE table_name ADD column_name datatype;
    - DROP TABLE Shippers;


#### DML (Data Manipulation Language) :
**DML** statements are used for managing data with in schema objects. 

#### Some commands:
    SELECT: retrieve data from the database
    INSERT: insert data into a table
    UPDATE: update existing data within a table
    DELETE: deletes all records from a table, space for the records remain

#### Examples:
    - select City from customers;

    - INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);

    - UPDATE table_name SET column1 = value1, column2 = value2, WHERE condition;
    
    - DELETE FROM table_name WHERE condition;


#### SQL Joins
    SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are as follows: 

        -INNER JOIN
        -LEFT JOIN
        -RIGHT JOIN
        -FULL JOIN
    
#### INNER JOIN:
    The INNER JOIN keyword selects all rows from both the tables as long as the condition is satisfied. This keyword will create the result-set by combining all rows from both the tables where the condition satisfies i.e value of the common field will be the same.

*Examples:*
    - SELECT table1.column1,table1.column2,table2.column1,....
    FROM table1 
    INNER JOIN table2
    ON table1.matching_column = table2.matching_column;

#### LEFT JOIN:
    This join returns all the rows of the table on the left side of the join and matches rows for the table on the right side of the join. For the rows for which there is no matching row on the right side, the result-set will contain null. LEFT JOIN is also known as LEFT OUTER JOIN.

*Examples:*
    SELECT table1.column1,table1.column2,table2.column1,....
    FROM table1 
    LEFT JOIN table2
    ON table1.matching_column = table2.matching_column; 

#### RIGHT JOIN:
    RIGHT JOIN is similar to LEFT JOIN. This join returns all the rows of the table on the right side of the join and matching rows for the table on the left side of the join. For the rows for which there is no matching row on the left side, the result-set will contain null. RIGHT JOIN is also known as RIGHT OUTER JOIN.

*Examples*:
    SELECT table1.column1,table1.column2,table2.column1,....
    FROM table1 
    RIGHT JOIN table2
    ON table1.matching_column = table2.matching_column;

#### FULL JOIN:
    FULL JOIN creates the result-set by combining results of both LEFT JOIN and RIGHT JOIN. The result-set will contain all the rows from both tables. For the rows for which there is no matching, the result-set will contain NULL values.

*Examples:*
    SELECT Student.NAME,StudentCourse.COURSE_ID 
    FROM Student
    FULL JOIN StudentCourse 
    ON StudentCourse.ROLL_NO = Student.ROLL_NO;

#### Aggregate functions in SQL
    As the Basic SQL Tutorial points out, SQL is excellent at aggregating data the way you might in a pivot table in Excel. You will use aggregate functions all the time, so it's important to get comfortable with them. The functions themselves are the same ones you will find in Excel or any other analytics program. We'll cover them individually in the next few lessons. Here's a quick preview:

    COUNT counts how many rows are in a particular column.
    SUM adds together all the values in a particular column.
    MIN and MAX return the lowest and highest values in a particular column, respectively.
    AVG calculates the average of a group of selected values

   *Examples:*
    -SELECT AVG(column_name) FROM table_name;
    -SELECT ROUND(AVG(scores)) FROM students; 


--------------------------------------------------------

#### REFERENCES:
1.  https://mode.com/sql-tutorial/sql-aggregate-functions/

2. https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=true

3. https://www.edureka.co/blog/sql-commands

