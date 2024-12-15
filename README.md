# SQL Assignment Week 1


## *What You'll Need*
- A computer with internet access.
- A code editor (e.g., Visual Studio Code).
- MySQL Workbench or another SQL database environment.

---



## *Submission Instructions*
1. Answer every question below and put your responses in a file named `answers.md`
2. Push your completed `answers.md` file to your GitHub repository.
3. Submit the GitHub link for review.

---

## **Assignment Questions**

1. State and Explain the components of a DBMS(Database Management System)

### 1. **Database Engine**
   - **Definition:** The core service for storing, processing, and securing data.
   - **Explanation:** It handles the execution of queries and ensures that data is efficiently retrieved and manipulated. This component manages data storage on disk and performs operations like indexing, transaction management, and concurrency control.

### 2. **Database Schema**
   - **Definition:** The logical structure of the database.
   - **Explanation:** It defines how data is organized, including tables, relationships, constraints, and views. The schema acts as a blueprint for the database and determines how data is stored and accessed.

### 3. **Query Processor**
   - **Definition:** The component that interprets and executes database queries.
   - **Explanation:** It translates user-submitted queries (e.g., SQL commands) into a form that the database engine can execute. The processor optimizes queries for efficient execution.

### 4. **Transaction Management**
   - **Definition:** The system that ensures the consistency and reliability of the database.
   - **Explanation:** It manages transactions to maintain the ACID (Atomicity, Consistency, Isolation, Durability) properties. It ensures that multiple users can access the database simultaneously without conflicts or data corruption.

### 5. **Storage Manager**
   - **Definition:** The module responsible for data storage and retrieval.
   - **Explanation:** It handles the physical storage of data on disk, organizes it using structures like indexes, and manages data access to ensure efficiency. It also includes backup and recovery mechanisms.

### 6. **Metadata Catalog (Data Dictionary)**
   - **Definition:** A repository of information about the database structure.
   - **Explanation:** It contains details like table definitions, column data types, constraints, and user permissions. This helps the DBMS and users understand the organization of the database.

### 7. **Concurrency Control Manager**
   - **Definition:** The mechanism that manages concurrent access to the database.
   - **Explanation:** It ensures that multiple users can work with the database simultaneously without interference or inconsistency, using techniques like locking and versioning.

### 8. **Authorization and Security Manager**
   - **Definition:** The component responsible for database security.
   - **Explanation:** It controls user access, ensuring only authorized users can perform specific operations. This includes managing authentication, roles, and permissions.

### 9. **User Interface (UI)**
   - **Definition:** The platform through which users interact with the DBMS.
   - **Explanation:** It provides tools, commands, or graphical interfaces for users to define, query, and manage the database easily.

2. What is a relational database? Give 4 examples.
A **relational database** is a type of database that stores and organizes data in a structured format, using **tables** consisting of rows and columns. 

### Examples of Relational Databases:

1. **MySQL**  
   - Open-source and widely used for web applications, such as WordPress and e-commerce platforms.
   - Popular for its speed, scalability, and ease of use.

2. **PostgreSQL**  
   - Advanced open-source relational database with support for complex queries, JSON data, and extensibility.
   - Known for robustness and adherence to SQL standards.

3. **Oracle Database**  
   - A commercial relational database system with advanced features for large-scale enterprise applications.
   - Commonly used in financial and business applications.

4. **Microsoft SQL Server**  
   - A relational database developed by Microsoft, widely used in business applications.
   - Integrates well with other Microsoft products like Power BI and Azure. 

3. State and Explain three classifications of SQL?
SQL (**Structured Query Language**) is classified based on the type of operations it performs on a database. The three main classifications of SQL are:

---

### 1. **Data Definition Language (DDL)**
   - **Definition:** DDL consists of SQL commands used to define or modify the structure of database objects like tables, indexes, schemas, and views.
   - **Purpose:** It defines the schema of the database and manages its structure.
   - **Key Commands:**
     - `CREATE`: Creates a new table, database, index, or view.
     - `ALTER`: Modifies an existing table or database structure.
     - `DROP`: Deletes a table, database, or view.
     - `TRUNCATE`: Removes all records from a table without logging individual row deletions.
   - **Example:**
     ```sql
     CREATE TABLE Students (
         ID INT PRIMARY KEY,
         Name VARCHAR(50),
         Age INT
     );
     ```
   - **Explanation:** DDL commands do not manipulate the data but only the structure of the database. These commands are auto-committed, meaning changes are immediately saved.

---

### 2. **Data Manipulation Language (DML)**
   - **Definition:** DML consists of SQL commands used to insert, update, delete, and retrieve data stored in a database.
   - **Purpose:** It enables users to work with the data itself.
   - **Key Commands:**
     - `SELECT`: Retrieves data from the database.
     - `INSERT`: Adds new records to a table.
     - `UPDATE`: Modifies existing records.
     - `DELETE`: Removes records from a table.
   - **Example:**
     ```sql
     INSERT INTO Students (ID, Name, Age) 
     VALUES (1, 'Alice', 20);
     ```
   - **Explanation:** DML commands focus on data manipulation rather than structure. These changes are not auto-committed, so they can be rolled back if necessary.

