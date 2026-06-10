#  TOPIC 1: Introduction to Databases

This lesson is introduces me  to **databases and how they work**. 

---

### 🗄️ What is a Database?
A database is a structured repository of data built for a specific purpose — like storing employee info for HR or inventory for a sales system.

---

### 📋 How Data is Organized
- **Records** = a single entry (e.g., one employee's details)
- **Fields** = individual characteristics within a record (name, address, birthdate, etc.)
- **Tables** = a collection of records arranged in rows and columns (similar to a spreadsheet)

---

### 🗂️ Schema & Metadata
- **Schema** = Describes the design and structure of the database, the blueprint of the database (table names, fields, data types, relationships)
- **Metadata** Data about data. It tells you information about what is contained within the database, including:

The schema
Indexes
Views
Size of tables (in kilobytes or megabytes)
Number of rows

---

### ⚙️ Database Management Systems (DBMS)
Software that manages databases. It allows users and applications to interact with data, handles multiple transactions at once, and ensures data **integrity and security**.

---

### 📊 Types of Databases
| Type | Examples |
|------|----------|
| Flat Files | Excel |
| Relational | SQL Server, MySQL |
| NoSQL | Flexible/scalable, newer type |

---



### 🎯 Bottom Line
This module focuses on **relational databases and SQL** — the tools most commonly used by data analysts.

# TOPIC 2: Flat File Databases

For centuries, humanity has been storing data and records—often related to transactions and trade. The first cuneiform scriptures that archaeologists have discovered, which date from thousands of years ago, were very often related to accounting. They were used to record information like the number of cows sold to a given farmer or the salaries paid to members of an ancient army.
See picture below:

![Babylonian Cuneiform tablet. Account of gold. 7th–6th century B.C. Wikipedia Commons](https://github.com/DataWithMowa/Cisco-Data-Analytics-Essentials/blob/main/Introduction%20to%20Relational%20Database%20%26%20SQL/Data%20Basic%20Management/Babylonian%20Cuneiform%20tablet..png)

With time, the alphabet and then methods of recording have changed, but we can still find ourselves using paper and pen to store data in a very similar way to those ancient documents.

![Patterson's General Store Ledger, Chapel Hill Historical Society, Public domain, via Wikimedia Commons](https://github.com/DataWithMowa/Cisco-Data-Analytics-Essentials/blob/main/Introduction%20to%20Relational%20Database%20%26%20SQL/Data%20Basic%20Management/330px-Millinery_Book_Ledger_-_DPLA_-_4e890e62dfe17d454d20da31c89554c8_(page_105).jpg)

In the beginning of the computer era, we tried to make this process easier. To do it, we “copied” what we have been doing for centuries and created flat file databases. A flat file database is like the ledger in the picture above but stored as text characters inside a table format in a computer. It stores information in rows, each with the same structure as the previous one. We call each of those rows, which can be readily accessed and edited, a record or instance. Columns run vertically from top to bottom, and they contain different types of information, also known as fields or attributes, for each record or row. Rows run horizontally from left to right and are also known as records s. A spreadsheet file, shown below, is an example of a flat file database.

Flat file databases can also be in plain text format. A common example of this type of flat file database is a CSV, or comma-separated values, file. Here, there are no cells, as in a spreadsheet—instead, information in each row is separated by plain text characters, called delimiters, such as commas.

Flat files are good for simple data, and you will use them in many scenarios. However, if you need to store large amounts of complex data, the flat file system quickly becomes inefficient. Flat files are also prone to some types of errors. One of these common problems is called data inconsistency.

Let’s suppose that, like in the old ledger image above, we have a flat file to keep track of what the gold miners buy in our general store, and we have records like this:

**Customer, date, article, cost**

**Joe “Goldentooth” Smith, 12-23-1897, Cat gut banjo strings, 0.15$**
Some days later Joe comes back to buy a bottle of whiskey for the New Year’s party:

**Joe “Goldentooth” Smith, 12-31-1897, Bottle of whiskey, 0.75$**
We need to write the full name again, and that is redundant. A flat file can have a lot of duplications like this that make it inefficient.

Now let’s say Joe has a fight at the New Year’s party and lost his golden tooth, so now he is called Joe “Missingtooth” Smith. He comes back to the store to buy some soup and the record for this purchase is:

**Joe “Missingtooth” Smith, 01-02-1898, Can of soup, 0.05$**
Now, in our flat file database, we have the same customer with 2 different names, which will create a data inconsistency. To solve this problem, we would need to search and find all the previous “Goldentooth” entries for this customer and correct them to “Missingtooth.”

Another inconsistency could be created if an employee accidentally writes “Bottle of whisky” instead of “Bottle of whiskey” to record the sale of this same product. Then if we search in the flat file for all of the “Bottle of whiskey” entries, we will miss the one that is spelled differently.

Another problem could arise If we want to add the address of the customer, so the record would look like this:

**Customer, address, date, article, cost**

**Joe “Goldentooth” Smith, Stinky Hut #23, 02-12-1898, Golden tooth, 20.99$**
It would be really difficult to modify the existing file to add that column between the customer and the date and fill all the missing values in the pre-existing records.

Compared to relational databases, the advantages and challenges of flat file databases are as follows:

#### Advantages

- All records are stored in one file
 Simple to set up and use Efficient for smaller businesses and datasets

#### Challenges

- Difficult to make changes to the record structure
- Inefficient for large-scale record keeping
- Increased redundancy due to duplicate records
- Data inconsistencies are easy to create

## TOPIC 3: LIMITATIONS OF FLAT FILES

## Limitations of Flat Files (Spreadsheets & CSVs)

A **flat file** stores all data in a single table — every row is a record, every column is a field. Simple and familiar, but this structure breaks down quickly in the real world.

---

### The Core Problem: Everything in One Table

Imagine a school wants to track students and their courses. In a flat file, it looks like this:

| Student ID | Student Name | Age | Course 1 | Teacher 1 | Course 2 | Teacher 2 |
|---|---|---|---|---|---|---|
| 001 | Mowa | 22 | Math | Mr. Bello | English | Mrs. Ade |
| 002 | Tunde | 21 | Math | Mr. Bello | Science | Dr. Kalu |
| 003 | Amaka | 23 | English | Mrs. Ade | — | — |

Now the problems become obvious:

---

### 1. **Data Redundancy**
"Mr. Bello teaches Math" is written twice (for Mowa and Tunde). If you have 500 students taking Math, Mr. Bello's name appears 500 times. You're storing the same information over and over, wasting space.

### 2. **Update Anomalies**
If Mr. Bello changes his name or leaves and a new teacher takes over Math, you'd have to find and update *every single row* that mentions him. Miss one, and now your data is inconsistent — some rows say one thing, others say another.

### 3. **No Relationships Between Data**
What if a student takes 5 courses? You'd need to add Course 3, Course 4, Course 5 columns... and most rows would be empty. The structure doesn't naturally handle "one student, many courses."

### 4. **Duplicate / Inconsistent Entries**
Someone might type "Mr Bello" in one row and "Mr. Bello" in another. The file has no way to enforce that these must match — so searches and reports can silently miss data.

### 5. **No Access Control**
A spreadsheet is essentially all-or-nothing. You can't easily say "this person can see student names but not ages." Everyone with the file sees everything.

### 6. **Poor Performance at Scale**
A CSV with 50 rows is fine. A CSV with 2 million rows becomes painfully slow to open, search, or sort — especially without any indexing system.

---

### Why Relational Databases Solve This

A relational database would split this into **separate tables** — one for Students, one for Courses, one for Teachers — and link them with IDs. "Mr. Bello teaches Math" is stored *once*, and every student who takes Math just references that record. Update it in one place, and it's updated everywhere instantly.

That's the fundamental leap from flat files to relational databases — and why tools like SQL exist.

## TOPIC 4: Relational Databases

That is what a relational database does: it keeps related types of data in tables, and each table can have relationships with other tables that link all the information together.

![RDB TABLES](https://github.com/DataWithMowa/Cisco-Data-Analytics-Essentials/blob/main/Introduction%20to%20Relational%20Database%20%26%20SQL/Data%20Basic%20Management/RDB%20TABLES.png)

All the information about tables, attributes, relationships and other elements of a relational database is documented in a schema, which is a formal description that defines the structure of the database. The schema can be easily modified; for example, it is possible to add a new column to a table, add new tables, or delete old ones using a simple command.

With this structure, we can record and store each person’s information only one time and then link it with the movies where that person plays a role or if directs a movie (Some people do both things—this is why it is useful to have a People table instead of Directors and Actors tables). This way, if we need to change anything about a person, we only need to do it in one place and avoid the redundancies and inconsistencies associated with flat file databases.

The simplicity, ease of use, and accuracy of the relational database model makes it the most popular database framework in use today. However, the cost, maintenance, and lack of scalability mean that it is not suitable for every use case.

If we want to use a relational database, there are many tools available to set one up and use it. This type of tool is called a Relational Database System (RDBS): software built to create any number of relational databases and work with them to store and retrieve data. The most well-known RDBSs are MySQL, PostgreSQL, Oracle Rdb, and Microsoft SQL Server.

##### The advantages and challenges of relational databases are as follows:

#### Advantages

- Data is stored in interrelated tables, allowing for storing complex data efficiently
- Increased security and data accuracy
- Ideal for large data storage

#### Challenges

- RDBS software can be expensive to set up and maintain
- RDBSs require a specific skillset to use
- Performance can be slow if there are multiple large and complex tables

## TOPIC 5: Entity Relationship Diagrams (ERDs)

Here's what it's saying in plain English:

---

Flat files like spreadsheets have limitations (as we just covered). Relational databases were built to fix those problems — and their superpower is the ability to **link tables together**.

But linking tables requires a bit more structure. To understand that structure, you use an **ERD (Entity Relationship Diagram)** — basically a visual map that shows you what tables exist in a database and how they connect to each other.

---

### The two keys that make it all work:

**Primary Key**
Every table has one special field called the primary key. Its only job is to **uniquely identify each row**. Think of it like a national ID number — no two people can have the same one, and you can't leave it blank. In the example, each table (Content, User, Rating) has its own primary key.

**Foreign Key**
This is how tables talk to each other. A foreign key in one table is just a **reference pointing to the primary key of another table**. For example, the User table has a field called `content_id` — that field points to the `content_id` primary key in the Content table. That's what creates the *relationship* between the two tables.

Unlike primary keys, foreign keys *can* repeat — multiple users can be linked to the same piece of content, and that's perfectly fine.

---

**The bottom line:** Primary keys uniquely identify rows within a table. Foreign keys link one table to another. Together, they keep the data accurate and make it possible to combine information from multiple tables when you need it.

