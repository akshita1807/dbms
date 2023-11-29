# DBMS Last Minute Revision notes✅

# Data
raw information

# DataBase
A database is an organized collection of data,stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). 

# DBMS-database management system
A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner. It allows users to create, update and delete the data.Provides safety and easy reterival.

# File Processing System
File System manages data using files.But there is more inconsistency and redundancy while storing data in FPS.So DBMS was introduced.
The file system does not incorporate any backup and recovery of data if a file is lost or corrupted.Data access is also difficult.

# Why DBMS or Advantages of DBMS?
-provides data integrity i.e correctness of data  
-makes data sharing and retrieval easy  
-reduce data redundancy  
-provides data security  
-provides data backup and recovery  

# Disadvantages of DBMS?
-complex to setup and maintain  
-The cost of purchasing, maintaining and upgrading a DBMS can be high.  

# DBMS architecture
This framework is used to describe the structure of a specific database system.The three schema architecture contains three-levels. It breaks the database down into three different categories.

**External schema** -represent the portion of the database that a particular user or group of users is interested in.Defines the user interfaces, views, and access privileges.
Presents a customized and simplified view of the database to meet the specific needs of different user groups.
Shields users from the complexity of the underlying database structure.

**logical or conceptual schema**-Defines the structure of the entire database, including tables, relationships, constraints, and security policies..Programmers and database administrators work at this level.

**Internal schema or physical schema**-The internal level has an internal schema which describes the physical storage structure of the database.It is used to define that how the data will be stored

**Data base administrator(DBA)- has entire knowledge of database**

# RDBMS-Relational DataBase Model
An RDBMS stores data in tables with rows and columns, and uses SQL (Structured Query Language) to manipulate the data.

# NoSQL DBMS
A NoSQL DBMS stores data in non-relational data structures, such as key-value pairs, document-based models, or graph models.For eg MOngo DB


# E-R Diagram
stands for entity relationship diagram tells how the data is stored.It is the blueprint of how data is stores.It has three components-entity,relationships and attributes.

# Entity
An entity is a real-world object.It can be a person, place, event, or thing.For eg student.There are two types of entities-weak entity and strong entity.
weak entity-dependent on another entity.for eg bank account,is a weak entity ,it can't exist without bank.represented by double outlined rectangle
strong entity-can be identified uniquely.for eg bank.represented by rectangle

# Attributes
Attributes are properties or characteristics of entities. They describe the data we want to store about the entities.For the "Student" entity, attributes might include "StudentID," "Name," and "DateOfBirth."

**Types of attributes**
**key attribute**-
A key attribute is an attribute that is part of the primary key of an entity.
Example: In a "Student" entity, the "StudentID" attribute is a key attribute.

**Composite attribute**-composite attributes are composed of one or more simple attributes.for eg.An address attribute might be composed of sub-parts like "Street," "City," and "Zip Code."

**Multivalued attribute**-attribute holding multivalues at a same time. For eg phone number can be many so phone number is a multivalued attribute.Represent by double lined oval.

**Derived attribute**-A derived attribute is an attribute whose value can be derived from other attributes in the database.The "Age" of a person can be derived from the "DateOfBirth" attribute.represented by dotted oval



# Relationships
Relationships represent connections or associations between entities. They describe how entities interact with each other.  
**One-to-one**=In a one-to-one relationship, one instance of an entity is associated with only one instance of another entity, and vice versa.
Example: A relationship between "Person" and "Passport," where each person has only one passport, and each passport is issued to only one person.

**One-to-many**=In a one-to-many relationship, one instance of an entity is associated with multiple instances of another entity, but each instance of the second entity is associated with only one instance of the first entity.
Example: A relationship between "Department" and "Employee," where one department can have many employees, but each employee belongs to only one department.

**Many-to-one**=In a many-to-one relationship, multiple instances of one entity are associated with a single instance of another entity.
Example: In the same "Department" and "Employee" relationship, but viewed from the opposite perspective, where many employees belong to a single department.

**Many-to-many**=In a many-to-many relationship, multiple instances of one entity are associated with multiple instances of another entity.
Example: A relationship between "Student" and "Course," where a student can enroll in multiple courses, and a course can have multiple students.



# Functional dependency
relationship between two sets of attributes where one attribute determines the value of another attribute

we denote functional dependencies using a notation. It contains two main components: the left-hand side (LHS) and the right-hand side (RHS) of an arrow (->). 

For example, if we have a table with attributes "A," "B," and "C," and attribute "A" determines the values of attributes "B" and "C," you would denote it as