---

### 3. **Data Control Language (DCL)**
   - **Definition:** DCL consists of SQL commands used to control access to the database and manage permissions for users.
   - **Purpose:** It ensures database security and defines which users can perform specific operations.
   - **Key Commands:**
     - `GRANT`: Assigns permissions to users.
     - `REVOKE`: Removes permissions from users.
   - **Example:**
     ```sql
     GRANT SELECT, INSERT ON Students TO User1;
     ```
   - **Explanation:** DCL commands allow administrators to control access to specific parts of the database, ensuring data confidentiality and security.

---


4. What is the difference between a Primary Key and a Foreign Key?
A primary key is a column in a table that uniquely identifies each record in that table while a foreign key is a column in a table that creates a relationship between two tables by referencing the primary key of another table.
5. What is an Entity-Relationship Diagram?
It is a visual representation of the relationships between entities in a database and help in designing the structure of a database by illustrating the key components and relationships.
6. What are the advantages of relational databases?

---

### **1. Structured Organization**
- **Data Storage in Tables**: Data is organized into rows and columns, making it highly structured and easy to understand.
- **Normalization**: Reduces data redundancy and ensures data integrity by breaking data into related tables.

---

### **2. Data Integrity and Accuracy**
- **Constraints**: Features like primary keys, foreign keys, and unique constraints enforce rules and maintain data accuracy.
- **Referential Integrity**: Ensures consistency between related tables (e.g., a foreign key must match a primary key in another table).

---

### **3. Flexibility**
- **Dynamic Queries**: SQL (Structured Query Language) allows users to retrieve, update, and manipulate data in numerous ways without altering the database structure.
- **Scalable Schema**: Tables and relationships can be added or modified as data needs evolve.

---

### **4. Data Security**
- **Access Control**: Permissions can be set at various levels (database, table, column, or row), ensuring only authorized users can access or modify data.
- **Encryption**: Data can be encrypted both in transit and at rest to protect against unauthorized access.

---

### **5. Reliability and Consistency**
- **ACID Properties**: 
  - **Atomicity**: Ensures all parts of a transaction are completed or none are.
  - **Consistency**: Maintains database validity before and after a transaction.
  - **Isolation**: Prevents concurrent transactions from interfering with each other.
  - **Durability**: Ensures committed transactions persist even after a system failure.

---

### **6. Standardized Language**
- **SQL Support**: Relational databases use SQL, a widely adopted standard, making it easy for developers to work with them and migrate between systems.

---

### **7. Scalability**
- **Horizontal and Vertical Scaling**: Relational databases can scale to handle increased data or user demands.
- **Optimized Performance**: Indexing, caching, and query optimization improve performance for large datasets.

---

### **8. Interoperability**
- **Cross-Platform Compatibility**: Most relational database systems (e.g., MySQL, PostgreSQL, SQL Server) are compatible with various operating systems, programming languages, and tools.

---

### **9. Mature Ecosystem**
- Relational databases have been in use for decades, leading to robust documentation, community support, and a wide range of third-party tools for management and analytics.

---

### **10. Backup and Recovery**
- **Automatic Backup**: Many systems provide built-in tools for regular backups.
- **Transaction Logs**: Enable recovery to a specific point in time in case of data corruption or failure.

---

### **11. Business Intelligence and Reporting**
- **Integration with BI Tools**: Relational databases can easily connect to business intelligence tools to generate detailed reports and analyses.
- **Aggregation and Join Queries**: Facilitate complex data analysis across multiple tables.

---

7. State four types of data type used to store data in tables?
   
---

### 1. **Numeric Data Types**
   - These types are used to store numbers (integers, decimals, and floating-point values). Common numeric data types include:
     - **INT** (Integer): Stores whole numbers, e.g., `10`, `-100`.
     - **FLOAT** or **REAL**: Stores floating-point numbers, e.g., `3.14`, `-5.67`.
     - **DECIMAL** or **NUMERIC**: Stores numbers with fixed precision and scale, e.g., `123.45`.
     - **BIGINT**: Stores larger integers (often used for counting large datasets).

   **Example**: 
   - **Salary DECIMAL(10, 2)** stores salaries up to 10 digits, with 2 digits after the decimal point.

---

### 2. **Character/String Data Types**
   - These types store text-based data, such as names, descriptions, and addresses. They can vary in length, and some are fixed while others are variable.
     - **CHAR(n)**: A fixed-length string, where `n` is the number of characters. Padding is added if the string is shorter than `n`.
     - **VARCHAR(n)**: A variable-length string that can store up to `n` characters. It only takes up space for the actual data.
     - **TEXT**: A flexible-length string for larger text data, often used for descriptions or long-form content.

   **Example**:
   - **Username VARCHAR(50)** can store a name up to 50 characters long.

