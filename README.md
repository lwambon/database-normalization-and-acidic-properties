<h1>Normalization</h1>
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