A -> B, C


**trivial functional dependency**-A trivial functional dependency occurs when Q is a subset of P in −
P ->Q

**non-trivial functional dependency**-A non-trivial functional dependency occurs when Q is not a subset of P in −
P -> Q

# Axiom rules in functional Dependency


**primary rules**-
Axiom of Reflexivity: If A is a set of attributes and B is a subset of A, then A holds B. If B⊆A then A→B. This property is trivial property.

Axiom of Augmentation: If A→B holds and Y is the attribute set, then AY→BY also holds. That is adding attributes to dependencies, does not change the basic dependencies. If A→B, then AC→BC for any C.

Axiom of Transitivity: Same as the transitive rule in algebra, if A→B holds and B→C holds, then A→C also holds. A→B is called A functionally which determines B. If X→Y and Y→Z, then X→Z.


**secondary rules**-
Union: If A→B holds and A→C holds, then A→BC holds. If X→Y and X→Z then X→YZ.

Composition: If A→B and X→Y hold, then AX→BY holds.

Decomposition: If A→BC holds then A→B and A→C hold. If X→YZ then X→Y and X→Z.

Pseudo Transitivity: If A→B holds and BC→D holds, then AC→D holds. If X→Y and YZ→W then XZ→W.

**why we use axiom rules in functional dependency?**  
We use Armstrong Axioms to determine the functional dependency in the database. Generally, it is used to derive other functional dependency in the database using the given functional dependency.

# Closures
 Closure of an Attribute can be defined as a set of attributes that can be functionally determined from it. A closure is represented by A+.

for eg:
Given relational schema R( P Q R S T U V) having following attribute P Q R S T U and V, also there is a set of functional dependency denoted by FD = { P->Q, QR->ST, PTV->V }.

Determine Closure of (QR)+ and (PR)+
QR+  QRST
PR+  PRQ

# Keys
keys are  widely used to identify the tuples(rows) uniquely in the table.
Types of keys:

**Super Key**-The set of attributes that can uniquely identify a tuple is known as Super Key. For Example, STUD_NO, (STUD_NO, STUD_NAME), etc.It supports NULL values.

**Candidate Key**-The minimal set of attributes that can uniquely identify a tuple is known as a candidate key. For Example, STUD_NO in STUDENT relation. 
It is a subset of super key.
It must contain unique values.
It can contain NULL values.

**Primary Key**-There can be more than one candidate key in relation out of which one can be chosen as the primary key. For Example, STUD_NO, as well as STUD_PHONE, are candidate keys for relation STUDENT but STUD_NO can be chosen as the primary key.
It can identify only one tuple (a record) at a time.
It has no duplicate values, it has unique values.
It cannot be NULL.

**Alternate Key**-The candidate key other than the primary key is called an alternate key.
All the keys which are not primary keys are called alternate keys.

**Composite Key**
Sometimes, a table might not have a single column/attribute that uniquely identifies all the records of a table. To uniquely identify rows of a table, a combination of two or more columns/attributes can be used.  It still can give duplicate values in rare cases. So, we need to find the optimal set of attributes that can uniquely identify rows in a table.

It acts as a primary key if there is no primary key in a table
Two or more attributes are used together to make a composite key.

**Foreign Key**-A foreign key is a column or a set of columns in a table that refers to the primary key or a unique key in another table. It establishes a connection between the data in the two tables.

The primary purpose of a foreign key is to maintain referential integrity. It ensures that relationships between tables are valid by enforcing that values in the foreign key column(s) correspond to existing values in the referenced table's primary key or unique key column(s).

**Unique Key**-A unique key refers to a column/a set of columns that identify every record uniquely in a table. All the values in this key would have to be unique. Remember that a unique key is different from a primary key. It is because it is only capable of having one null value. A primary key, on the other hand, cannot have a null value.

# Data Redundancy
it means having multiple copies of same data in the database.Causes increase in storage and space.It occurs when data is not normalised. Redundancy in relation may cause insertion, deletion, and update anomalies

**Anomalies**  
Insertion Anamoly-This problem happens when the insertion of a data record is not possible without adding some additional unrelated data.

Deletion Anamoly-This happens when deletion of a data record results in loosing some unrelated information that was stored as a part of the record that was deleted from table.

Updation Anamoly-When we want to update single piece of data,so we have to do it at all places.If updation do not occur at all places than database will become inconsistence.

Data redundancy and anomalies takes place when data is not normalized.So to avoid this ,normalisation came into action

