# JOINS
A JOIN clause is used to combine rows from two or more tables, based on a related column between them.
### Types of joins
Inner<br>
 JoinLeft<br>
  JoinRightJoin <br>
  Full Join



## Inner Join
An INNER JOIN is the default join which retrieves the intersection of two tables. It compares each row of the first table with each row of the second table. If the pairs of these rows satisfy the join-predicate, they are joined together.
syntax
`SELECT column_name(s) 
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;`
#### Exampe
syntax<br>
<img src="/images/innerjoinsyntax.JPG" alt="inner join syntax"/> <br>
<img src="/images/product table.JPG" alt="product
table"/><br>
<img src="/images/product.JPG" alt="product syntax"/><br>
<img src="/images/categories table.JPG" alt="categories table "/><br>
<img src="/images/category.JPG" alt="categories syntax"/>

## Left Join

LEFT JOIN returns all the rows of the table on the left side of the join and matches rows for the table on the right side of the join. For the rows for which there is no matching row on the right side, the result-set will contain null

syntax<br>
`SELECT column_name(s) 
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;`
#### Example

<img src="/images/left join syntax.JPG" alt="left join syntax"/> <br>
<img src="/images/left join table.JPG" alt="left join table"/> <br>
<img src="/images/orders table syntax.JPG" alt="orders
syntax"/><br>
<img src="/images/orders table.JPG" alt="orders table"/><br>
<img src="/images/customers syntax.JPG" alt="customers syntax "/><br>
<img src="/images/customers table.JPG" alt="customers table"/>


## Right Join 
returns all rows from the right table, even if there are no matches in the left table.

syntax
`SELECT column_name(s) 
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;`

## Example

<img src="/images/orders table syntax.JPG" alt="orders
syntax"/><br>
<img src="/images/orders table.JPG" alt="orders table"/><br>
<img src="/images/customers syntax.JPG" alt="customers syntax "/><br>
<img src="/images/customers table.JPG" alt="customers table"/>

<img src="/images/right join syntax.JPG" alt="right join syntax"/> <br>
<img src="/images/right join table.JPG" alt="right join table"/> <br>

## Full Join
 returns rows when there is a match in one of the tables.Creates the result-set by combining results of both LEFT JOIN and RIGHT JOIN. The result-set will contain all the rows from both tables

syntax
`SELECT column_name(s) 
FROM table1
FULL JOIN table2
ON table1.column_name = table2.column_name;`

#### Example

<br>
<img src="/images/books table.JPG" alt="books table"/><br>
<img src="/images/books syntax.JPG" alt="books syntax "/><br>
<img src="/images/students table.JPG" alt="students table"/> <br>
<img src="/images/students syntax.JPG" alt="students syntax"/><br>
<img src="/images/right join syntax.JPG" alt="right join syntax"/> <br>
<img src="/images/right join table.JPG" alt="right join table"/> <br>

# NORMALIZATION
Normalization is the process of organizing the data in the database.
Normalization is used to minimize the redundancy from a relation or set of relations. It is also used to eliminate undesirable characteristics like Insertion, Update, and Deletion Anomalies.

## Reasons for Normalization
The main objective of database normalization is to eliminate redundant data, minimize data modification errors, and simplify the query process. Ultimately, normalization goes beyond simply standardizing data, and can even improve workflow, increase security, and lessen costs
In normalization, the data is divided into several tables linked together with relationships.

## Types of Normalization
First Normal Form (1NF)<br>
Second Normal Form (2NF)<br>
Third Normal Form (3NF)<br>
Boyce-Codd Normal Form (BCNF)<br>
Fourth Normal Form (4NF)<br>

## First Normal Form (1NF)
In the 1NF stage, each column in a table is unique, with no repetition of groups of data. Here, each entry (or tuple) has a unique identifier known as a primary key.
For a table to be in the first normal form, it must meet the following criteria:
a single cell must not hold more than one value (atomicity)
there must be a primary key for identification
no duplicated rows or columns
each column must have only one value for each row in the table

#### Example
before first normal form <br>
<img src="/images/before 1nf.JPG" alt=" before 1nf"/><br>
<img src="/images/inf before table.JPG" alt="before 1nf table "/><br>
after first normal form <br>
<img src="/images/borrowers inf.JPG" alt="borrowers 1nf table"/> <br>
<img src="/images/borrowers sinf.JPG" alt="borrowers inf syntax"/><br>
<img src="/images/books inf.JPG" alt="books inf"/> <br>
<img src="/images/books table inf.JPG" alt="books inf table"/> <br>

## Second Normal Form(2NF)
2NF builds on 1NF by requiring that each non-primary key column in a table is fully functionally dependent on the primary key. This means that a table should not have partial dependencies, where a non-primary key column depends on only part of the primary key.

A table is said to be in 2NF if it meets the following criteria:

