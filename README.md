# Reading Notes

**this wepsite is to demonstrate my knowledge from this course and keep updating what i learn .**

## Introduction to SQL 
**What is SQL Language?**
Structured Query Language, or SQL, is an accepted industry-standard language. It is a query language used to access a database from a language like C/C++, Java, or a web application. SQL is the lingua franca for most database applications. You need a database to store and organize all the information you need to store and organize, such as contacts, addresses, invoices, etc. As of this writing, SQL is the most popular database programming language available.
Using an SQL editor, SQL programmers can access a database to perform queries and get data out of the database. A variety of databases supports SQL. Commonly used databases include Oracle, SQL Server, MySQL, Sybase, and PostgreSQL.
SQL is the industry-standard language for managing databases. It's an easy language to learn and use. In this beginner's tutorial, you'll learn to query, analyze, and create tables, views, indexes, and schemas.
**Why should I learn SQL?**
SQL is the language used to manage and query a database. If you're doing SQL programming for databases like MySQL, Oracle, or SQL Server, it's the language you'll use the most. SQL is the language of the database.

If you're using a database, it's the language you'll use most. SQL is an industry-standard language. Anyone who writes SQL queries knows the language and can share what they know with you. This reduces confusion when you're querying a database.

If you're a Java programmer, learning SQL is like learning a new language. It's easy to pick up if you know to approach the language differently than a native Java developer.
**What we learned in SQL**
- Basic SQL commands
INSERT: used to add new data to a database.
SELECT: used to retrieve data from a database.
DELETE: used to delete data from a database.
UPDATE: used to modify existing data in a database.

- Data types
VARCHAR stores character strings (such as names or addresses).
INTEGER: used to store numerical data.
DATE: used to store date values.

- Operators
AND: used to combine two or more conditions.
OR: used to specify that either of the two conditions can be true.
BETWEEN: used to specify a range of values.

- Creating tables
CREATE TABLE: used to create a new table in a database.

- Modifying tables
ALTER TABLE: used to modify an existing table in a database.

- Querying data
WHERE: used to filter the results of a SELECT statement based on specified conditions.

- Joining tables
INNER JOIN combines rows from two or more tables based on a common column.
LEFT/RIGHT/FULL JOIN: return all the rows from the left table and any rows from the right table that match them.

![Screenshot of SQL Totorial](https://github.com/aws69/reading-notes/blob/main/Assests/Screenshot%202023-08-07%20034115.png?raw=true)

## Code 102 - Intro to Software Development
### Clas 03
int: int is a primitive data type in Java. It is a built-in type and represents a 32-bit signed integer value. Primitives are more memory-efficient and have better performance compared to objects.
Integer: Integer is a class that is part of the Java standard library and belongs to the java.lang package. It's a wrapper class that provides methods to manipulate int values as objects. Since it's a class, it has some overhead in terms of memory usage and performance compared to the primitive int.

int: The default value for an int is 0. If you declare an int variable without explicitly initializing it, it will automatically have the value 0.
Integer: The default value for an Integer object (when not explicitly initialized) is null. Unlike primitive types, objects in Java are initialized to null by default.

Autoboxing: Autoboxing is the process of automatically converting a primitive type to its corresponding wrapper class object. For example, when you assign an int value to an Integer reference, Java will automatically convert the int to an Integer object. This feature was introduced to simplify code and make it more convenient to work with both primitive types and their corresponding objects.
Unboxing: Unboxing is the opposite process of autoboxing. It's the automatic conversion of a wrapper class object back to its corresponding primitive type. For example, if you have an Integer object and you assign it to an int variable, Java will automatically extract the int value from the Integer object.

=========================================================================================================================

The first kind of exception is the checked exception. These are exceptional conditions that a well-written application should anticipate and recover from. For example, suppose an application prompts a user for an input file name, then opens the file by passing the name to the constructor for java.io.FileReader. Normally, the user provides the name of an existing, readable file, so the construction of the FileReader object succeeds, and the execution of the application proceeds normally. But sometimes the user supplies the name of a nonexistent file, and the constructor throws java.io.FileNotFoundException. A well-written program will catch this exception and notify the user of the mistake, possibly prompting for a corrected file name.
Checked exceptions are subject to the Catch or Specify Requirement. All exceptions are checked exceptions, except for those indicated by Error, RuntimeException, and their subclasses.

The second kind of exception is the error. These are exceptional conditions that are external to the application, and that the application usually cannot anticipate or recover from. For example, suppose that an application successfully opens a file for input, but is unable to read the file because of a hardware or system malfunction. The unsuccessful read will throw java.io.IOError. An application might choose to catch this exception, in order to notify the user of the problem — but it also might make sense for the program to print a stack trace and exit.
Errors are not subject to the Catch or Specify Requirement. Errors are those exceptions indicated by Error and its subclasses.

The third kind of exception is the runtime exception. These are exceptional conditions that are internal to the application, and that the application usually cannot anticipate or recover from. These usually indicate programming bugs, such as logic errors or improper use of an API. For example, consider the application described previously that passes a file name to the constructor for FileReader. If a logic error causes a null to be passed to the constructor, the constructor will throw NullPointerException. The application can catch this exception, but it probably makes more sense to eliminate the bug that caused the exception to occur.
Runtime exceptions are not subject to the Catch or Specify Requirement. Runtime exceptions are those indicated by RuntimeException and its subclasses.
Errors and runtime exceptions are collectively known as unchecked exceptions.


The try block contains the code that you suspect might throw an exception.

The catch blocks follow the try block and are used to catch and handle specific types of exceptions. You can have multiple catch blocks to handle different types of exceptions that the code in the try block might throw.

The finally block is optional. It contains code that will be executed regardless of whether an exception was thrown or caught. It's often used for cleanup operations that need to happen regardless of the exception's occurrence.


==========================================================================================================================

A situation where it would be useful to have a program that scans text is when you're building a text processing tool, such as a text editor, a search engine, a language translator, or a data extraction tool. These programs often need to interact with text data entered by users or obtained from external sources, and scanning the text allows you to analyze and manipulate it effectively.


the Scanner class is commonly used to read input from various sources, such as the console or files. When you use a Scanner to read input, the input is broken down into tokens. The default delimiter for the Scanner class is whitespace, meaning it breaks the input into chunks separated by spaces, tabs, or newlines. You can customize the delimiter if needed.


## Code 201 - Foundations of Software Development

## Code 301 - Intermediate Software Development

## Code 401 - Advanced Software Development