# Normalisation
Normalization in the context of Database Management Systems (DBMS) is a process of organizing and structuring a relational database to reduce data redundancy and improve data integrity.The goal of normalization is to design a database schema that minimizes data anomalies and ensures that data is stored in an organized and efficient manner.Normalization divides the larger table into smaller and links them using relationships.

Types of Normalisation:

**1NF**-A table is referred to as being in its First Normal Form if atomicity of the table is 1.
Here, atomicity states that a single cell cannot hold multiple values. It must hold only a single-valued attribute.
The First normal form disallows the multi-valued attribute, composite attribute, and their combinations.

**2NF**-Table must be in 1 NF
The table should not possess partial dependency.
Partial Dependency-non-prime attributes are fully functionally dependent on the entire candidate key.
prime attributes-which are part of candidate key
non-prime attributes-which are not a part of candidate key

for eg: AB->ABCD here AB is the candidate key ,so AB will be the prime attributes and CD will be the non prime attributes

**3NF**-Table must be in 2NF
The second condition is that there should be no transitive dependency for non-prime attributes, which indicates that non-prime attributes (which are not a part of the candidate key) should not depend on other non-prime attributes in a table. Therefore, a transitive dependency is a functional dependency in which A → C (A determines C) indirectly, because of A → B and B → C (where it is not the case that B → A).

**BCNF**-Boyce Codd Normal Form is also known as 3.5 NF. It is the superior version of 3NF .
Table must be in 3NF
if have a functional dependency X → Y. In the particular functional dependency, X has to be the part of the super key of the provided table.

# Disadvantages of Normalisation
It is very time-consuming and difficult to normalize relations of a higher degree.  
Careless decomposition may lead to a bad database design, leading to serious problems.  

# DeNormalisation
The process of taking a normalized schema and making it non-normalized is called denormalization.Denormalization is a database optimization technique in which we add redundant data to one or more tables. This can help us avoid costly joins in a relational database.Denormalization is the process of intentionally introducing redundancy into a relational database by combining tables or incorporating redundant data. This contrasts with the normalization process, where the goal is to reduce redundancy and dependencies. 

# Indexing
Indexing is a data structure technique which allows you to quickly retrieve records from a database file. It consists of a set of key-value pairs, where the key is the indexed column or a combination of columns, and the value is a pointer to the corresponding data row. Indexing reduces the number of disks required to access a particular data by internally creating an index table.Types of indexing-

**Primary indexing**-he indexing or the index table created using Primary keys is known as Primary Indexing. It is defined on ordered data. As the index is comprised of primary keys, they are unique, not null, and possess one to one relationship with the data blocks.
Characteristics of Primary Indexing:
Search Keys are unique.  
Search Keys are in sorted order.  
Search Keys cannot be null as it points to a block of data.  
Fast and Efficient Searching.  

Primary indexing is further divided into sparse and dense indexing-
  
**Sparse indexing**-Sparse indexing consumes lesser space than dense indexing, but it is a bit slower as well. We do not include a search key for every record despite that we store a Search key that points to a block. The pointed block further contains a group of data. Sometimes we have to perform double searching this makes sparse indexing a bit slower.

**Dense indexing**-if each and every record/key from mainfile is stored in the index file,it is called dense indexing.This helps you to search faster but needs more space to store index records.


**Clustered**-Clustered Indexing is used when there are multiple related records found at one place. It is defined on ordered data. The important thing to note here is that the index table of clustered indexing is created using non-key values which may or may not be unique. To achieve faster retrieval, we group columns having similar characteristics. The indexes are created using these groups and this process is known as Clustering Index.

**Secondary**-It is a two-level indexing technique used to reduce the mapping size of the primary index. The secondary index points to a certain location where the data is to be found but the actual data is not sorted like in the primary indexing. Secondary Indexing is also known as non-clustered Indexing.Search Keys are sorted but actual data may or may not be sorted.Requires more time than primary indexing.


# Transactions
Transactions can be defined as a group of tasks performing some useful work.Transactions acess and modiefies data with the help of read and write operations.
A transaction in a database system must maintain Atomicity, Consistency, Isolation, and Durability − commonly known as ACID properties − in order to ensure accuracy, completeness, and data integrity.
Transactions has only two results.Success--if all set of instructions are executed successfully or failure--if all set of instructions are not executed successfully.

# ACID Properties
**Atomicity**-This property states that a transaction must be treated as an atomic unit, that is, either all of its operations are executed or none. There must be no state in a database where a transaction is left partially completed.

