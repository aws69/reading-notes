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


## Practice in the Terminal
Working through this beginners guide to the Linux command line (BASH) you will be up and running utilising powerful techniques, tips and tricks to make your life easier in no time. The following pages are intended to give you a solid foundation in how to use the terminal, to get the computer to do useful work for you. You won't be a Unix guru at the end but you will be well on your way and armed with the right knowledge and skills to get you there if that's what you want (which you should because that will make you even more awesome).
This Linux tutorial is divided into 13 sections :
### The Command Line!
A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.
The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands.
Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.
If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.
shortcut; When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys. So don't bother re-typing out commands you have previously entered, you can usually just hit the up arrow a few times. You can also edit these commands using the left and right arrow keys to move the cursor where you want.
### Basic Navigation!
In this section, we'll learn the basics of moving around the system. Many tasks rely on being able to get to, or reference the correct location in the system. As such, this stuff really forms the foundation of being able to work effectively in Linux.
- pwd :Print Working Directory - ie. Where are we currently.
- ls :List the contents of a directory.
- cd : Change Directories - ie. move to another directory.
*Absolute and Relative Paths*
There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

- Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

- Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.
*More on Paths*
- ~ (tilde) - This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents
- . (dot) - This is a reference to your current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy).
- .. (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.
### More About Files!
The first thing we need to appreciate with linux is that under the hood, everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. To begin with, this won't affect what we do too much but keep it in mind as it helps with understanding the behaviour of Linux as we manage files and directories.
Linux is Case Sensitive; This is very important and a common source of problems for people new to Linux. Other systems such as Windows are case insensitive when it comes to referring to files. Linux is not like this. As such it is possible to have two or more files and directories with the same name but letters of different case.
Linux actually has a very simple and elegant mechanism for specifying that a file or directory is hidden. If the file or directory's name begins with a . (full stop) then it is considered to be hidden. You don't even need a special command or action to make a file hidden. Files and directories may be hidden for a variety of reasons. Configuration files for a particular user (which are normally stored in their home directory) are hidden for instance so that they don't get in the way of the user doing their everyday tasks.
To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.

### Manual Pages! 
The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept. Some of them are a little hard to get your head around but they are fairly consistent in their structure so once you get the hang of it it's not too bad.You invoke the manual pages with the following command:
 man <command to look up>

 It is possible to do a keyword search on the Manual pages. This can be helpful if you're not quite sure of what command you may want to use but you know what you want to achieve. To be effective with this approach, you may need a few goes. It is not uncommon to find that a particular word exists in many manual pages.

man -k <search term>

### File Manipulation!
Linux organises it's file system in a hierarchical way. Over time you'll tend to build up a fair amount of data (storage capacities are always increasing). It's important that we create a directory structure that will help us organise that data in a manageable way.
So here are the comands that goona help you to do that : 
 - mkdir :Make Directory - ie. Create a directory.
 - rmdir :Remove Directory - ie. Delete a directory.
 - touch :Create a blank file.
 - cp :Copy - ie. Copy a file or directory.
 - mv :Move - ie. Move a file or directory (can also be used to rename).
 - rm :Remove - ie. Delete a file.
No undo
The Linux command line does not have an undo feature. Perform destructive actions carefully.
Command line options
Most commands have many useful command line options. Make sure you skim the man page for new commands so you are familiar with what they can do and what is available.

### Vi Text Editor!
Vi is a command line text editor. As you would be quite aware now, the command line is quite a different environment to your GUI. It's a single window with text input and output only. Vi has been designed to work within these limitations and many would argue, is actually quite powerful as a result. Vi is intended as a plain text editor (similar to Notepad on Windows, or Textedit on Mac) as opposed to a word processing suite such as Word or Pages. It does, however have a lot more power compared to Notepad or Textedit.

Vi is a command line text editor. As you would be quite aware now, the command line is quite a different environment to your GUI. It's a single window with text input and output only. Vi has been designed to work within these limitations and many would argue, is actually quite powerful as a result. Vi is intended as a plain text editor (similar to Notepad on Windows, or Textedit on Mac) as opposed to a word processing suite such as Word or Pages. It does, however have a lot more power compared to Notepad or Textedit.
- vi :Edit a file.
- cat :View a file.
- less :Convenient for viewing large files.

No mouse
vi is a text editor where everything is done on the keyboard. If you can touch type then this is great. If not then maybe you should think about learning.
Edit commands
There are many of them. Practice is the key to remember the most commonly used and useful ones.

this editor is fully new to me and look so interesting to work on it .

### Wildcards!
Wildcards are a set of building blocks that allow you to create a pattern defining a set of files or directories. As you would remember, whenever we refer to a file or directory on the command line we are actually referring to a path. Whenever we refer to a path we may also use wildcards in that path to turn it into a set of files or directories.

Here is the basic set of wildcards:

 - * - represents zero or more characters
 - ? - represents a single character
 - [] - represents a range of characters

Anywhere in any path
Wildcards may be used at any part of a path.
Wherever a path is used
Because wildcard substitution is done by the system, not the command, they may be used wherever a path is used.

### Permissions!
Linux permissions dictate 3 things you may do with a file, read, write and execute. They are referred to in Linux by a single letter each.

 - r read - you may view the contents of the file.
 - w write - you may change the contents of the file.
 - x execute - you may execute or run the file if it is a program or script.
 
 For every file we define 3 sets of people for whom we may specify permissions.
 - owner - a single person who owns the file. (typically the person who created the file but ownership may be granted to some one else by certain users)
 - group - every file belongs to a single group.
 - others - everyone else who is not in the group or the owner.

Three persmissions and three groups of people. That's about all there is to permissions really. Now let's see how we can view and change them.

Permissions for Directories
The same series of permissions may be used for directories but they have a slightly different behaviour.

r - you have the ability to read the contents of the directory (ie do an ls)
w - you have the ability to write into the directory (ie create files and directories)
x - you have the ability to enter that directory (ie cd)

chmod
Change permissions on a file or directory.
ls -ld
View the permissions for a specific directory.

Security
Correct permissions are important for the security of a system.
Usage
Setting the right permissions is important in the smooth running of certain tasks on Linux. (we will see an example of this in Section 13 on scripting)

### Filters!
A filter, in the context of the Linux command line, is a program that accepts textual data and then transforms it in a particular way. Filters are a way to take raw data, either produced by another program, or stored in a file, and manipulate it to be displayed in a way more suited to what we are after.

These filters often have various command line options that will modify their behaviour here some of them :
 - head
View the first n lines of data.
 - tail
View the last n lines of data.
 - sort
Organise the data into order.
 - nl
Print line numbers before data.
 - wc
Print a count of lines, words and characters.
 - cut
Cut the data into fields and only display the specified fields.
 - sed
Do a search and replace on the data.
 - uniq
Remove duplicate lines.
 - tac
Print the data in reverse order.

Processing
Filters allow us to process and format data in interesting ways.
man pages
Most of the programs we looked at have command line options that allow you to modify their behaviour.

### Grep and Regular Expressions!
Regular expressions are similar to the wildcards that we looked at in section 7. They allow us to create a pattern. They are a bit more powerful however. Re's are typically used to identify and manipulate specific pieces of data. eg. we may wish to identify every line which contains an email address or a url in a set of data.

The characters used in regular expressions are the same as those used in wildcards. Their behaviour is slightly different however. A common mistake is to forget this and get their functions mixed up.

egrep
View lines of data which match a particular pattern.
Regular Expressions
A powerful way to identify particular pieces of information.

### Piping and Redirection!
Every program we run on the command line automatically has three data streams connected to it.

STDIN (0) - Standard input (data fed into the program)
STDOUT (1) - Standard output (data printed by the program, defaults to the terminal)
STDERR (2) - Standard error (for error messages, also defaults to the terminal)

Piping and redirection is the means by which we may connect these streams between programs and files to direct data in interesting and useful ways.

 - '>' Save output to a file.
 - '>>' Append output to a file.
 - '<' Read input from a file.
 - '2>' Redirect error messages.
 - '|' Send the output from one program as input to another program.

### Process Management!
A program is a series of instructions that tell the computer what to do. When we run a program, those instructions are copied into memory and space is allocated for variables and other stuff required to manage its execution. This running instance of a program is called a process and it's processes which we manage.

 - top
View real-time data about processes running on the system.
 - ps
Get a listing of processes running on the system.
 - kill
End the running of a process.
 - jobs
Display a list of current jobs running in the background.
 - fg
Move a background process into the foreground.
 - ctrl + z
Pause the current foreground process and move it into the background.

### Bash Scripting!
A Bash script in computing terms is similar to a script in theatrical terms. It is a document stating what to say and do. Here, instead of the script being read and acted upon by a person, it is read and acted upon (or executed) by the computer.

A Bash script allows us to define a series of actions which the computer will then perform without us having to enter the commands ourselves. If a particular task is done often, or it is repetetive, then a script can be a useful tool.

* Anything you can run on the command line you may place into a script and they will behave exactly the same. Vice versa, anything you can put into a script, you may run on the command line and again it will perform exactly the same. *

 - #!
Shebang. Indicates which interpreter a script should be run with.
 - echo
Print a message to the screen.
 - which
Tells you the path to a particular program.
 - $
Placed before a variable name when we are referring to it's value.
 - '` `'
Backticks. Used to save the output of a program into a variable.
 - date
Prints the date.
 - if [ ] then else fi
Perform basic conditional logic.


Behaves the same
Anything you may do on the command line you may do in a script and it will behave exactly the same.
Formatting
Bash scripts are particularly picky when it comes to formatting. Make sure spaces are put where they are needed and not put when they are not needed.


## Code 201 - Foundations of Software Development

## Code 301 - Intermediate Software Development

## Code 401 - Advanced Software Development
