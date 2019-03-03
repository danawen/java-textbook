# SQL

SQL, or Structured Query Language, gives you the power to access and manipulate databases. A database is a structured set of information stored on a computer or server. 

Sets of data are stores in **tables**. Tables consist of rows and columns. 

## Example

Here's an example of a table called Students:

### Students

<table>
  <tr>
    <th>StudentID</th>
    <th>StudentName</th>
    <th>StudentEmail</th>
    <th>StudentPhone</th>
    <th>City</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Orlando</td>
    <td>Orlando@aca.com</td>
    <td>123-456-7891</td>
    <td>Houston</td>
  </tr>
  <tr>
    <td>2</td>
    <td>James</td>
    <td>James@aca.com</td>
    <td>123-456-7891</td>
    <td>San Antonio</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Kelly</td>
    <td>Kelly@aol.com</td>
    <td>123-456-7891</td>
    <td>Austin</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Kari</td>
    <td>Kari@aol.com</td>
    <td>123-456-7891</td>
    <td>Austin</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Jose</td>
    <td>Jose@aca.com</td>
    <td>123-456-7891</td>
    <td>Dallas</td>
  </tr>
</table>

The following command selects all the data from the table called Students:

```sql
SELECT * FROM Students;
```

*** Important SQL Commands

* SELECT - retrieves a set of data from a table
* UPDATE - change an entry in a table
* DELETE - remove an entry from a table
* INSERT INTO - add data into a table
* CREATE DATABASE - create database
* CREATE TABLE - create a table
* DROP TABLE - delete table

To select the columns StudentName and StudentEmail from the Students table:
```sql
SELECT StudentName, StudentEmail FROM Students;
```


To select all the students who live in Austin from the Students table:
```sql
SELECT * FROM Students
WHERE City='Austin';
```

## Assignment

Complete the [SQL Zoo Tutorial](https://sqlzoo.net/) to practice working with SQL. Please complete everything through the "SUM and COUNT" section, including the quiz for that section.

All the material about JOIN operations is optional.

## More Practice

- [W3Schools SQL tutorial](https://www.w3schools.com/sql/default.asp)
- [MySQL Installer for Windows (free)](https://www.mysql.com/why-mysql/windows/)
- [MySQL Workbench for Windows (free)](https://dev.mysql.com/downloads/workbench/)