---

### 3. **Date and Time Data Types**
   - These types store date and time values, allowing you to capture timestamps or durations.
     - **DATE**: Stores date values (year, month, day), e.g., `2024-12-15`.
     - **TIME**: Stores time values (hour, minute, second), e.g., `14:30:00`.
     - **DATETIME** or **TIMESTAMP**: Stores both date and time values, e.g., `2024-12-15 14:30:00`.
     - **YEAR**: Stores a year in a two-digit or four-digit format (e.g., `2024`).

   **Example**:
   - **OrderDate DATETIME** stores the exact date and time an order was placed.

---

### 4. **Boolean Data Type**
   - This type is used to store binary values, representing true or false conditions.
     - **BOOLEAN**: Typically stores `TRUE` or `FALSE` values. Some systems use `1` for true and `0` for false.
     - **BIT**: Often used in some DBMS to store binary values, usually represented as `0` or `1`.

   **Example**:
   - **IsActive BOOLEAN** stores whether a user account is active or not (`TRUE` or `FALSE`).

---

8. What is the purpose of a database management system (DBMS)? 

### Key Purposes of a DBMS:

---

### 1. **Data Storage, Retrieval, and Management**
   - **Efficient Storage**: DBMS provides a way to store large amounts of data efficiently while ensuring optimal space utilization.
   - **Easy Retrieval**: With a well-defined structure, users can easily retrieve data using queries (typically SQL) to get relevant information from the database.
   - **Data Manipulation**: Users can perform various operations on the data such as insertion, updating, deletion, and retrieval.

---

### 2. **Data Integrity**
   - **Consistency**: A DBMS ensures that the data remains consistent and follows predefined rules (like constraints, keys, and relationships). For example, a database can enforce referential integrity to ensure that a foreign key value in one table corresponds to a valid record in another.
   - **Validation**: It validates the data entered into the system, ensuring that it meets specific criteria (e.g., data type, range, format).

---

### 3. **Data Security**
   - **Access Control**: DBMS allows administrators to define access permissions, ensuring that only authorized users can access or modify specific data. For example, some users may only have read access, while others have both read and write access.
   - **Data Encryption**: DBMSs often offer encryption features to protect sensitive data, both when it's stored in the database and when it's being transmitted.

---

### 4. **Data Redundancy Control**
   - **Eliminating Redundancy**: DBMS reduces data redundancy (repeated storage of the same data) through normalization, ensuring that data is stored in the most efficient way and minimizing the chances of data inconsistencies.
   - **Centralized Management**: All data is stored in a centralized location, which makes it easier to manage, update, and control.

---

### 5. **Concurrency Control**
   - **Multi-User Support**: A DBMS allows multiple users to access and modify the database simultaneously without conflicting with each other, ensuring that transactions are handled properly.
   - **Locking Mechanisms**: It uses locks and transaction management to ensure that data is consistent and that users' actions do not interfere with each other in concurrent environments.

---

### 6. **Backup and Recovery**
   - **Data Backup**: DBMSs provide tools for regular backups, which are essential for preventing data loss due to system failures.
   - **Data Recovery**: In case of a system crash or data corruption, DBMSs offer recovery mechanisms to restore the database to a consistent state, minimizing downtime and data loss.

---

### 7. **Support for Data Independence**
   - **Logical Data Independence**: Changes in the database's logical structure (e.g., adding a new column or table) can be made without affecting the applications that use the database.
   - **Physical Data Independence**: Changes to the physical storage of data (e.g., how it's stored on disk) do not affect how the data is accessed or the structure of the database.

---

### 8. **Efficient Query Processing**
   - **Optimization**: DBMS uses query optimization techniques to process SQL queries in the most efficient way possible, reducing the time and resources needed to retrieve data.
   - **Indexes**: It can create indexes to speed up query execution, allowing faster access to large datasets.

---

### 9. **Transaction Management and ACID Properties**
   - **Atomicity**: Ensures that all parts of a transaction are completed successfully, or none are.
   - **Consistency**: Guarantees that the database remains in a valid state before and after a transaction.
   - **Isolation**: Ensures that the operations of one transaction do not interfere with another, even when transactions are executed concurrently.
   - **Durability**: Once a transaction is committed, its changes are permanent, even in case of a system failure.

---

### 10. **Data Modeling and Reporting**
   - **Schema Design**: DBMS allows the creation of schemas that define the structure of the database, including tables, relationships, and constraints.
   - **Reporting**: It often integrates with reporting tools or query languages (like SQL) to generate reports and insights based on the stored data.

---


*How to edit a [markdownfile](https://www.markdownguide.org/basic-syntax/#headings)*

###  NOTE: You should not fork the repository
