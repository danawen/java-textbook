# Java Database Connectivity (JDBC)

The Java Database Connectivity (JDBC) interface is a toolkit for managing connections between your Java code and a database. We will be using JDBC to connect our Java programs to a lightweight SQLite database.

## Set up the SQLite JDBC driver

Follow the steps to install and set up the SQLite JDBC driver on your local environment.
- Download the `sqlite-jdbc-3.23.1.jar` file from the [SQLite JDBC library download page](https://bitbucket.org/xerial/sqlite-jdbc/downloads/)
- Move the `.jar` file to a new folder `C:\Program Files\sqlite`
- In Eclipse, create a new Java project called "SQLiteSample"
- Add the SQLite JDBC `.jar` file to your Java project build path by following these steps:
  - Right-click on the "SQLiteSample" project and select "Build path" -> "Configure build path..."
  - In the Java Build Path pop-up window, select the "Libraries" tab. Click the button "Add External JARs..."
  - Navigate to `C:\Program Files\sqlite` and select the SQLite JDBC `.jar` file. Click the "Open" button.
  - Back in the Java Build Path window, select "Apply and Close".
- In your "SQLiteSample" project, create a file called `Sample.java`.
- Copy the `Sample.java` code from the [SQLite JDBC Usage page](https://github.com/xerial/sqlite-jdbc) (scroll down below the list of files to see the README document and code) into your own `Sample.java` file.
- Run your SQLiteSample project to verify that the sample code is successfully creating and updating the SQLite database.
- Read through the code in `Sample.java` and identify where SQL queries are sent to the database. What commands are being executed and how are they modifying the database? Experiment with adding your own SQL queries to the sample code.

## SQLite JDBC sample code

- [SqliteExample.java](https://github.com/danawen/dell-java/blob/assignments/SQLiteSample/src/SqliteExample.java) - Console program that demos basic interactions with a SQLite database (select, insert, update, delete).
- [Sample.java](https://github.com/danawen/dell-java/blob/assignments/SQLiteSample/src/Sample.java) - Modified sample code from SQLite JDBC driver page. Added an extra method to query `person` table by `name` column.

## Resources

- [SQLite Java Tutorial](http://www.sqlitetutorial.net/sqlite-java/) - Step-by-step instructions and examples of how to execute common SQLite database commands using Java code. A good second step after familiarizing yourself with the `Sample.java` code above.
- [SQLite homepage](https://www.sqlite.org) - Includes documentation and resources
- [SQLite Tutorial](http://www.sqlitetutorial.net/) - Introduces the basics of SQLite (database commands only, no Java)
- [JDBC Basics (Java Tutorials handbook)](https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html) - Comprehensive set of examples for a deep dive into JDBC. Relies on familiarity with Maven and other build tools. Recommended if you'd like to learn more about integrating Java with different database solutions.