It’s already in 1NF<br>
Has no partial dependency. That is, all non-key attributes are fully dependent on a primary key.
#### Example
before second normal form <br>
<img src="/images/2nf ss.JPG" alt=" before 2nf"/><br>
<img src="/images/2nf table.JPG" alt="before 2nf table "/><br>
after second normal form <br>
<img src="/images/2nf borrower s.JPG" alt="borrowers 2nf syntax"/> <br>
<img src="/images/borrower table.JPG" alt="borrowers 2nf table"/><br>
<img src="/images/2nf book s.JPG" alt="books 2nf"/> <br>
<img src="/images/book table 2nf.JPG" alt="books 2nf table"/> <br>


## Third Normal Form (3NF)
3NF builds on 2NF by requiring that each non-primary key column in a table is not transitively dependent on the primary key.
3NF is used to reduce the data duplication. It is also used to achieve the data integrity.A relation is in third normal form if it holds atleast one of the following conditions for every non-trivial function dependency X → Y.

X is a super key.<br>
Y is a prime attribute, i.e., each element of Y is part of some candidate key.
#### Example

before third normal form <br>
<img src="/images/3nf s.JPG" alt=" before 3nf"/><br>
<img src="/images/3nf table.JPG" alt="before 3nf table "/><br>
after third normal form <br>
<img src="/images/students 3nf.JPG" alt="students syntax 3nf"/><br>
<img src="/images/student table 3nf.JPG" alt="student table 3nf"/> <br>
<img src="/images/address 3nf.JPG" alt="address syntax 3nf"/> <br>
<img src="/images/address table 3nf.JPG" alt="address table 3nf "/> <br>


## Boyce-Codd Normal Form (BCNF)
A stricter form of 3NF that applies to tables with more than one candidate key.Guarantees the validity of data dependencies. The dependencies of any attributes on non-key attributes are removed under the third level of normalization

#### Example

before Boyce-Codd Normal Form  <br>
<img src="/images/3nf s.JPG" alt=" before bcnf"/><br>
<img src="/images/3nf table.JPG" alt="before bcnf table "/><br>

after Boyce-Codd Normal Form <br>
<img src="/images/studentbcnf.JPG" alt="students syntax bcnf"/><br>
<img src="/images/student 3nd t.JPG" alt="student table bcnf"/> <br>
<img src="/images/addressbcnf.JPG" alt="address syntax bcnf"/> <br>
<img src="/images/address 3nf t.JPG" alt="address table bcnf "/> <br>

<img src="/images/sa bcnf table.JPG" alt=" student address syntax bcnf"/> <br>
<img src="/images/sa bcnf.JPG" alt="student address table bcnf "/> <br>

## Fourth Normal Form (4NF)
4NF builds on BCNF by requiring that a table should not have multi-valued dependencies. A multi-valued dependency occurs when a non-primary key column depends on a combination of other non-primary key columns.<br>It collapses the dependencies into single vs. multi-valued and eliminates the root of any data redundancy concerned with the multi-valued one.

#### Example

## ACID PROPERTIES
ACID properties provide a framework for ensuring data consistency, integrity, and reliability in DBMS. They ensure that transactions are executed in a reliable and consistent manner, even in the presence of system failures, network issues, or other problems. These properties make DBMS a reliable and efficient tool for managing data in modern organizations.<br>They include
Atomicity <br>Consistency<br> Isolation <br>Durability

## Atomicity 

The entire transaction takes place at once or doesn’t happen at all.Transactions do not occur partially. Each transaction is considered as one unit and either runs to completion or is not executed at all. It involves the following two operations.<br>
 Abort => If a transaction aborts, changes made to the database are not visible.<br>
Commit => If a transaction commits, changes made are visible.

#### Example
Transferring money from one bank account involves multiple steps:

Debit amount X from Account A ,
Credit amount X to Account B
As per atomicity, either all debit and credit operations succeed or they all fail. If the debit succeeds, but the credit fails for any reason, the entire transaction is rolled back. Atomicity ensures there are no partial or incomplete transactions

## Consistency
Integrity constraints must be maintained so that the database is consistent before and after the transaction,which means if a change in the database is made, it should remain preserved always. It refers to the correctness of a database.
#### Example
a transaction crediting 5000 to a bank account with a current balance of 3000 is invalid if the account has an overdraft limit of 1000. The transaction violates consistency by exceeding the permissible account limit. Hence, it is blocked and aborted.

## Isolation
This property ensures that multiple transactions can occur concurrently without leading to the inconsistency of the database state. Transactions occur independently without interference.
#### Example
For instance, if Transaction T1 updates a row, Transaction T2 must wait until T1 commits or rolls back. Isolation prevents T2 from reading unreliable data updated by T1 but not committed yet.
Isolation avoids concurrency issues like:
Dirty reads ,
Lost updates ,
Non-repeatable reads 
## Durability
This property ensures that once the transaction has completed execution, the updates and modifications to the database are stored in and written to disk and they persist even if a system failure occurs. These updates now become permanent and are stored in non-volatile memory.

#### Example
if a transaction updates a customer's address, durability ensures the updated address is not lost due to a hard disk failure or power outage. The change will persist with the help of storage devices, backups, and logs.

Durability ensures that transactions, once committed, will survive permanently

