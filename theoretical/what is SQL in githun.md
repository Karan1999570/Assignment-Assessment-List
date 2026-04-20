# What is SQL?

 1. SQL (Structured Query Language) is a standardized programming language used to manage, manipulate, and retrieve data stored in relational databases. It was developed in the 1970s by IBM researchers and became an ANSI/ISO standard in 1986. Almost every major database system — MySQL, PostgreSQL, Oracle, SQL Server, SQLite — uses SQL as its core language.

 2. Core Concepts
  
 **Relational Databases**

   .  Data is stored in tables (rows and columns), similar to spreadsheets. Tables relate to each other through keys. This structure is called a Relational Database Management System (RDBMS).

**Data Types**

 *Common SQL data types include*

 1. INT / BIGINT – whole numbers
 2. VARCHAR(n) / TEXT – strings
 3. DECIMAL / FLOAT – decimal numbers
 4. DATE / DATETIME / TIMESTAMP – date and time values
 5. BOOLEAN – true/false
 6. BLOB / BYTEA – binary data (images, files)   

**SQL Command Categories** 

1. DDL – Data Definition Language
  
  *1.1- how to crate databade*

 CREATE: Used to create a new database or database object (e.g., database, table, view, index).

  ---  create database databasename;
       exm.
       crate database class_room1;   

  *1.2.how crate tabel*
   
        create table tablename(
   column1 datatype,
   column2 datatype,
   column3 datatype 
     )

     exm.

     crate table students(
        id int,
         name varchar(50),
         age int,
         department varchar(50)
     )

  *1.3 data types and size of column in tables rules*

    1.int
     . SQL me INT (ya INTEGER) ek data type hai jo whole numbers (poore number) store karne ke liye use hota hai — jaise 1, 50, -200, 1000, etc.
     
     
     exmp.
     CREATE TABLE students (
     id INT,
     age INT
     );
     

    2.varchar
     . SQL me VARCHAR ek data type hai jo text (string) store karne ke liye use hota hai — jaise naam, address, email, etc.
     
     
     exmp.
     CREATE TABLE students (
     name VARCHAR(50),
     city VARCHAR(100)
     );
     

    3.date
    . SQL me DATE ek data type hai jo date (tarikh) store karne ke liye use hota hai — jaise year, month aur day
    
     
     exmp.
     CREATE TABLE employees (
     id INT,
     name VARCHAR(50),
     join_date DATE
     );
     
    
    4.float
    . SQL me FLOAT ek data type hai jo decimal numbers (point wale numbers) store karne ke liye use hota hai.
    
    
     exmp.
     CREATE TABLE products (
     id INT,
     price FLOAT,
     discount FLOAT
     );
     

    5.boolean
    . SQL me BOOLEAN ek data type hai jo sirf true/false (yes/no) type values store karne ke liye use hota hai.
    
    
     exmp.
     CREATE TABLE users (
     id INT,
     name VARCHAR(50),
     is_active BOOLEAN
     );
     
    
    6.text
    . SQL me TEXT ek data type hai jo bada text (long text / paragraphs) store karne ke liye use hota hai.

    
     exmp.
     CREATE TABLE posts (
     id INT,
     title VARCHAR(100),
     content TEXT
     );
     
    
    7.datetime
    . SQL me DATETIME ek data type hai jo date + time dono ko ek saath store karne ke liye use hota hai.

    
    exmp.
     CREATE TABLE orders (
     id INT,
     product_name VARCHAR(100),
     order_time DATETIME
     );
     

    8.char
    . SQL me CHAR ek data type hai jo fixed-length text (fixed size ka text) store karne ke liye use hota hai.
    
    
    exmp.
     CREATE TABLE users (
     id INT,
     gender CHAR(1),
     country_code CHAR(3)
     );
    
    9.decimal
    . SQL me DECIMAL ek data type hai jo exact decimal numbers store karne ke liye use hota hai — khas taur par jahan accuracy bahut important hoti hai (jaise paise / money).
    
    
    exmp.
     CREATE TABLE products (
     id INT,
     price DECIMAL(10,2),
     tax DECIMAL(5,2)
     );
    
    10.enum
    . SQL me ENUM ek data type hai jo fixed list (predefined values) me se sirf ek value select karne ke liye use hota hai.
    
    
    emap.
     CREATE TABLE users (
     id INT,
     name VARCHAR(50),
     gender ENUM('Male', 'Female', 'Other')
     );
    

    11.bigint
    . SQL me BIGINT ek numeric data type hai jo bahut bade whole numbers (integers) store karne ke liye use hota hai.
    
    
    exmp.
     CREATE TABLE transactions (
     id BIGINT,
     user_id BIGINT,
     amount DECIMAL(10,2)
    );
    
    12.auto_increment
    . SQL me AUTO_INCREMENT ek property (feature) hai jo kisi column (mostly INT ya BIGINT) ko automatically number generate karne ke liye use hota hai.

    
    exmp.
     CREATE TABLE students (
     id INT AUTO_INCREMENT,
     name VARCHAR(50),
     PRIMARY KEY (id)
     );
    
    