<h1>JOINS</h1>
<p>A JOIN clause is used to combine rows from two or more tables, based on a related column between them.</p>
<h3>Types of joins</h3>
<p>Inner Join <br>Left Join <br>Right Join <br>Full Join</p>
<h2>Inner Join</h2>
<p>An INNER JOIN is the default join which retrieves the intersection of two tables. It compares each row of the first table with each row of the second table. If the pairs of these rows satisfy the join-predicate, they are joined together.</p>
<h5>Exampe</h5>

<h2>Left Join</h2>

<p>LEFT JOIN returns all the rows of the table on the left side of the join and matches rows for the table on the right side of the join. For the rows for which there is no matching row on the right side, the result-set will contain null</p>
<h5>Example</h5>

<h2>Right Join </h2>
<p>returns all rows from the right table, even if there are no matches in the left table.</p>
<h5>Example</h5>
<h2>Full Join</h2>
<p> returns rows when there is a match in one of the tables.Creates the result-set by combining results of both LEFT JOIN and RIGHT JOIN. The result-set will contain all the rows from both tables</p>
<h5>Example</h5>

<h1>NORMALIZATION</h1>
<p>Normalization is the process of organizing the data in the database.</p>
<p>Normalization is used to minimize the redundancy from a relation or set of relations. It is also used to eliminate undesirable characteristics like Insertion, Update, and Deletion Anomalies.</p>

<h3>Reasons for Normalization</h3>
<p>The main objective of database normalization is to eliminate redundant data, minimize data modification errors, and simplify the query process. Ultimately, normalization goes beyond simply standardizing data, and can even improve workflow, increase security, and lessen costs</p>
<p>In normalization, the data is divided into several tables linked together with relationships.</p>

<h2>Types of Normalization</h3>
<p>First Normal Form (1NF)</p>
<p>Second Normal Form (2NF)</p>
<p>Third Normal Form (3NF)</p>
<p>Boyce-Codd Normal Form (BCNF)</p>
<p>Fourth Normal Form (4NF)</p>

<h3>First Normal Form (1NF)</h3>
<p>In the 1NF stage, each column in a table is unique, with no repetition of groups of data. Here, each entry (or tuple) has a unique identifier known as a primary key.</p>
<p>For a table to be in the first normal form, it must meet the following criteria:</p>
<p>a single cell must not hold more than one value (atomicity)</p>
<p>there must be a primary key for identification</p>
<p>no duplicated rows or columns</p>
<p>each column must have only one value for each row in the table</p>
<h5>Example</h5>


<h3>Second Normal Form(2NF)</h3>
<p>2NF builds on 1NF by requiring that each non-primary key column in a table is fully functionally dependent on the primary key. This means that a table should not have partial dependencies, where a non-primary key column depends on only part of the primary key.</p>

<p>A table is said to be in 2NF if it meets the following criteria:

It’s already in 1NF<br>
Has no partial dependency. That is, all non-key attributes are fully dependent on a primary key.</p>
<h5>Example</h5>

<h3>Third Normal Form (3NF)</h3>
<p>3NF builds on 2NF by requiring that each non-primary key column in a table is not transitively dependent on the primary key.</p>
<p>3NF is used to reduce the data duplication. It is also used to achieve the data integrity.A relation is in third normal form if it holds atleast one of the following conditions for every non-trivial function dependency X → Y.

X is a super key.<br>
Y is a prime attribute, i.e., each element of Y is part of some candidate key.</p>
<h5>Example</h5>

<h3>Boyce-Codd Normal Form (BCNF)</h3>
<p>A stricter form of 3NF that applies to tables with more than one candidate key.Guarantees the validity of data dependencies. The dependencies of any attributes on non-key attributes are removed under the third level of normalization</p>
<h5>Example</h5>

<h3>Fourth Normal Form (4NF)</h3>
<p>4NF builds on BCNF by requiring that a table should not have multi-valued dependencies. A multi-valued dependency occurs when a non-primary key column depends on a combination of other non-primary key columns.<br>It collapses the dependencies into single vs. multi-valued and eliminates the root of any data redundancy concerned with the multi-valued one.</p>
<h5>Example</h5>

<h1>ACID PROPERTIES</h1>
<p>ACID properties provide a framework for ensuring data consistency, integrity, and reliability in DBMS. They ensure that transactions are executed in a reliable and consistent manner, even in the presence of system failures, network issues, or other problems. These properties make DBMS a reliable and efficient tool for managing data in modern organizations.<br>They include</p>
<p>Atomicity <br>Consistency<br> Isolation <br>Durability</p>
<h2>Atomicity </h2>
<p>The entire transaction takes place at once or doesn’t happen at all.Transactions do not occur partially. Each transaction is considered as one unit and either runs to completion or is not executed at all. It involves the following two operations.<br>
 Abort => If a transaction aborts, changes made to the database are not visible.<br>
Commit => If a transaction commits, changes made are visible.</p>

<h2>Consistency</h2>
<p>Integrity constraints must be maintained so that the database is consistent before and after the transaction,which means if a change in the database is made, it should remain preserved always. It refers to the correctness of a database.</p>

<h2> Isolation</h2>
<p>This property ensures that multiple transactions can occur concurrently without leading to the inconsistency of the database state. Transactions occur independently without interference. </p>
<h2>Durability</h2>
<p>This property ensures that once the transaction has completed execution, the updates and modifications to the database are stored in and written to disk and they persist even if a system failure occurs. These updates now become permanent and are stored in non-volatile memory.</p>

