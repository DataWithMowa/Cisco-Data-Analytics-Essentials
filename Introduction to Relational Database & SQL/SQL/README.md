## 1. The SQL Query Language

Once we have designed our database with all the tables and columns that we need, we need a way to add data to those tables, read that data, update it if it changes, and delete anything we don’t need anymore. To do that, most of the relational databases use a language called SQL, or “Structured Query Language,” and each time we use SQL to do something in the database, it’s called a “query.”

SQL queries are made up of statements that, as in other common programming languages, have a defined syntax. Let’s see an example of a simple SQL query to read data from the Movie table in the Movies database we presented before:
 
Let’s say we want to list the title and year of all the movies in the table. The query would look like this:

SELECT title, year FROM Movie

This query uses the keyword SELECT because we are selecting specific data to read and display. This first command defines the goal of the whole query. The SELECT command, along with INSERT, UPDATE, and DELETE, is part of the SQL language used to work with, or manipulate, the data itself. This is called DML (Data Manipulation Language).

Another part of the SQL language is called DDL, or Data Definition Language, and it allows us to create and maintain the database schema. With DDL we can do things like create tables, define their structure, and specify the data type that is expected for each column.

A note on SQL queries: SQL is so universally supported by relational database systems (RDBSs) that relational databases are often referred to as “SQL databases.” The SQL language itself is an open-source standard, but each RDBS supports its own selection of SQL keywords, so it is important to refer to the documentation of the specific RDBS we are using.

## 2. What is SQL?

Simply put, this is explaining the basics of SQL (the language used to talk to databases):

**What SQL is:** A programming language used to communicate with relational databases (databases that organize data into tables).

**What it can do:** SQL statements let you retrieve, update, delete, and create data, plus set permissions for who can access what.

**The most important command — SELECT:** This is the one you'll use most. It pulls data out of a table. Example:

```sql
SELECT * FROM patients;
```

This means "show me everything (the `*` means 'all') from the patients table."

**Two categories of SQL commands:**
- **DDL (Data Definition Language)** – commands like CREATE DATABASE/TABLE and DROP DATABASE/TABLE, used mainly by database admins to build or remove entire databases/tables
- **DML (Data Manipulation Language)** – commands like SELECT, used to work with the actual data inside tables (this is the focus for now)

**A few style notes/conventions:**
- It's common to write SQL keywords in CAPS (like `SELECT`, `FROM`) for readability, but SQL doesn't actually care — lowercase works fine too
- It's common practice to end statements with a semicolon `;`
- Spaces don't matter to SQL, but it's best to avoid spaces in table/column names to prevent headaches

**Bottom line:** SQL is how you "ask" a database questions or give it instructions, and `SELECT * FROM tablename;` is your basic "show me everything in this table" command.
