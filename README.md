# Summary of The Ultimate MySQL Bootcamp

## What is a database?
A database is an organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). Together, the data and the DBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just database.

## Database vs Database Management System (DBMS)
A database is a logically modeled cluster of information [data] that is typically stored on a computer or other type of hardware that is easily accessible in various ways. A database management system is a computer program or other piece of software that allows one to access, interact with, and manipulate a database.
## MySQL vs SQL
![Alt text](./images/relation-db.png?raw=true "Title")

SQL is used for accessing, updating and maintaining data in a database and MySQL is an RDBMS (Relational Database Management System) that allows users to keep the data that exists in a database organized. SQL does not change (much), as it is a language. MySQL updates frequently as it is a piece of software

SQL is a language for querying databases and MySQL is an open source database product
<table>
    <tr>
        <th>SQL</th>
        <th>MySQL</th>
    </tr>
    <tr>
        <td>SQL is a query programming language that manages RDBMS.</td>
        <td>MySQL is a relational database management system that uses SQL.</td>
    </tr>
    <tr>
        <td>SQL is primarily used to query and operate database systems.</td>
        <td>MySQL allows you to handle, store, modify and delete data and store data in an organized way.</td>
    </tr>
    <tr>
        <td>SQL does not support any connector.</td>
        <td>MySQL comes with an in-built tool known as MySQL Workbench that facilitates creating, designing, and building databases.</td>
    </tr>
    <tr>
        <td>SQL follows a simple standard format without many or regular updates.</td>
        <td>MySQL has numerous variants and gets frequent updates.</td>
    </tr>
    <tr>
        <td>SQL supports only a single storage engine.</td>
        <td>MySQL offers support for multiple storage engines along with plug-in storage, making it more flexible.</td>
    </tr>
    <tr>
        <td>SQL does not allow other processors or even its own binaries to manipulate data during execution.</td>
        <td>MySQL is less secure than SQL, as it allows third-party processors to manipulate data files during execution.</td>
    </tr>
</table>

## Creating Databases and Tables

### Databases
Example Command:
- Create: 
  ```
  CREATE DATABASE database_name
  ```
- Delete: 
  ```
  DROP database_name
  ```

- Use: 
  ```
  USE database_name
  ```


### Tables
Each column in a database table is required to have a name and a data type.

An SQL developer must decide what type of data that will be stored inside each column when creating a table. The data type is a guideline for SQL to understand what type of data is expected inside of each column, and it also identifies how SQL will interact with the stored data.

Example Command:
- Create:
  ```
  CREATE TABLE cats 
  (
      name varchar(100),
      age int(11),
  );
  ```
- Dropping Tables
  ```
  DROP TABLE <tablename>; 
  ```


### CODE: Introduction
- Insert
  ```
  INSERT INTO cats(name, age) VALUES ('Jetson', 7);
  ```
- Multiple Insert
  ```
    INSERT INTO cats(name, age) VALUES ('Jetson', 7), 
    ('Jhony', 11), 
    ('Jhon',22);

  ```
- SELECT
    ```
    SELECT * FROM cats; 
    ```
    ```
    SELECT name FROM cats; 
    ```
    ```
    SELECT age FROM cats; 
    ```
    ```
    SELECT name, age, breed FROM cats; 
    ```
     ```
    SELECT name, age, breed FROM cats WHERE name = 'Jetson'; 
    ```
    ```
    SELECT cat_id AS id, name FROM cats;
    ```
- UPDATE
  ```
  UPDATE cats SET breed='Shorthair' WHERE breed='Tabby';
  ```
- DELETE
  ```
  DELETE FROM cats WHERE age=4;
  ```
  