**Consistency**-The database must remain in a consistent state after any transaction. No transaction should have any adverse effect on the data residing in the database. If the database was in a consistent state before the execution of a transaction, it must remain consistent after the execution of the transaction as well.

**Isolation**-No transaction will affect the existence of any other transaction.
It shows that the data which is used at the time of execution of a transaction cannot be used by the second transaction until the first one is completed.

**Durability**-The database should be durable enough to hold all its latest updates even if the system fails or restarts. 

**Different transaction states**-
Active state(when transaction starts)  
Partially Committed state  
committed state  
failed state  
aborted state  
terminated state  

# Conflicts and problems in transactions

**Dirty Read**-A dirty read problem may arise when the number of transactions (that perform on shared data) executes simultaneously.
It occurs when a transaction reads the data that has been updated by another transaction that is still uncommitted.
Due to some reason a transaction gets rollbacked and therefore another transaction processes with dirty data.

**Un-repeatable read**-when a transaction reads the same row twice and gets a different value each time. For example, suppose transaction T1 reads data. Due to concurrency, another transaction T2 updates the same data and commit, Now if transaction T1 rereads the same data, it will retrieve a different value.It means transactions here are not isolated and one transaction is interrupting another.

**Phantom read**-
It happens when a transaction reads a set of rows that match a certain condition, but, during the course of the transaction, another transaction inserts or deletes rows that also meet the specified condition
for eg: T1-Reads a set of rows from a certain table based on a condition (e.g., a range of values).
T2-Inserts new rows or deletes existing rows that satisfy the same condition used by Transaction A. It will create a problem

**Scheduling**-is a process of lining the transactions and executing them one by one. When there are multiple transactions that are running in a concurrent manner and the order of operation is needed to be set so that the operations do not overlap each other, Scheduling is brought into play.The sequence of operation is called schedule.
It is of two types-

serial schedules-serial schedule is one in which no transaction starts until a running transaction has ended are called serial schedules.

non-serial schedule-Multiple transactions execute concurrently.
Operations of all the transactions are inter leaved or mixed with each other.
parallel processing happens
 
non serial schedules are further divided into:

serializable-This is used to guarantee the database's consistency. It is mostly used in Non-Serial scheduling to ensure that the schedule will not result in any inconsistencies.   Only when the non-serial schedule is equivalent to the serial schedules for an n number of transactions is it considered to be serializable. Multiple transactions can run at the same time because concurrency is allowed in this instance.

It is further divided into :

conflict serializable-If a schedule can be turned into a serial schedule by switching non-conflicting operations, it is called conflict serializable. 
Two operations are conflicting if they access the same data item and at least one of them is a write operation

view serializable-If a schedule is viewed equal to a serial schedule, it is called view serializable (no overlapping transactions).Conflict serializable schedule is also view serializable.

non-serializable-
It is further divided into recoverable and non-recoverable.(not so asked)


# Locks
A database lock  is a mechanism to protect a shared piece of data from getting updated by two or more database users at the same time.When a single database user or session has acquired a lock then no other database user or session can modify that data until the lock is released.Locks gurantee isolation.
Locks are of two tyes:  
**Shared Lock**-Shared lock is required for reading a data item.In shared lock many transactions may hold a lock on the same data item.When more than one transaction is allowed to read the data items then that is known as shared lock.

**Exclusive locks**-When any transaction is about to perform the write operation then the lock on the data item is an exclusive lock.Because if we allow more than one transaction then that will lead to the inconsistency in the database.



# Views
A view in SQL is a virtual table that is based upon the result-set of an SQL statement.A view will also have rows and columns just like a real table in a database.Simply a view is nothing but a stored SQL Query.A view can contain all the rows of a table or specific rows based on some condition.SQL functions conditions and join statements to a view and present the data just like the data is produced from a single table.
They are of two types-simple views and complex views

# NVL
The NVL function allows you to replace null values with a specified default value. The syntax of the NVL function is as follows:

NVL(expr1, expr2)
expr1: The expression to be checked for null. If expr1 is null, the function returns expr2.  
expr2: The value to be returned if expr1 is null.  


# Triggers
A trigger is a special kind of stored procedure that is activated ("triggered") in response to a particular event in a database.Trigger is called automatically when a data modification event occurs against a table.
Types of triggers-
1) DML triggers are automatically fired when an INSERT, UPDATE or DELETE event occurs on a table.  
2) DDL triggers are automatically invoked when a CREATE, ALTER, or DROP event occurs in a    database.  
