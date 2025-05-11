---


---

<h2 id="mastering-sql-advanced-techniques-and-best-practices-for-efficient-database-management">Mastering SQL: Advanced Techniques and Best Practices for Efficient Database Management</h2>
<ol>
<li>
<p><strong>Introduction to SQL</strong></p>
<ul>
<li>What SQL is, history, and basic database concepts.</li>
</ul>
</li>
<li>
<p><strong>Basic SQL Syntax and Queries</strong></p>
<ul>
<li>SELECT, WHERE, and basic querying.</li>
</ul>
</li>
<li>
<p><strong>Filtering and Sorting Data</strong></p>
<ul>
<li>Using operators, logical conditions, and ORDER BY.</li>
</ul>
</li>
<li>
<p><strong>Joining Tables</strong></p>
<ul>
<li>INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN.</li>
</ul>
</li>
<li>
<p><strong>Aggregating Data</strong></p>
<ul>
<li>COUNT, SUM, AVG, MAX, MIN, GROUP BY, HAVING.</li>
</ul>
</li>
<li>
<p><strong>Subqueries and Nested Queries</strong></p>
<ul>
<li>Writing and optimizing subqueries within SELECT, INSERT, UPDATE, DELETE.</li>
</ul>
</li>
<li>
<p><strong>Modifying Data</strong></p>
<ul>
<li>INSERT, UPDATE, DELETE statements and their use cases.</li>
</ul>
</li>
<li>
<p><strong>Database Constraints and Integrity</strong></p>
<ul>
<li>Primary keys, foreign keys, unique constraints, and not null constraints.</li>
</ul>
</li>
<li>
<p><strong>Advanced SQL Functions</strong></p>
<ul>
<li>CASE, COALESCE, CAST, and more complex expressions.</li>
</ul>
</li>
<li>
<p><strong>Database Design and Normalization</strong></p>
<ul>
<li>Concepts of database normalization (1NF, 2NF, 3NF) and designing efficient schemas.</li>
</ul>
</li>
</ol>
<h3 id="chapter-1-introduction-to-sql">Chapter 1: <strong>Introduction to SQL</strong></h3>
<p>This chapter provides the foundational understanding of SQL (Structured Query Language), its role in interacting with databases, and the essential concepts you’ll need to work with SQL effectively.</p>
<h4 id="what-is-sql">1. <strong>What is SQL?</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: SQL is a standardized language used for managing and manipulating relational databases. It allows users to perform various operations like querying, updating, inserting, and deleting data.</p>
</li>
<li>
<p><strong>Purpose</strong>: SQL helps in querying databases to retrieve information, managing database schemas, and performing administrative tasks like securing and maintaining data.</p>
</li>
</ul>
<h4 id="history-of-sql">2. <strong>History of SQL</strong></h4>
<ul>
<li>
<p><strong>Origins</strong>: SQL was developed by IBM in the early 1970s as part of the System R project. It was influenced by relational database theory proposed by Edgar F. Codd.</p>
</li>
<li>
<p><strong>Standardization</strong>: SQL became a standard in 1986 by the American National Standards Institute (ANSI) and later by the International Organization for Standardization (ISO).</p>
</li>
<li>
<p><strong>Evolution</strong>: Over time, SQL has evolved with new versions and implementations across various database management systems (DBMS) like MySQL, PostgreSQL, Oracle, SQL Server, and SQLite.</p>
</li>
</ul>
<h4 id="sql-and-databases">3. <strong>SQL and Databases</strong></h4>
<ul>
<li>
<p><strong>Relational Databases</strong>: SQL is primarily used for interacting with relational databases, which organize data into tables (relations) consisting of rows and columns.</p>
</li>
<li>
<p><strong>Database Management Systems (DBMS)</strong>: A DBMS is a software that interacts with databases. Examples include MySQL, PostgreSQL, Microsoft SQL Server, and Oracle Database. SQL is the query language these systems use to manipulate and access the data.</p>
</li>
</ul>
<h4 id="relational-database-concepts">4. <strong>Relational Database Concepts</strong></h4>
<ul>
<li>
<p><strong>Tables</strong>: Data in relational databases is stored in tables, each with a set of rows and columns.</p>
</li>
<li>
<p><strong>Rows</strong>: Each row represents a single record or data entry.</p>
</li>
<li>
<p><strong>Columns</strong>: Each column in a table represents an attribute or a field of the record.</p>
</li>
<li>
<p><strong>Schemas</strong>: A database schema defines the structure of the database, including the tables, relationships, and constraints.</p>
</li>
</ul>
<h4 id="basic-sql-operations">5. <strong>Basic SQL Operations</strong></h4>
<p>SQL operations are categorized into four major types:</p>
<ul>
<li>
<p><strong>DML (Data Manipulation Language)</strong>: Commands used to manipulate data within tables. Examples include:</p>
<ul>
<li>
<p><strong>SELECT</strong>: Retrieve data from one or more tables.</p>
</li>
<li>
<p><strong>INSERT</strong>: Add new records to a table.</p>
</li>
<li>
<p><strong>UPDATE</strong>: Modify existing records.</p>
</li>
<li>
<p><strong>DELETE</strong>: Remove records from a table.</p>
</li>
</ul>
</li>
<li>
<p><strong>DDL (Data Definition Language)</strong>: Commands used to define and manage database structures. Examples include:</p>
<ul>
<li>
<p><strong>CREATE</strong>: Create new tables, schemas, or databases.</p>
</li>
<li>
<p><strong>ALTER</strong>: Modify existing database objects.</p>
</li>
<li>
<p><strong>DROP</strong>: Delete database objects like tables or databases.</p>
</li>
</ul>
</li>
<li>
<p><strong>DCL (Data Control Language)</strong>: Commands used to manage access control and permissions. Examples include:</p>
<ul>
<li>
<p><strong>GRANT</strong>: Give users access to database resources.</p>
</li>
<li>
<p><strong>REVOKE</strong>: Remove access or permissions from users.</p>
</li>
</ul>
</li>
<li>
<p><strong>TCL (Transaction Control Language)</strong>: Commands that deal with transactions, ensuring data integrity. Examples include:</p>
<ul>
<li>
<p><strong>COMMIT</strong>: Save the changes made during a transaction.</p>
</li>
<li>
<p><strong>ROLLBACK</strong>: Undo changes made during a transaction.</p>
</li>
</ul>
</li>
</ul>
<h4 id="sql-queries">6. <strong>SQL Queries</strong></h4>
<ul>
<li>
<p><strong>Basic Query Structure</strong>: The most common SQL operation is querying data from a table using the <code>SELECT</code> statement. A basic query looks like this:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Clauses</strong>: SQL queries consist of different clauses such as:</p>
<ul>
<li>
<p><code>SELECT</code>: Specifies the columns to be returned.</p>
</li>
<li>
<p><code>FROM</code>: Specifies the table to retrieve data from.</p>
</li>
<li>
<p><code>WHERE</code>: Adds conditions to filter the data.</p>
</li>
<li>
<p><code>ORDER BY</code>: Sorts the result.</p>
</li>
</ul>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department <span class="token operator">=</span> <span class="token string">'HR'</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="sql-syntax-rules">7. <strong>SQL Syntax Rules</strong></h4>
<ul>
<li>
<p>SQL commands are case-insensitive (e.g., <code>select</code> is the same as <code>SELECT</code>).</p>
</li>
<li>
<p>Keywords like <code>SELECT</code>, <code>FROM</code>, and <code>WHERE</code> should be written in uppercase for readability (though lowercase works too).</p>
</li>
<li>
<p>Commands must end with a semicolon (<code>;</code>), especially when executing multiple commands.</p>
</li>
</ul>
<h4 id="common-sql-data-types">8. <strong>Common SQL Data Types</strong></h4>
<p>SQL supports various data types, including:</p>
<ul>
<li>
<p><strong>Numeric Types</strong>: <code>INT</code>, <code>DECIMAL</code>, <code>FLOAT</code>, etc.</p>
</li>
<li>
<p><strong>Text Types</strong>: <code>VARCHAR</code>, <code>CHAR</code>, <code>TEXT</code>.</p>
</li>
<li>
<p><strong>Date and Time Types</strong>: <code>DATE</code>, <code>TIME</code>, <code>DATETIME</code>.</p>
</li>
<li>
<p><strong>Boolean</strong>: <code>BOOLEAN</code>, representing true or false.</p>
</li>
</ul>
<h4 id="understanding-sql-statements">9. <strong>Understanding SQL Statements</strong></h4>
<ul>
<li>
<p><strong>Simple SELECT</strong>: Retrieve all data from a table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>SELECT with WHERE</strong>: Filter data using a condition.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department <span class="token operator">=</span> <span class="token string">'Sales'</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>SELECT with ORDER BY</strong>: Sort data by a column.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> last_name <span class="token keyword">ASC</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="practical-application-of-sql">10. <strong>Practical Application of SQL</strong></h4>
<ul>
<li>
<p><strong>Real-World Use Cases</strong>: SQL is widely used in business applications, web development, data analysis, and reporting. Understanding SQL allows you to extract meaningful insights from data, manage databases, and ensure data integrity.</p>
</li>
<li>
<p><strong>SQL and Reporting</strong>: SQL is essential in generating reports, such as sales data, inventory management, and customer insights, often used for decision-making in businesses.</p>
</li>
</ul>
<h3 id="summary">Summary:</h3>
<p>Chapter 1 introduces the core concepts of SQL, including its role in interacting with relational databases, the basics of SQL syntax, and the key operations you can perform using SQL. Understanding these basics is crucial before diving deeper into more advanced topics like joins, subqueries, and database design.</p>
<h3 id="chapter-2-basic-sql-syntax-and-queries">Chapter 2: <strong>Basic SQL Syntax and Queries</strong></h3>
<p>This chapter introduces the foundational elements of SQL syntax, focusing on the basic structure of SQL queries and the most common operations used to interact with relational databases.</p>
<h4 id="understanding-sql-syntax">1. <strong>Understanding SQL Syntax</strong></h4>
<ul>
<li>
<p>SQL statements have a standard structure, with commands, clauses, and expressions. While SQL syntax is not case-sensitive, it’s a common practice to write keywords in uppercase for clarity.</p>
</li>
<li>
<p>SQL queries are composed of one or more of the following components:</p>
<ul>
<li>
<p><strong>Clauses</strong>: Parts of the SQL query that define the operation.</p>
</li>
<li>
<p><strong>Expressions</strong>: Conditions or formulas used to define the data.</p>
</li>
<li>
<p><strong>Predicates</strong>: Conditions that filter rows, such as comparisons or logical operators.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example of basic syntax structure</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 
<span class="token keyword">FROM</span> table_name 
<span class="token keyword">WHERE</span> condition 
<span class="token keyword">ORDER</span> <span class="token keyword">BY</span> <span class="token keyword">column</span><span class="token punctuation">;</span>
</code></pre>
<h4 id="the-select-statement">2. <strong>The SELECT Statement</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: The <code>SELECT</code> statement is used to retrieve data from one or more tables in a database.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>: To select all data from a table:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><code>*</code> is a wildcard that selects all columns from the specified table.</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li>
<p><strong>Selecting Specific Columns</strong>: Instead of <code>*</code>, you can specify which columns you want to retrieve.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="the-from-clause">3. <strong>The FROM Clause</strong></h4>
<ul>
<li>
<p>The <code>FROM</code> clause specifies the table from which to retrieve data.</p>
</li>
<li>
<p><strong>Example</strong>: To query from the “employees” table:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="the-where-clause">4. <strong>The WHERE Clause</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: The <code>WHERE</code> clause filters the rows based on specific conditions. It allows you to retrieve only the data that meets certain criteria.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>: The <code>WHERE</code> clause is used to specify the condition for selecting data:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name <span class="token keyword">WHERE</span> condition<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<p><strong>Common conditions</strong>:</p>
<ul>
<li>
<p><strong>Comparison Operators</strong>: <code>=</code>, <code>&gt;</code>, <code>&lt;</code>, <code>&gt;=</code>, <code>&lt;=</code>, <code>&lt;&gt;</code> (not equal).</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token number">50000</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Logical Operators</strong>: <code>AND</code>, <code>OR</code>, <code>NOT</code> are used to combine conditions.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token number">50000</span> <span class="token operator">AND</span> department <span class="token operator">=</span> <span class="token string">'HR'</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>BETWEEN</strong>: Used to filter data within a range.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">BETWEEN</span> <span class="token number">40000</span> <span class="token operator">AND</span> <span class="token number">60000</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>IN</strong>: Allows you to specify multiple values in the <code>WHERE</code> clause.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department <span class="token operator">IN</span> <span class="token punctuation">(</span><span class="token string">'HR'</span><span class="token punctuation">,</span> <span class="token string">'Sales'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>LIKE</strong>: Used for pattern matching with wildcards (<code>%</code> for any sequence of characters, <code>_</code> for a single character).</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> last_name <span class="token operator">LIKE</span> <span class="token string">'S%'</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>IS NULL</strong>: Checks for NULL values.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> middle_name <span class="token operator">IS</span> <span class="token boolean">NULL</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="the-order-by-clause">5. <strong>The ORDER BY Clause</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: The <code>ORDER BY</code> clause sorts the results of a query in either ascending (default) or descending order.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> column1 <span class="token punctuation">[</span><span class="token keyword">ASC</span><span class="token operator">|</span><span class="token keyword">DESC</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Sorting Order</strong>:</p>
<ul>
<li>
<p><code>ASC</code>: Ascending order (default).</p>
</li>
<li>
<p><code>DESC</code>: Descending order.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>: Sorting employees by salary in descending order:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span><span class="token punctuation">;</span>
</code></pre>
<h4 id="the-limit-clause">6. <strong>The LIMIT Clause</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: The <code>LIMIT</code> clause restricts the number of rows returned by a query.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name <span class="token keyword">LIMIT</span> number_of_rows<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get only the top 5 employees with the highest salaries:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span> <span class="token keyword">LIMIT</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="using-distinct">7. <strong>Using DISTINCT</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: The <code>DISTINCT</code> keyword removes duplicate rows from the result set.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">DISTINCT</span> column_name <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve unique job titles from the employees table:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">DISTINCT</span> job_title <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="combining-multiple-queries-with-union">8. <strong>Combining Multiple Queries with UNION</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: The <code>UNION</code> operator is used to combine the results of two or more <code>SELECT</code> queries. All queries combined using <code>UNION</code> must have the same number of columns with compatible data types.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table1
<span class="token keyword">UNION</span>
<span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table2<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Combine employee names from two different tables (e.g., full-time and part-time employees):</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> full_time_employees
<span class="token keyword">UNION</span>
<span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> part_time_employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="using-aliases-for-columns-and-tables">9. <strong>Using Aliases for Columns and Tables</strong></h4>
<ul>
<li>
<p><strong>Purpose</strong>: Aliases provide a temporary name for tables or columns in a query, making the result set easier to understand or more readable.</p>
</li>
<li>
<p><strong>Column Alias</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name <span class="token keyword">AS</span> <span class="token string">'Employee First Name'</span><span class="token punctuation">,</span> last_name <span class="token keyword">AS</span> <span class="token string">'Employee Last Name'</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Table Alias</strong>: Alias for tables is useful when joining multiple tables.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">e</span><span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> <span class="token number">e</span><span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees <span class="token keyword">AS</span> <span class="token number">e</span>
<span class="token keyword">JOIN</span> departments <span class="token keyword">AS</span> <span class="token number">d</span> <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="basic-error-handling-and-debugging">10. <strong>Basic Error Handling and Debugging</strong></h4>
<ul>
<li>
<p><strong>Syntax Errors</strong>: If you write an incorrect SQL statement (such as a misspelled keyword or missing clause), the database system will return an error.</p>
</li>
<li>
<p><strong>Logical Errors</strong>: Logical errors, such as incorrect filtering or sorting, might not trigger errors but can return unexpected results. It’s important to carefully check query logic when results don’t match expectations.</p>
</li>
<li>
<p><strong>Debugging Tips</strong>:</p>
<ul>
<li>
<p>Check the SQL syntax.</p>
</li>
<li>
<p>Verify column and table names are correct.</p>
</li>
<li>
<p>Use comments (<code>--</code> for single-line and <code>/* */</code> for multi-line comments) to isolate parts of your query for testing.</p>
</li>
</ul>
</li>
</ul>
<h3 id="summary-1">Summary:</h3>
<p>Chapter 2 introduces you to the basic SQL syntax for querying data. You learn how to construct simple queries using <code>SELECT</code>, <code>FROM</code>, <code>WHERE</code>, <code>ORDER BY</code>, and <code>LIMIT</code> clauses. You also learn how to manipulate results with <code>DISTINCT</code>, use logical operators, and combine queries with <code>UNION</code>. This foundational knowledge is essential for building more advanced queries and interacting effectively with databases.</p>
<h3 id="chapter-3-filtering-and-sorting-data">Chapter 3: <strong>Filtering and Sorting Data</strong></h3>
<p>This chapter delves deeper into how to filter and sort data in SQL queries, which is essential for retrieving specific information from large datasets. You’ll learn how to apply various conditions to select only the relevant data, and how to order the results in a meaningful way.</p>
<h4 id="the-where-clause-–-filtering-data">1. <strong>The WHERE Clause – Filtering Data</strong></h4>
<p>The <code>WHERE</code> clause is the most common way to filter data. It helps you define conditions that rows must meet to be included in the result set. The condition in the <code>WHERE</code> clause can be a comparison, a logical operator, or more complex expressions.</p>
<ul>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name <span class="token keyword">WHERE</span> condition<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Conditions</strong>:</p>
<ul>
<li>
<p><strong>Comparison Operators</strong>: These are used to compare values.</p>
<ul>
<li>
<p><code>=</code>: Equal to</p>
</li>
<li>
<p><code>&gt;</code>: Greater than</p>
</li>
<li>
<p><code>&lt;</code>: Less than</p>
</li>
<li>
<p><code>&gt;=</code>: Greater than or equal to</p>
</li>
<li>
<p><code>&lt;=</code>: Less than or equal to</p>
</li>
<li>
<p><code>&lt;&gt;</code> or <code>!=</code>: Not equal to</p>
</li>
</ul>
<p><strong>Example</strong>: Get employees whose salary is greater than 50,000.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token number">50000</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Logical Operators</strong>: These allow combining multiple conditions.</p>
<ul>
<li>
<p><code>AND</code>: Ensures all conditions are true.</p>
</li>
<li>
<p><code>OR</code>: Ensures at least one condition is true.</p>
</li>
<li>
<p><code>NOT</code>: Reverses the condition (e.g., <code>NOT NULL</code>, <code>NOT IN</code>).</p>
</li>
</ul>
<p><strong>Example</strong>: Get employees with a salary above 50,000 and who work in the ‘Sales’ department.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary 
<span class="token keyword">FROM</span> employees 
<span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token number">50000</span> <span class="token operator">AND</span> department <span class="token operator">=</span> <span class="token string">'Sales'</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>BETWEEN</strong>: Used to filter data within a specific range. It is inclusive of the boundary values.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">BETWEEN</span> <span class="token number">40000</span> <span class="token operator">AND</span> <span class="token number">60000</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>IN</strong>: Specifies a list of possible values. It’s an easier way to test if a value exists in a given list of values.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department <span class="token operator">IN</span> <span class="token punctuation">(</span><span class="token string">'HR'</span><span class="token punctuation">,</span> <span class="token string">'Sales'</span><span class="token punctuation">,</span> <span class="token string">'IT'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>LIKE</strong>: Used for pattern matching, typically with wildcards. It’s useful for partial matches.</p>
<ul>
<li>
<p><code>%</code>: Matches zero or more characters.</p>
</li>
<li>
<p><code>_</code>: Matches a single character.</p>
</li>
</ul>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> last_name <span class="token operator">LIKE</span> <span class="token string">'S%'</span><span class="token punctuation">;</span>  <span class="token comment">-- Last names starting with S</span>
</code></pre>
</li>
<li>
<p><strong>IS NULL / IS NOT NULL</strong>: Used to check for NULL values.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> middle_name <span class="token operator">IS</span> <span class="token boolean">NULL</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<h4 id="advanced-filtering-techniques">2. <strong>Advanced Filtering Techniques</strong></h4>
<p>In this section, you’ll learn more complex filtering methods to refine data retrieval.</p>
<ul>
<li>
<p><strong>Combining Conditions with Parentheses</strong>: Parentheses help organize complex conditions and ensure correct evaluation order.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary 
<span class="token keyword">FROM</span> employees 
<span class="token keyword">WHERE</span> <span class="token punctuation">(</span>salary <span class="token operator">&gt;</span> <span class="token number">50000</span> <span class="token operator">OR</span> department <span class="token operator">=</span> <span class="token string">'HR'</span><span class="token punctuation">)</span> <span class="token operator">AND</span> hire_date <span class="token operator">&gt;</span> <span class="token string">'2020-01-01'</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Using <code>EXISTS</code></strong>: The <code>EXISTS</code> operator is used in correlated subqueries to check if the subquery returns any rows.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name 
<span class="token keyword">FROM</span> employees <span class="token number">e</span> 
<span class="token keyword">WHERE</span> <span class="token keyword">EXISTS</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> departments <span class="token number">d</span> <span class="token keyword">WHERE</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Using <code>NULL</code> with Comparison Operators</strong>: Remember, comparing with <code>NULL</code> directly using <code>=</code> or <code>&lt;&gt;</code> doesn’t work. Instead, use <code>IS NULL</code> or <code>IS NOT NULL</code>.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> commission_pct <span class="token operator">IS</span> <span class="token operator">NOT</span> <span class="token boolean">NULL</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="sorting-data-with-the-order-by-clause">3. <strong>Sorting Data with the ORDER BY Clause</strong></h4>
<p>Sorting is an essential part of data retrieval, especially when you’re working with large datasets. The <code>ORDER BY</code> clause helps to organize the result set based on one or more columns.</p>
<ul>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> column1 <span class="token punctuation">[</span><span class="token keyword">ASC</span><span class="token operator">|</span><span class="token keyword">DESC</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>
<p><strong>ASC (Ascending Order)</strong>: This is the default. It sorts the result from the smallest to largest (or alphabetically from A to Z).</p>
</li>
<li>
<p><strong>DESC (Descending Order)</strong>: Sorts the result from largest to smallest (or alphabetically from Z to A).</p>
</li>
</ul>
</li>
</ul>
<p><strong>Examples</strong>:</p>
<ul>
<li>
<p>Sort employees by their last name in ascending order:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> last_name <span class="token keyword">ASC</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>Sort employees by salary in descending order:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p>Sort by multiple columns:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> department<span class="token punctuation">,</span> salary 
<span class="token keyword">FROM</span> employees 
<span class="token keyword">ORDER</span> <span class="token keyword">BY</span> department <span class="token keyword">ASC</span><span class="token punctuation">,</span> salary <span class="token keyword">DESC</span><span class="token punctuation">;</span>
</code></pre>
<p>In this case, employees are first sorted by department in ascending order. Within each department, employees are sorted by salary in descending order.</p>
</li>
</ul>
<h4 id="limiting-and-paging-results">4. <strong>Limiting and Paging Results</strong></h4>
<p>When dealing with large datasets, it’s often useful to limit the number of rows returned by a query. This is where the <code>LIMIT</code> clause (or <code>TOP</code> in some databases like SQL Server) comes in handy.</p>
<ul>
<li>
<p><strong>Basic Syntax for LIMIT</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">FROM</span> table_name <span class="token keyword">LIMIT</span> number_of_rows<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve the top 5 employees with the highest salaries.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span> <span class="token keyword">LIMIT</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>OFFSET and LIMIT</strong>: To implement paging, you can use <code>LIMIT</code> with <code>OFFSET</code>. The <code>OFFSET</code> specifies how many rows to skip.</p>
<ul>
<li><strong>Example</strong>: Retrieve rows 11-20 (skip 10 rows, and then return the next 10 rows).</li>
</ul>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> employees <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> last_name <span class="token keyword">ASC</span> <span class="token keyword">LIMIT</span> <span class="token number">10</span> <span class="token keyword">OFFSET</span> <span class="token number">10</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="sorting-and-filtering-with-aggregate-functions">5. <strong>Sorting and Filtering with Aggregate Functions</strong></h4>
<ul>
<li>
<p><strong>Combining <code>GROUP BY</code> with <code>HAVING</code></strong>: When dealing with aggregate functions (e.g., <code>COUNT</code>, <code>AVG</code>, <code>SUM</code>), you often need to group data by certain columns. The <code>GROUP BY</code> clause is used to group the result set by one or more columns, and the <code>HAVING</code> clause is used to filter groups based on a condition, similar to how the <code>WHERE</code> clause works for individual rows.</p>
</li>
<li>
<p><strong>Example</strong>: Find departments with an average salary greater than 50,000.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department<span class="token punctuation">,</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> 
<span class="token keyword">FROM</span> employees 
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department 
<span class="token keyword">HAVING</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token operator">&gt;</span> <span class="token number">50000</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="using-window-functions-for-sorting-and-filtering">6. <strong>Using Window Functions for Sorting and Filtering</strong></h4>
<p>Window functions allow you to perform calculations across a set of table rows that are somehow related to the current row. This can be helpful for sorting and filtering based on complex conditions without collapsing the rows into aggregated results.</p>
<ul>
<li>
<p><strong>ROW_NUMBER()</strong>: Assigns a unique number to each row within a partition of a result set.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> 
       ROW_NUMBER<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> row_num
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<p>This query assigns a ranking number based on salary in descending order.</p>
</li>
</ul>
<h4 id="using-complex-expressions">7. <strong>Using Complex Expressions</strong></h4>
<p>SQL allows you to combine values and functions to filter and sort data in more advanced ways.</p>
<ul>
<li><strong>CASE Statements</strong>: Similar to an <code>if</code> or <code>switch</code> statement in programming, a <code>CASE</code> expression allows you to return a value based on conditions.</li>
</ul>
<p><strong>Example</strong>: Classify employees based on their salary ranges.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> 
       <span class="token keyword">CASE</span> 
         <span class="token keyword">WHEN</span> salary <span class="token operator">&lt;</span> <span class="token number">30000</span> <span class="token keyword">THEN</span> <span class="token string">'Low'</span>
         <span class="token keyword">WHEN</span> salary <span class="token operator">BETWEEN</span> <span class="token number">30000</span> <span class="token operator">AND</span> <span class="token number">70000</span> <span class="token keyword">THEN</span> <span class="token string">'Medium'</span>
         <span class="token keyword">ELSE</span> <span class="token string">'High'</span>
       <span class="token keyword">END</span> <span class="token keyword">AS</span> salary_range
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<h3 id="summary-2">Summary:</h3>
<p>Chapter 3 expands your knowledge of filtering and sorting data in SQL. You now understand how to use various comparison and logical operators in the <code>WHERE</code> clause, how to organize results with the <code>ORDER BY</code> clause, and how to limit or page through results. You also learned how to filter data based on aggregate functions using <code>GROUP BY</code> and <code>HAVING</code>, and how window functions can provide additional power for sorting and filtering complex datasets. These skills are essential for narrowing down and organizing data in a meaningful way.</p>
<h3 id="chapter-4-joining-tables">Chapter 4: <strong>Joining Tables</strong></h3>
<p>This chapter explores <strong>SQL joins</strong>, which allow you to combine data from two or more tables based on a related column. Joins are crucial when working with normalized databases, where data is split across multiple tables to reduce redundancy. Understanding how to use joins will help you extract useful insights from complex datasets.</p>
<h4 id="what-is-a-join">1. <strong>What is a Join?</strong></h4>
<p>A <strong>join</strong> in SQL is a way to combine rows from two or more tables based on a related column between them. Each table contains different pieces of related data, and joining them together creates a more complete dataset. The most common reason for using joins is to retrieve data from multiple tables simultaneously.</p>
<p>There are several types of joins:</p>
<ul>
<li>
<p><strong>Inner Join</strong></p>
</li>
<li>
<p><strong>Left Join (or Left Outer Join)</strong></p>
</li>
<li>
<p><strong>Right Join (or Right Outer Join)</strong></p>
</li>
<li>
<p><strong>Full Outer Join</strong></p>
</li>
<li>
<p><strong>Cross Join</strong></p>
</li>
<li>
<p><strong>Self Join</strong></p>
</li>
</ul>
<h4 id="inner-join">2. <strong>INNER JOIN</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>INNER JOIN</code> returns only the rows where there is a match in both tables. If there is no match, those rows are excluded from the result set.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">columns</span>
<span class="token keyword">FROM</span> table1
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> table2
<span class="token keyword">ON</span> table1<span class="token punctuation">.</span><span class="token keyword">column</span> <span class="token operator">=</span> table2<span class="token punctuation">.</span><span class="token keyword">column</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve employees with their department names from the <code>employees</code> and <code>departments</code> tables.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> employees<span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> employees<span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> departments<span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> departments <span class="token keyword">ON</span> employees<span class="token punctuation">.</span>department_id <span class="token operator">=</span> departments<span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
<p>In this example, only employees who belong to a department will be returned. If an employee doesn’t belong to any department, they are excluded.</p>
</li>
</ul>
<h4 id="left-join-or-left-outer-join">3. <strong>LEFT JOIN (or LEFT OUTER JOIN)</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>LEFT JOIN</code> (also known as <code>LEFT OUTER JOIN</code>) returns all rows from the left table (table1), and the matched rows from the right table (table2). If there is no match, the result is <code>NULL</code> on the side of the right table.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">columns</span>
<span class="token keyword">FROM</span> table1
<span class="token keyword">LEFT</span> <span class="token keyword">JOIN</span> table2
<span class="token keyword">ON</span> table1<span class="token punctuation">.</span><span class="token keyword">column</span> <span class="token operator">=</span> table2<span class="token punctuation">.</span><span class="token keyword">column</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve all employees, even if they don’t belong to a department.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> employees<span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> employees<span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> departments<span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">LEFT</span> <span class="token keyword">JOIN</span> departments <span class="token keyword">ON</span> employees<span class="token punctuation">.</span>department_id <span class="token operator">=</span> departments<span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
<p>This query returns all employees, and for those without a department, the <code>department_name</code> will be <code>NULL</code>.</p>
</li>
</ul>
<h4 id="right-join-or-right-outer-join">4. <strong>RIGHT JOIN (or RIGHT OUTER JOIN)</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>RIGHT JOIN</code> (also known as <code>RIGHT OUTER JOIN</code>) is the opposite of the <code>LEFT JOIN</code>. It returns all rows from the right table (table2) and the matched rows from the left table (table1). If there is no match, the result is <code>NULL</code> on the left side.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">columns</span>
<span class="token keyword">FROM</span> table1
<span class="token keyword">RIGHT</span> <span class="token keyword">JOIN</span> table2
<span class="token keyword">ON</span> table1<span class="token punctuation">.</span><span class="token keyword">column</span> <span class="token operator">=</span> table2<span class="token punctuation">.</span><span class="token keyword">column</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve all departments, even if there are no employees in those departments.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> employees<span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> employees<span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> departments<span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">RIGHT</span> <span class="token keyword">JOIN</span> departments <span class="token keyword">ON</span> employees<span class="token punctuation">.</span>department_id <span class="token operator">=</span> departments<span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
<p>This query returns all departments, and for departments with no employees, the <code>first_name</code> and <code>last_name</code> will be <code>NULL</code>.</p>
</li>
</ul>
<h4 id="full-outer-join">5. <strong>FULL OUTER JOIN</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>FULL OUTER JOIN</code> returns all rows when there is a match in either the left or the right table. If there is no match, <code>NULL</code> is returned for missing values on either side.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">columns</span>
<span class="token keyword">FROM</span> table1
<span class="token keyword">FULL</span> <span class="token keyword">OUTER</span> <span class="token keyword">JOIN</span> table2
<span class="token keyword">ON</span> table1<span class="token punctuation">.</span><span class="token keyword">column</span> <span class="token operator">=</span> table2<span class="token punctuation">.</span><span class="token keyword">column</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve all employees and all departments, even if there’s no match between the two.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> employees<span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> employees<span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> departments<span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">FULL</span> <span class="token keyword">OUTER</span> <span class="token keyword">JOIN</span> departments <span class="token keyword">ON</span> employees<span class="token punctuation">.</span>department_id <span class="token operator">=</span> departments<span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
<p>This query returns all employees and all departments. For employees without a department or departments without employees, the non-matching fields will be <code>NULL</code>.</p>
</li>
</ul>
<h4 id="cross-join">6. <strong>CROSS JOIN</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>CROSS JOIN</code> returns the Cartesian product of two tables. This means it will return all possible combinations of rows from the first table with all rows from the second table. Be careful when using this join, as it can produce a large number of results if the tables involved have many rows.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">columns</span>
<span class="token keyword">FROM</span> table1
<span class="token keyword">CROSS</span> <span class="token keyword">JOIN</span> table2<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get all possible pairs of employees and departments.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> employees<span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> departments<span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">CROSS</span> <span class="token keyword">JOIN</span> departments<span class="token punctuation">;</span>
</code></pre>
<p>If there are 10 employees and 5 departments, this query will return 50 rows (10 x 5 = 50 combinations).</p>
</li>
</ul>
<h4 id="self-join">7. <strong>SELF JOIN</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: A self join is a regular join, but the table is joined with itself. You can use a self join to compare rows within the same table.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">a</span><span class="token punctuation">.</span>column1<span class="token punctuation">,</span> <span class="token number">b</span><span class="token punctuation">.</span>column2
<span class="token keyword">FROM</span> <span class="token keyword">table</span> <span class="token number">a</span>
<span class="token keyword">JOIN</span> <span class="token keyword">table</span> <span class="token number">b</span>
<span class="token keyword">ON</span> <span class="token number">a</span><span class="token punctuation">.</span><span class="token keyword">column</span> <span class="token operator">=</span> <span class="token number">b</span><span class="token punctuation">.</span><span class="token keyword">column</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Retrieve employees who report to other employees (assuming we have a <code>manager_id</code> column).</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">e1</span><span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Employee<span class="token punctuation">,</span> <span class="token number">e2</span><span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Manager
<span class="token keyword">FROM</span> employees <span class="token number">e1</span>
<span class="token keyword">LEFT</span> <span class="token keyword">JOIN</span> employees <span class="token number">e2</span> <span class="token keyword">ON</span> <span class="token number">e1</span><span class="token punctuation">.</span>manager_id <span class="token operator">=</span> <span class="token number">e2</span><span class="token punctuation">.</span>employee_id<span class="token punctuation">;</span>
</code></pre>
<p>In this query, <code>e1</code> represents employees, and <code>e2</code> represents their managers. The <code>LEFT JOIN</code> ensures we still get employees even if they don’t have a manager (i.e., their <code>manager_id</code> is <code>NULL</code>).</p>
</li>
</ul>
<h4 id="join-conditions-and-multiple-joins">8. <strong>JOIN Conditions and Multiple Joins</strong></h4>
<ul>
<li>
<p><strong>Multiple Joins</strong>: You can join more than two tables in a single query by chaining joins.</p>
<p><strong>Example</strong>: Retrieve employee names, their department names, and their manager names.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">e</span><span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Employee<span class="token punctuation">,</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name<span class="token punctuation">,</span> m<span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Manager
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> departments <span class="token number">d</span> <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id
<span class="token keyword">LEFT</span> <span class="token keyword">JOIN</span> employees m <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>manager_id <span class="token operator">=</span> m<span class="token punctuation">.</span>employee_id<span class="token punctuation">;</span>
</code></pre>
<p>This query joins the <code>employees</code> table twice—once for the employees themselves and once for their managers. The <code>LEFT JOIN</code> ensures employees with no managers are included.</p>
</li>
<li>
<p><strong>Join Conditions</strong>: You can join tables based on any condition, not just equality. For example, you can use inequality conditions (<code>&gt;</code>, <code>&lt;</code>, <code>&gt;=</code>, etc.) or combinations of multiple conditions.</p>
<p><strong>Example</strong>: Retrieve all employees who started after their manager.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">e</span><span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> <span class="token number">e</span><span class="token punctuation">.</span>hire_date<span class="token punctuation">,</span> m<span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Manager<span class="token punctuation">,</span> m<span class="token punctuation">.</span>hire_date <span class="token keyword">AS</span> Manager_Hire_Date
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> employees m <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>manager_id <span class="token operator">=</span> m<span class="token punctuation">.</span>employee_id
<span class="token keyword">WHERE</span> <span class="token number">e</span><span class="token punctuation">.</span>hire_date <span class="token operator">&gt;</span> m<span class="token punctuation">.</span>hire_date<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="using-aliases-in-joins">9. <strong>Using Aliases in Joins</strong></h4>
<ul>
<li>
<p><strong>Table Aliases</strong>: Using aliases for tables (like <code>e</code> for employees) makes your SQL queries shorter and easier to read.</p>
</li>
<li>
<p><strong>Column Aliases</strong>: Similarly, using aliases for columns (e.g., <code>e.first_name AS Employee_Name</code>) improves readability.</p>
</li>
</ul>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">e</span><span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Employee_Name<span class="token punctuation">,</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name <span class="token keyword">AS</span> Department<span class="token punctuation">,</span> m<span class="token punctuation">.</span>first_name <span class="token keyword">AS</span> Manager_Name
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> departments <span class="token number">d</span> <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id
<span class="token keyword">LEFT</span> <span class="token keyword">JOIN</span> employees m <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>manager_id <span class="token operator">=</span> m<span class="token punctuation">.</span>employee_id<span class="token punctuation">;</span>
</code></pre>
<h4 id="performance-considerations-with-joins">10. <strong>Performance Considerations with Joins</strong></h4>
<ul>
<li>
<p><strong>Indexes</strong>: To improve the performance of joins, ensure the columns used in the <code>ON</code> condition are indexed. For example, indexing <code>employee_id</code> in both tables will speed up the <code>INNER JOIN</code>.</p>
</li>
<li>
<p><strong>Reducing Join Size</strong>: Be mindful of the number of rows involved in the join. For large tables, a poorly designed join can significantly impact performance. Try to minimize unnecessary rows by using appropriate filters (<code>WHERE</code> clause) before performing joins.</p>
</li>
<li>
<p><strong>Optimizing with <code>EXPLAIN</code></strong>: Use the <code>EXPLAIN</code> keyword to analyze the execution plan of a query and optimize joins.</p>
</li>
</ul>
<h3 id="summary-3">Summary:</h3>
<p>Chapter 4 provides an in-depth exploration of SQL joins. You’ve learned how to use different types of joins—<code>INNER JOIN</code>, <code>LEFT JOIN</code>, <code>RIGHT JOIN</code>, <code>FULL OUTER JOIN</code>, <code>CROSS JOIN</code>, and <code>SELF JOIN</code>—to retrieve data from multiple tables. You’ve also learned how to combine tables, apply conditions, use aliases for readability, and optimize queries. Joins are a critical part of querying relational databases and are essential for retrieving meaningful insights from connected data.</p>
<h3 id="chapter-5-aggregating-data">Chapter 5: <strong>Aggregating Data</strong></h3>
<p>In this chapter, we’ll focus on <strong>aggregating data</strong>, which is a critical skill for summarizing, analyzing, and extracting useful insights from large datasets. SQL provides powerful functions to perform operations such as counting, summing, averaging, and more. You’ll learn how to use these functions in combination with grouping and filtering to aggregate data effectively.</p>
<h4 id="what-is-aggregation-in-sql">1. <strong>What is Aggregation in SQL?</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: Aggregation refers to the process of summarizing data by performing calculations across multiple rows. This is typically done using aggregate functions like <code>COUNT()</code>, <code>SUM()</code>, <code>AVG()</code>, <code>MIN()</code>, and <code>MAX()</code>.</p>
</li>
<li>
<p>Aggregating data is often useful when you want to get a high-level overview of your data, such as the total sales, average salary, or maximum temperature in a city over time.</p>
</li>
</ul>
<h4 id="aggregate-functions">2. <strong>Aggregate Functions</strong></h4>
<p>SQL provides several built-in aggregate functions that operate on a set of values and return a single result.</p>
<ul>
<li>
<p><strong>COUNT()</strong>: Returns the number of rows that match a given condition or the total number of rows in a table.</p>
<ul>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">COUNT</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get the number of employees in the <code>employees</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token operator">*</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example with a Condition</strong>: Get the number of employees with a salary above 50,000.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token operator">*</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token number">50000</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
<li>
<p><strong>SUM()</strong>: Adds up the values of a specified column.</p>
<ul>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">SUM</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get the total salary of all employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
<li>
<p><strong>AVG()</strong>: Calculates the average value of a specified column.</p>
<ul>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get the average salary of employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
<li>
<p><strong>MIN()</strong>: Returns the smallest value in a specified column.</p>
<ul>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">MIN</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get the minimum salary of employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">MIN</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
<li>
<p><strong>MAX()</strong>: Returns the largest value in a specified column.</p>
<ul>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">MAX</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get the maximum salary of employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">MAX</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<h4 id="group-by-clause">3. <strong>GROUP BY Clause</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>GROUP BY</code> clause is used in combination with aggregate functions to group rows that share a property into summary rows, like “total sales per region” or “average salary by department”.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> AGGREGATE_FUNCTION<span class="token punctuation">(</span>column2<span class="token punctuation">)</span>
<span class="token keyword">FROM</span> table_name
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> column1<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get the total salary for each department.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department<span class="token punctuation">,</span> <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> 
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Explanation</strong>: In this example, the <code>employees</code> table is grouped by the <code>department</code> column, and for each group (department), we calculate the sum of the <code>salary</code> column. This query returns the total salary per department.</p>
</li>
</ul>
<h4 id="having-clause">4. <strong>HAVING Clause</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>HAVING</code> clause is used to filter results after aggregation, similar to how the <code>WHERE</code> clause is used to filter rows before aggregation. The key difference is that <code>HAVING</code> works with groups created by the <code>GROUP BY</code> clause, while <code>WHERE</code> filters individual rows.</p>
</li>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> AGGREGATE_FUNCTION<span class="token punctuation">(</span>column2<span class="token punctuation">)</span>
<span class="token keyword">FROM</span> table_name
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> column1
<span class="token keyword">HAVING</span> condition<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Get departments with a total salary greater than 200,000.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department<span class="token punctuation">,</span> <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> 
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department
<span class="token keyword">HAVING</span> <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token operator">&gt;</span> <span class="token number">200000</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Explanation</strong>: In this query, we first group employees by department and calculate the total salary per department using <code>SUM(salary)</code>. Then, we filter the departments to only include those with a total salary greater than 200,000 using the <code>HAVING</code> clause.</p>
</li>
</ul>
<h4 id="multiple-aggregate-functions">5. <strong>Multiple Aggregate Functions</strong></h4>
<ul>
<li>You can use multiple aggregate functions in a single query to perform multiple calculations on the same set of rows.</li>
</ul>
<p><strong>Example</strong>: Get the total salary, average salary, and the number of employees in each department.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department<span class="token punctuation">,</span> 
       <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> total_salary<span class="token punctuation">,</span> 
       <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> avg_salary<span class="token punctuation">,</span> 
       <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token operator">*</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> num_employees
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Explanation</strong>: This query retrieves the total salary, average salary, and number of employees for each department. Each aggregate function operates on the <code>salary</code> column, but they are grouped by the <code>department</code> column.</li>
</ul>
<h4 id="using-distinct-with-aggregate-functions">6. <strong>Using DISTINCT with Aggregate Functions</strong></h4>
<ul>
<li><strong>Definition</strong>: You can use the <code>DISTINCT</code> keyword within aggregate functions to perform the calculation on only unique (distinct) values.</li>
</ul>
<p><strong>Example</strong>: Get the number of unique job titles in the <code>employees</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token keyword">DISTINCT</span> job_title<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Explanation</strong>: This query counts the number of unique job titles in the <code>employees</code> table. If there are multiple employees with the same job title, only one instance of that title is counted.</li>
</ul>
<h4 id="combining-aggregation-with-joins">7. <strong>Combining Aggregation with Joins</strong></h4>
<ul>
<li>When working with multiple tables, you can use aggregation with <code>JOIN</code> to summarize data from related tables.</li>
</ul>
<p><strong>Example</strong>: Get the total salary and the number of employees in each department, joining the <code>employees</code> table with the <code>departments</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name<span class="token punctuation">,</span> 
       <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token number">e</span><span class="token punctuation">.</span>employee_id<span class="token punctuation">)</span> <span class="token keyword">AS</span> num_employees<span class="token punctuation">,</span> 
       <span class="token function">SUM</span><span class="token punctuation">(</span><span class="token number">e</span><span class="token punctuation">.</span>salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> total_salary
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> departments <span class="token number">d</span> <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Explanation</strong>: This query retrieves the total salary and the number of employees per department. It first joins the <code>employees</code> table with the <code>departments</code> table on <code>department_id</code>, then groups the result by department name.</li>
</ul>
<h4 id="using-window-functions-for-advanced-aggregation">8. <strong>Using Window Functions for Advanced Aggregation</strong></h4>
<p>Window functions allow you to perform aggregations across a set of rows that are related to the current row within the result set, without collapsing the rows into a single result.</p>
<ul>
<li>
<p><strong>ROW_NUMBER()</strong>: Assigns a unique sequential integer to rows within a partition.</p>
</li>
<li>
<p><strong>RANK()</strong>: Assigns a rank to rows within a partition, with gaps in the ranking for ties.</p>
</li>
<li>
<p><strong>SUM() OVER()</strong>: Performs a sum calculation over a specific window of rows.</p>
</li>
</ul>
<p><strong>Example</strong>: Get the running total of salaries for each employee, ordered by their salary.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span>
       <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> running_total
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Explanation</strong>: This query calculates the running total of salaries for each employee. The <code>SUM(salary) OVER (ORDER BY salary)</code> calculates a cumulative sum as it processes each row, ordered by salary.</li>
</ul>
<h4 id="performance-considerations">9. <strong>Performance Considerations</strong></h4>
<ul>
<li>
<p><strong>Indexes</strong>: Aggregating data over large datasets can be slow if the columns used in the aggregation or the <code>GROUP BY</code> clause are not indexed. Indexing these columns can significantly speed up the query.</p>
</li>
<li>
<p><strong>Memory Usage</strong>: Aggregation operations, especially on large datasets, can consume a lot of memory. Use <code>LIMIT</code> and <code>OFFSET</code> when working with very large datasets to reduce the result size.</p>
</li>
<li>
<p><strong>Optimization</strong>: Consider using optimized database engines or breaking down complex aggregations into smaller steps if performance becomes a concern.</p>
</li>
</ul>
<h3 id="summary-4">Summary:</h3>
<p>Chapter 5 covers the essentials of <strong>aggregating data</strong> in SQL using functions like <code>COUNT()</code>, <code>SUM()</code>, <code>AVG()</code>, <code>MIN()</code>, and <code>MAX()</code>. You’ve learned how to group data with the <code>GROUP BY</code> clause, filter grouped data with the <code>HAVING</code> clause, and use multiple aggregate functions in a single query. Additionally, we covered using <code>DISTINCT</code> with aggregates, performing aggregations with <code>JOIN</code>, and leveraging window functions for more complex aggregation tasks. Aggregating data is a powerful tool for summarizing large datasets and making data-driven decisions.</p>
<h3 id="chapter-6-subqueries-and-nested-queries">Chapter 6: <strong>Subqueries and Nested Queries</strong></h3>
<p>In this chapter, we will explore <strong>subqueries</strong> and <strong>nested queries</strong>, two powerful tools in SQL that allow you to perform more complex operations by embedding queries within other queries. Subqueries can be used to filter, calculate, or transform data in ways that would be difficult with a single query.</p>
<h4 id="what-is-a-subquery">1. <strong>What is a Subquery?</strong></h4>
<ul>
<li>
<p>A <strong>subquery</strong> (or inner query) is a query embedded inside another query. It allows you to perform intermediate steps in a query and use their results as part of the outer query.</p>
</li>
<li>
<p>Subqueries can be used in various places within a SQL statement:</p>
<ul>
<li>
<p><strong>In the WHERE clause</strong> to filter rows based on the result of another query.</p>
</li>
<li>
<p><strong>In the SELECT clause</strong> to compute a value based on another query.</p>
</li>
<li>
<p><strong>In the FROM clause</strong> to define a derived table.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example of a subquery</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id <span class="token keyword">FROM</span> departments <span class="token keyword">WHERE</span> department_name <span class="token operator">=</span> <span class="token string">'Sales'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this query, the subquery <code>(SELECT department_id FROM departments WHERE department_name = 'Sales')</code> returns the <code>department_id</code> of the ‘Sales’ department, and the outer query uses that value to retrieve employees from that department.</li>
</ul>
<h4 id="types-of-subqueries">2. <strong>Types of Subqueries</strong></h4>
<p>There are two main types of subqueries:</p>
<ul>
<li>
<p><strong>Single-row Subqueries</strong>: Return only one row and one column.</p>
</li>
<li>
<p><strong>Multi-row Subqueries</strong>: Return more than one row and potentially multiple columns.</p>
</li>
</ul>
<h5 id="single-row-subqueries">2.1 <strong>Single-Row Subqueries</strong></h5>
<ul>
<li>A <strong>single-row subquery</strong> returns exactly one row and one column. It is typically used when you expect only a single value from the subquery.</li>
</ul>
<p><strong>Example</strong>: Retrieve employees who earn more than the average salary.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>The subquery <code>(SELECT AVG(salary) FROM employees)</code> calculates the average salary, and the outer query retrieves employees with salaries greater than that average.</li>
</ul>
<h5 id="multi-row-subqueries">2.2 <strong>Multi-Row Subqueries</strong></h5>
<ul>
<li>A <strong>multi-row subquery</strong> returns multiple rows and can be used when comparing the outer query to a set of values.</li>
</ul>
<p><strong>Example</strong>: Retrieve employees who work in departments with more than 10 employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> department_id
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> department_id <span class="token operator">IN</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id <span class="token keyword">FROM</span> employees <span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id <span class="token keyword">HAVING</span> <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token operator">*</span><span class="token punctuation">)</span> <span class="token operator">&gt;</span> <span class="token number">10</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this case, the subquery <code>(SELECT department_id FROM employees GROUP BY department_id HAVING COUNT(*) &gt; 10)</code> returns a list of department IDs with more than 10 employees, and the outer query retrieves employees who belong to those departments.</li>
</ul>
<h5 id="correlated-subqueries">2.3 <strong>Correlated Subqueries</strong></h5>
<ul>
<li>A <strong>correlated subquery</strong> is a subquery that references a column from the outer query. Unlike regular subqueries, a correlated subquery is executed once for each row in the outer query.</li>
</ul>
<p><strong>Example</strong>: Get employees who earn more than the average salary in their own department.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> department_id
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>Here, the subquery <code>(SELECT AVG(salary) FROM employees WHERE department_id = e.department_id)</code> calculates the average salary for each department dynamically as the outer query processes each row.</li>
</ul>
<h5 id="subqueries-in-the-from-clause">2.4 <strong>Subqueries in the FROM Clause</strong></h5>
<ul>
<li>A <strong>subquery in the FROM clause</strong> is treated as a derived table (or inline view) that can be joined or selected from in the outer query.</li>
</ul>
<p><strong>Example</strong>: Get the department-wise average salary, but only for departments with more than 5 employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department_id<span class="token punctuation">,</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> avg_salary
<span class="token keyword">FROM</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">IN</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id <span class="token keyword">FROM</span> employees <span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id <span class="token keyword">HAVING</span> <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token operator">*</span><span class="token punctuation">)</span> <span class="token operator">&gt;</span> <span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> dept_salaries
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id<span class="token punctuation">;</span>
</code></pre>
<ul>
<li>The subquery <code>(SELECT department_id, salary FROM employees WHERE department_id IN (SELECT department_id FROM employees GROUP BY department_id HAVING COUNT(*) &gt; 5))</code> is used to create a derived table (<code>dept_salaries</code>) that contains only the relevant rows. The outer query then calculates the average salary for each department.</li>
</ul>
<h4 id="using-subqueries-with-aggregate-functions">3. <strong>Using Subqueries with Aggregate Functions</strong></h4>
<p>Subqueries are commonly used with aggregate functions like <code>COUNT()</code>, <code>SUM()</code>, <code>AVG()</code>, <code>MIN()</code>, and <code>MAX()</code> to calculate values that are then used in the outer query.</p>
<p><strong>Example</strong>: Get employees whose salary is greater than the average salary of all employees.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>Here, the subquery <code>(SELECT AVG(salary) FROM employees)</code> returns the average salary for all employees, and the outer query retrieves employees who earn more than this average.</li>
</ul>
<h4 id="nested-queries-in-the-select-clause">4. <strong>Nested Queries in the SELECT Clause</strong></h4>
<p>You can use subqueries in the <code>SELECT</code> clause to compute a value for each row returned by the outer query.</p>
<p><strong>Example</strong>: Get the employee’s name and their department’s average salary.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> 
       <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id<span class="token punctuation">)</span> <span class="token keyword">AS</span> avg_salary
<span class="token keyword">FROM</span> employees <span class="token number">e</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this query, the subquery calculates the average salary for each employee’s department dynamically for each row returned by the outer query.</li>
</ul>
<h4 id="subqueries-with-exists">5. <strong>Subqueries with EXISTS</strong></h4>
<ul>
<li>The <code>EXISTS</code> operator is used to check if a subquery returns any rows. It returns <code>TRUE</code> if the subquery returns at least one row, and <code>FALSE</code> otherwise.</li>
</ul>
<p><strong>Example</strong>: Get employees who belong to a department that has employees with salaries greater than 100,000.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">WHERE</span> <span class="token keyword">EXISTS</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token number">1</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">AND</span> salary <span class="token operator">&gt;</span> <span class="token number">100000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>The subquery checks if there are any employees in the same department (<code>e.department_id</code>) with a salary greater than 100,000. The outer query returns those employees for whom the subquery condition is met.</li>
</ul>
<h4 id="using-subqueries-with-in-any-and-all">6. <strong>Using Subqueries with IN, ANY, and ALL</strong></h4>
<ul>
<li>
<p><strong>IN</strong>: The <code>IN</code> operator is used to match a value against a list of values returned by a subquery.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> department_id <span class="token operator">IN</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id <span class="token keyword">FROM</span> departments <span class="token keyword">WHERE</span> location <span class="token operator">=</span> <span class="token string">'New York'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>ANY</strong>: The <code>ANY</code> operator compares a value to a set of values returned by a subquery. It returns <code>TRUE</code> if the condition is <code>TRUE</code> for any row in the subquery result.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token keyword">ANY</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>ALL</strong>: The <code>ALL</code> operator compares a value to all values returned by a subquery. It returns <code>TRUE</code> only if the condition is <code>TRUE</code> for all rows in the subquery result.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token keyword">ALL</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> salary <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="performance-considerations-for-subqueries">7. <strong>Performance Considerations for Subqueries</strong></h4>
<ul>
<li>
<p><strong>Efficiency</strong>: Subqueries can be resource-intensive, especially if used with large datasets. Subqueries in the <code>WHERE</code> clause are executed for each row in the outer query (in the case of correlated subqueries), which can slow down performance.</p>
</li>
<li>
<p><strong>Optimization</strong>: Sometimes, subqueries can be replaced by <strong>joins</strong>, which might be more efficient. For example, instead of using a subquery to find the maximum salary in the <code>WHERE</code> clause, a <code>JOIN</code> or <code>GROUP BY</code> might be more efficient.</p>
</li>
<li>
<p><strong>EXPLAIN</strong>: Use the <code>EXPLAIN</code> command to understand the execution plan of your query and optimize subqueries accordingly.</p>
</li>
</ul>
<h4 id="best-practices-for-using-subqueries">8. <strong>Best Practices for Using Subqueries</strong></h4>
<ul>
<li>
<p><strong>Keep it Simple</strong>: Try to keep subqueries as simple as possible. Complex, nested subqueries can be difficult to read and maintain.</p>
</li>
<li>
<p><strong>Avoid Unnecessary Subqueries</strong>: Whenever possible, try to use joins instead of subqueries. Joins are often more efficient and easier to understand.</p>
</li>
<li>
<p><strong>Use Subqueries with Care</strong>: When you need to perform intermediate calculations or comparisons, subqueries are invaluable. But always test performance, especially on large datasets.</p>
</li>
</ul>
<h3 id="summary-5">Summary:</h3>
<p>Chapter 6 covers the concept of <strong>subqueries and nested queries</strong> in SQL, including the different types of subqueries (single-row, multi-row, correlated), and where to use them in various parts of a SQL query (WHERE, SELECT, FROM). We explored common subquery operations like using aggregate functions, checking conditions with <code>EXISTS</code>, and utilizing <code>IN</code>, <code>ANY</code>, and <code>ALL</code> operators. Additionally, we touched on performance considerations and best practices for writing efficient subqueries. Mastering subqueries is essential for solving complex problems in SQL and getting the most out of your data.</p>
<h3 id="chapter-7-modifying-data">Chapter 7: <strong>Modifying Data</strong></h3>
<p>This chapter focuses on modifying the data in a relational database using SQL commands. While querying data is essential for retrieving information, modifying data is crucial for managing and maintaining databases. In SQL, we can modify data using the <code>INSERT</code>, <code>UPDATE</code>, and <code>DELETE</code> commands.</p>
<h4 id="insert-statement">1. <strong>INSERT Statement</strong></h4>
<p>The <code>INSERT</code> statement is used to add new rows to a table. You can either insert specific column values or insert multiple rows at once.</p>
<ul>
<li>
<p><strong>Basic Syntax (Inserting One Row)</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> table_name <span class="token punctuation">(</span>column1<span class="token punctuation">,</span> column2<span class="token punctuation">,</span> column3<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">)</span>
<span class="token keyword">VALUES</span> <span class="token punctuation">(</span>value1<span class="token punctuation">,</span> value2<span class="token punctuation">,</span> value3<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Insert a new employee into the <code>employees</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> department_id<span class="token punctuation">)</span>
<span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'John'</span><span class="token punctuation">,</span> <span class="token string">'Doe'</span><span class="token punctuation">,</span> <span class="token number">55000</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this query, a new row is inserted into the <code>employees</code> table, with values provided for the <code>first_name</code>, <code>last_name</code>, <code>salary</code>, and <code>department_id</code> columns.</li>
</ul>
</li>
<li>
<p><strong>Inserting Data Without Specifying Column Names</strong>:</p>
<ul>
<li>If you are inserting values for every column in the table in the same order as they are defined in the schema, you can omit the column names.</li>
</ul>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees
<span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'Jane'</span><span class="token punctuation">,</span> <span class="token string">'Smith'</span><span class="token punctuation">,</span> <span class="token number">60000</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This is only valid if you’re inserting values for every column and in the exact order that the table schema defines.</li>
</ul>
</li>
<li>
<p><strong>Inserting Multiple Rows</strong>:<br>
You can insert multiple rows at once by using multiple sets of values.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> department_id<span class="token punctuation">)</span>
<span class="token keyword">VALUES</span> 
    <span class="token punctuation">(</span><span class="token string">'Mark'</span><span class="token punctuation">,</span> <span class="token string">'Johnson'</span><span class="token punctuation">,</span> <span class="token number">45000</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    <span class="token punctuation">(</span><span class="token string">'Sara'</span><span class="token punctuation">,</span> <span class="token string">'Williams'</span><span class="token punctuation">,</span> <span class="token number">48000</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    <span class="token punctuation">(</span><span class="token string">'Paul'</span><span class="token punctuation">,</span> <span class="token string">'Brown'</span><span class="token punctuation">,</span> <span class="token number">52000</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="update-statement">2. <strong>UPDATE Statement</strong></h4>
<p>The <code>UPDATE</code> statement is used to modify the existing records in a table. You can update one or more rows by specifying conditions in the <code>WHERE</code> clause.</p>
<ul>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">UPDATE</span> table_name
<span class="token keyword">SET</span> column1 <span class="token operator">=</span> value1<span class="token punctuation">,</span> column2 <span class="token operator">=</span> value2<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
<span class="token keyword">WHERE</span> condition<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Update the salary of an employee.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">UPDATE</span> employees
<span class="token keyword">SET</span> salary <span class="token operator">=</span> <span class="token number">60000</span>
<span class="token keyword">WHERE</span> employee_id <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This query updates the <code>salary</code> for the employee with <code>employee_id = 5</code> to 60,000.</li>
</ul>
</li>
<li>
<p><strong>Updating Multiple Columns</strong>:<br>
You can update multiple columns in a single <code>UPDATE</code> statement.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">UPDATE</span> employees
<span class="token keyword">SET</span> salary <span class="token operator">=</span> <span class="token number">65000</span><span class="token punctuation">,</span> department_id <span class="token operator">=</span> <span class="token number">4</span>
<span class="token keyword">WHERE</span> employee_id <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this case, both the <code>salary</code> and <code>department_id</code> columns are updated for the employee with <code>employee_id = 5</code>.</li>
</ul>
</li>
<li>
<p><strong>Important Considerations</strong>:</p>
<ul>
<li><strong>WHERE Clause</strong>: Always use the <code>WHERE</code> clause to specify which rows to update. If you omit the <code>WHERE</code> clause, <strong>all rows</strong> in the table will be updated.</li>
</ul>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">UPDATE</span> employees
<span class="token keyword">SET</span> salary <span class="token operator">=</span> <span class="token number">50000</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This query would set the salary of <strong>every employee</strong> to 50,000, which is usually not the desired behavior.</li>
</ul>
</li>
<li>
<p><strong>Using Subqueries in UPDATE</strong>: You can also use subqueries in the <code>SET</code> clause to dynamically update values based on other tables.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">UPDATE</span> employees
<span class="token keyword">SET</span> salary <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> employees<span class="token punctuation">.</span>department_id<span class="token punctuation">)</span>
<span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This query sets the salary of employees in department 3 to the average salary of their department.</li>
</ul>
</li>
</ul>
<h4 id="delete-statement">3. <strong>DELETE Statement</strong></h4>
<p>The <code>DELETE</code> statement is used to remove one or more rows from a table based on a specified condition.</p>
<ul>
<li>
<p><strong>Basic Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">DELETE</span> <span class="token keyword">FROM</span> table_name
<span class="token keyword">WHERE</span> condition<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Delete an employee based on <code>employee_id</code>.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">DELETE</span> <span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> employee_id <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This query deletes the row for the employee with <code>employee_id = 10</code>.</li>
</ul>
</li>
<li>
<p><strong>Deleting Multiple Rows</strong>: You can delete multiple rows by specifying a condition that matches several rows.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">DELETE</span> <span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This query deletes all employees who belong to department 3.</li>
</ul>
</li>
<li>
<p><strong>Caution</strong>: Like the <code>UPDATE</code> statement, the <code>DELETE</code> statement should always include a <code>WHERE</code> clause. If you omit it, all rows in the table will be deleted, which is a dangerous operation.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">DELETE</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li>This query would delete every employee from the <code>employees</code> table. Always double-check the conditions before running <code>DELETE</code> statements.</li>
</ul>
</li>
<li>
<p><strong>Using Subqueries with DELETE</strong>: You can also use subqueries with <code>DELETE</code> to remove rows based on a condition from another table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">DELETE</span> <span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> department_id <span class="token operator">IN</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id <span class="token keyword">FROM</span> departments <span class="token keyword">WHERE</span> department_name <span class="token operator">=</span> <span class="token string">'Sales'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this query, employees who belong to the “Sales” department are deleted.</li>
</ul>
</li>
</ul>
<h4 id="truncate-statement">4. <strong>TRUNCATE Statement</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>TRUNCATE</code> statement removes all rows from a table, but unlike <code>DELETE</code>, it does not log individual row deletions and cannot be rolled back in some database systems (such as MySQL).</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">TRUNCATE</span> <span class="token keyword">TABLE</span> table_name<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Remove all rows from the <code>employees</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">TRUNCATE</span> <span class="token keyword">TABLE</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Difference Between <code>DELETE</code> and <code>TRUNCATE</code></strong>:</p>
<ul>
<li>
<p><strong><code>DELETE</code></strong>: Can delete specific rows using a <code>WHERE</code> clause. It is a slower operation as it logs each row deletion and can be rolled back if part of a transaction.</p>
</li>
<li>
<p><strong><code>TRUNCATE</code></strong>: Removes all rows from the table, does not log each row deletion, and cannot be rolled back (depending on the DBMS).</p>
</li>
</ul>
</li>
</ul>
<h4 id="using-transactions-with-data-modification">5. <strong>Using Transactions with Data Modification</strong></h4>
<ul>
<li>
<p>A <strong>transaction</strong> in SQL allows you to execute multiple operations as a single unit. Transactions are particularly useful for ensuring data consistency and integrity.</p>
</li>
<li>
<p><strong>Commands</strong>:</p>
<ul>
<li>
<p><code>BEGIN TRANSACTION</code>: Starts a new transaction.</p>
</li>
<li>
<p><code>COMMIT</code>: Saves all changes made in the current transaction.</p>
</li>
<li>
<p><code>ROLLBACK</code>: Reverts all changes made in the current transaction.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>: Insert a new employee and update the department in a single transaction.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">BEGIN</span> <span class="token keyword">TRANSACTION</span><span class="token punctuation">;</span>

<span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> department_id<span class="token punctuation">)</span>
<span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'Lisa'</span><span class="token punctuation">,</span> <span class="token string">'Taylor'</span><span class="token punctuation">,</span> <span class="token number">55000</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">UPDATE</span> employees
<span class="token keyword">SET</span> department_id <span class="token operator">=</span> <span class="token number">4</span>
<span class="token keyword">WHERE</span> first_name <span class="token operator">=</span> <span class="token string">'Lisa'</span> <span class="token operator">AND</span> last_name <span class="token operator">=</span> <span class="token string">'Taylor'</span><span class="token punctuation">;</span>

<span class="token keyword">COMMIT</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>In this example, the insertion and update are part of a single transaction. If something goes wrong before the <code>COMMIT</code>, the changes can be undone by using <code>ROLLBACK</code>.</li>
</ul>
<h4 id="using-data-modification-with-constraints">6. <strong>Using Data Modification with Constraints</strong></h4>
<ul>
<li>
<p>SQL allows you to define <strong>constraints</strong> to ensure the integrity of your data. These constraints can impact how data modification operations behave:</p>
<ul>
<li>
<p><strong>PRIMARY KEY</strong>: Ensures that each row in a table is unique and not NULL.</p>
</li>
<li>
<p><strong>FOREIGN KEY</strong>: Ensures referential integrity by ensuring that a value in one table exists in another table.</p>
</li>
<li>
<p><strong>CHECK</strong>: Ensures that the value of a column meets certain conditions (e.g., a salary cannot be negative).</p>
</li>
<li>
<p><strong>NOT NULL</strong>: Ensures that a column cannot contain NULL values.</p>
</li>
<li>
<p><strong>UNIQUE</strong>: Ensures that all values in a column are unique.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>: Attempt to insert a row with a duplicate primary key will fail if the primary key constraint is violated.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>employee_id<span class="token punctuation">,</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">)</span>
<span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token string">'Alice'</span><span class="token punctuation">,</span> <span class="token string">'Johnson'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">-- Assuming employee_id is a primary key and 1 already exists</span>
</code></pre>
<ul>
<li>If <code>employee_id</code> is the primary key and already contains the value <code>1</code>, this operation will fail.</li>
</ul>
<h4 id="bulk-operations-and-optimizations">7. <strong>Bulk Operations and Optimizations</strong></h4>
<ul>
<li>
<p><strong>Bulk Inserts</strong>: If you need to insert many rows, it’s more efficient to insert them in bulk rather than inserting one row at a time.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">)</span>
<span class="token keyword">VALUES</span>
    <span class="token punctuation">(</span><span class="token string">'John'</span><span class="token punctuation">,</span> <span class="token string">'Doe'</span><span class="token punctuation">,</span> <span class="token number">50000</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    <span class="token punctuation">(</span><span class="token string">'Jane'</span><span class="token punctuation">,</span> <span class="token string">'Smith'</span><span class="token punctuation">,</span> <span class="token number">55000</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    <span class="token punctuation">(</span><span class="token string">'Mark'</span><span class="token punctuation">,</span> <span class="token string">'Johnson'</span><span class="token punctuation">,</span> <span class="token number">60000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Bulk Updates</strong>: Similarly, bulk updates should be done in a single operation to avoid performance overhead.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">UPDATE</span> employees
<span class="token keyword">SET</span> salary <span class="token operator">=</span> salary <span class="token operator">*</span> <span class="token number">1.1</span>
<span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Using Indexes</strong>: For performance reasons, it’s advisable to index columns that are frequently updated or used in conditions. This helps speed up modifications like <code>UPDATE</code>, <code>DELETE</code>, or <code>INSERT</code> queries.</p>
</li>
</ul>
<h3 id="summary-6">Summary:</h3>
<p>Chapter 7 covers the core SQL statements used to <strong>modify data</strong> in a relational database. You’ve learned how to use the <code>INSERT</code>, <code>UPDATE</code>, and <code>DELETE</code> statements to add, modify, and remove data, respectively. You also explored advanced techniques such as using <code>TRUNCATE</code>, working with transactions, and ensuring data integrity through constraints. Additionally, the chapter touches on optimization strategies for bulk operations and the importance of using indexes to improve performance when modifying large datasets. These skills are critical for maintaining and managing data in a live production environment.</p>
<h3 id="chapter-8-database-constraints-and-integrity">Chapter 8: <strong>Database Constraints and Integrity</strong></h3>
<p>In this chapter, we’ll focus on <strong>database constraints</strong> and <strong>data integrity</strong>, which are fundamental concepts in relational database management. Constraints ensure that the data in the database remains consistent, valid, and reliable by enforcing rules on the data being inserted, updated, or deleted. Understanding and using constraints properly is crucial for maintaining high-quality data in a database.</p>
<h4 id="what-are-database-constraints">1. <strong>What are Database Constraints?</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: Constraints are rules applied to columns or tables that ensure the accuracy and reliability of the data. They help maintain the integrity of the database by preventing invalid data entries and ensuring relationships between tables are properly maintained.</p>
</li>
<li>
<p><strong>Types of Constraints</strong>:</p>
<ul>
<li>
<p><strong>NOT NULL</strong>: Ensures that a column cannot have NULL values.</p>
</li>
<li>
<p><strong>UNIQUE</strong>: Ensures that all values in a column are distinct.</p>
</li>
<li>
<p><strong>PRIMARY KEY</strong>: Ensures that each row in a table is unique and not NULL.</p>
</li>
<li>
<p><strong>FOREIGN KEY</strong>: Enforces a relationship between two tables by ensuring that the value in one table matches a value in another table.</p>
</li>
<li>
<p><strong>CHECK</strong>: Ensures that values in a column meet a specific condition.</p>
</li>
<li>
<p><strong>DEFAULT</strong>: Assigns a default value to a column when no value is specified.</p>
</li>
<li>
<p><strong>INDEX</strong>: Not a constraint per se, but improves the performance of queries by allowing quicker search and retrieval.</p>
</li>
</ul>
</li>
</ul>
<h4 id="not-null-constraint">2. <strong>NOT NULL Constraint</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>NOT NULL</code> constraint ensures that a column cannot have a NULL value. This is useful when you want to ensure that a particular column always contains data.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> table_name <span class="token punctuation">(</span>
    column_name data_type <span class="token operator">NOT</span> <span class="token boolean">NULL</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Create a <code>employees</code> table where <code>first_name</code> and <code>last_name</code> cannot be NULL.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    first_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span> <span class="token operator">NOT</span> <span class="token boolean">NULL</span><span class="token punctuation">,</span>
    last_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span> <span class="token operator">NOT</span> <span class="token boolean">NULL</span><span class="token punctuation">,</span>
    salary <span class="token keyword">DECIMAL</span><span class="token punctuation">(</span><span class="token number">10</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: If you want to ensure that every employee has a first and last name, the <code>NOT NULL</code> constraint prevents inserting any row where these columns are left empty.</p>
</li>
</ul>
<h4 id="unique-constraint">3. <strong>UNIQUE Constraint</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>UNIQUE</code> constraint ensures that all values in a column are unique. Unlike the <code>PRIMARY KEY</code> constraint, the <code>UNIQUE</code> constraint allows NULL values (unless combined with <code>NOT NULL</code>).</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> table_name <span class="token punctuation">(</span>
    column_name data_type <span class="token keyword">UNIQUE</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Ensure that <code>email</code> values in the <code>employees</code> table are unique.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    first_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    last_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    email <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">100</span><span class="token punctuation">)</span> <span class="token keyword">UNIQUE</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: If you have an <code>email</code> column in the <code>employees</code> table, you would use the <code>UNIQUE</code> constraint to make sure no two employees can have the same email address.</p>
</li>
</ul>
<h4 id="primary-key-constraint">4. <strong>PRIMARY KEY Constraint</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>PRIMARY KEY</code> constraint ensures that each row in a table has a unique identifier. It combines the properties of the <code>NOT NULL</code> and <code>UNIQUE</code> constraints. A table can only have one primary key, but the primary key can consist of one or more columns (composite primary key).</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> table_name <span class="token punctuation">(</span>
    column1 data_type <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    column2 data_type
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Create an <code>employees</code> table where <code>employee_id</code> is the primary key.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    first_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    last_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    salary <span class="token keyword">DECIMAL</span><span class="token punctuation">(</span><span class="token number">10</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Composite Primary Key</strong>: You can combine multiple columns to form a composite primary key.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> orders <span class="token punctuation">(</span>
    order_id <span class="token keyword">INT</span><span class="token punctuation">,</span>
    product_id <span class="token keyword">INT</span><span class="token punctuation">,</span>
    <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span> <span class="token punctuation">(</span>order_id<span class="token punctuation">,</span> product_id<span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: The <code>employee_id</code> column in the <code>employees</code> table is used as the primary key, ensuring that each employee has a unique ID.</p>
</li>
</ul>
<h4 id="foreign-key-constraint">5. <strong>FOREIGN KEY Constraint</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>FOREIGN KEY</code> constraint ensures that a value in one table matches a value in another table, creating a relationship between the two tables. This is a way of enforcing referential integrity between tables.</p>
</li>
<li>
<p>The <code>FOREIGN KEY</code> constraint ensures that you cannot insert or update a row in the child table unless the value exists in the parent table.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> table_name <span class="token punctuation">(</span>
    column_name data_type<span class="token punctuation">,</span>
    <span class="token keyword">FOREIGN</span> <span class="token keyword">KEY</span> <span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">REFERENCES</span> parent_table <span class="token punctuation">(</span>parent_column<span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Create an <code>employees</code> table where <code>department_id</code> is a foreign key referencing the <code>departments</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> departments <span class="token punctuation">(</span>
    department_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    department_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    first_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    last_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    department_id <span class="token keyword">INT</span><span class="token punctuation">,</span>
    <span class="token keyword">FOREIGN</span> <span class="token keyword">KEY</span> <span class="token punctuation">(</span>department_id<span class="token punctuation">)</span> <span class="token keyword">REFERENCES</span> departments <span class="token punctuation">(</span>department_id<span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: The <code>department_id</code> in the <code>employees</code> table references the <code>department_id</code> in the <code>departments</code> table, ensuring that employees are only assigned to valid departments.</p>
</li>
<li>
<p><strong>On Delete and On Update Actions</strong>: You can define actions that happen when a referenced row is deleted or updated.</p>
<ul>
<li>
<p><code>ON DELETE CASCADE</code>: Deletes rows in the child table if the referenced row in the parent table is deleted.</p>
</li>
<li>
<p><code>ON UPDATE CASCADE</code>: Updates rows in the child table if the referenced row in the parent table is updated.</p>
</li>
</ul>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    department_id <span class="token keyword">INT</span><span class="token punctuation">,</span>
    <span class="token keyword">FOREIGN</span> <span class="token keyword">KEY</span> <span class="token punctuation">(</span>department_id<span class="token punctuation">)</span> <span class="token keyword">REFERENCES</span> departments<span class="token punctuation">(</span>department_id<span class="token punctuation">)</span>
    <span class="token keyword">ON</span> <span class="token keyword">DELETE</span> <span class="token keyword">CASCADE</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="check-constraint">6. <strong>CHECK Constraint</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>CHECK</code> constraint is used to limit the values that can be inserted into a column. It ensures that all values in a column satisfy a specific condition or rule.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> table_name <span class="token punctuation">(</span>
    column_name data_type <span class="token keyword">CHECK</span> <span class="token punctuation">(</span>condition<span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Create an <code>employees</code> table where the salary must be greater than 0.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    first_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    last_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    salary <span class="token keyword">DECIMAL</span><span class="token punctuation">(</span><span class="token number">10</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token keyword">CHECK</span> <span class="token punctuation">(</span>salary <span class="token operator">&gt;</span> <span class="token number">0</span><span class="token punctuation">)</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: The <code>CHECK</code> constraint ensures that the <code>salary</code> column never contains a value less than or equal to 0.</p>
</li>
</ul>
<h4 id="default-constraint">7. <strong>DEFAULT Constraint</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: The <code>DEFAULT</code> constraint provides a default value for a column when no value is specified during an <code>INSERT</code> operation. This is useful for setting a default value in cases where a value is optional.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> table_name <span class="token punctuation">(</span>
    column_name data_type <span class="token keyword">DEFAULT</span> default_value
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Create an <code>employees</code> table where the <code>hire_date</code> defaults to the current date if not specified.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    first_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    last_name <span class="token keyword">VARCHAR</span><span class="token punctuation">(</span><span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    hire_date <span class="token keyword">DATE</span> <span class="token keyword">DEFAULT</span> <span class="token keyword">CURRENT_DATE</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: If no <code>hire_date</code> is provided when inserting a new employee, the database will automatically set the <code>hire_date</code> to the current date.</p>
</li>
</ul>
<h4 id="indexing-for-performance">8. <strong>Indexing for Performance</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: An <strong>index</strong> is a database object that improves the speed of data retrieval operations on a table. While not a constraint itself, indexes are often used in conjunction with constraints, especially on columns that are frequently queried or used in join conditions.</p>
</li>
<li>
<p><strong>Syntax</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">INDEX</span> index_name
<span class="token keyword">ON</span> table_name <span class="token punctuation">(</span>column_name<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Example</strong>: Create an index on the <code>last_name</code> column of the <code>employees</code> table.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">INDEX</span> idx_last_name <span class="token keyword">ON</span> employees<span class="token punctuation">(</span>last_name<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Use Case</strong>: Indexes speed up <code>SELECT</code> queries that filter or sort by the indexed column. However, indexes can slow down <code>INSERT</code>, <code>UPDATE</code>, and <code>DELETE</code> operations because the index needs to be updated whenever the data changes.</p>
</li>
</ul>
<h4 id="enforcing-data-integrity">9. <strong>Enforcing Data Integrity</strong></h4>
<ul>
<li>
<p>Data integrity refers to the accuracy, consistency, and reliability of data stored in a database. Constraints help ensure data integrity by enforcing rules and relationships within the data.</p>
<ul>
<li>
<p><strong>Entity Integrity</strong>: Ensured by the <code>PRIMARY KEY</code> and <code>NOT NULL</code> constraints.</p>
</li>
<li>
<p><strong>Referential Integrity</strong>: Ensured by the <code>FOREIGN KEY</code> constraint, which maintains relationships between tables.</p>
</li>
<li>
<p><strong>Domain Integrity</strong>: Ensured by the <code>CHECK</code>, <code>DEFAULT</code>, and <code>UNIQUE</code> constraints, which ensure that data is valid within its domain or range.</p>
</li>
</ul>
</li>
</ul>
<h4 id="cascading-actions">10. <strong>Cascading Actions</strong></h4>
<ul>
<li>
<p><strong>CASCADING DELETE</strong> and <strong>CASCADING UPDATE</strong> can be set on <code>FOREIGN KEY</code> relationships to automatically propagate changes when the referenced data changes. These actions ensure referential integrity is maintained even when records are updated or deleted.</p>
</li>
<li>
<p><strong>Example</strong>: When a department is deleted, all employees in that department should also be deleted.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">TABLE</span> employees <span class="token punctuation">(</span>
    employee_id <span class="token keyword">INT</span> <span class="token keyword">PRIMARY</span> <span class="token keyword">KEY</span><span class="token punctuation">,</span>
    department_id <span class="token keyword">INT</span><span class="token punctuation">,</span>
    <span class="token keyword">FOREIGN</span> <span class="token keyword">KEY</span> <span class="token punctuation">(</span>department_id<span class="token punctuation">)</span> <span class="token keyword">REFERENCES</span> departments<span class="token punctuation">(</span>department_id<span class="token punctuation">)</span>
    <span class="token keyword">ON</span> <span class="token keyword">DELETE</span> <span class="token keyword">CASCADE</span>
<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h3 id="summary-7">Summary:</h3>
<p>Chapter 8 covers <strong>database constraints</strong> and <strong>data integrity</strong>, crucial components for ensuring the quality and consistency of data within a relational database. You learned about various constraints like <code>NOT NULL</code>, <code>UNIQUE</code>, <code>PRIMARY KEY</code>, <code>FOREIGN KEY</code>, <code>CHECK</code>, and <code>DEFAULT</code>, which enforce rules on data. You also learned about indexing for performance optimization and the importance of enforcing referential and domain integrity. By properly using constraints, you can ensure that your database maintains high data quality and reliability.</p>
<h3 id="chapter-9-advanced-sql-functions">Chapter 9: <strong>Advanced SQL Functions</strong></h3>
<p>In this chapter, we will dive into some of the <strong>advanced SQL functions</strong> that enhance your ability to manipulate and analyze data. While basic SQL functions like <code>COUNT()</code>, <code>AVG()</code>, and <code>SUM()</code> are commonly used for aggregating data, advanced functions enable more complex operations, transformations, and data manipulation. These functions provide additional power for data analysis, making them essential tools for anyone working with SQL.</p>
<h4 id="string-functions">1. <strong>String Functions</strong></h4>
<p>String functions allow you to manipulate text and perform operations like concatenation, case conversion, searching, and trimming. These functions are crucial for working with textual data.</p>
<ul>
<li>
<p><strong>CONCAT()</strong>: Joins two or more strings together.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> CONCAT<span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> <span class="token string">' '</span><span class="token punctuation">,</span> last_name<span class="token punctuation">)</span> <span class="token keyword">AS</span> full_name <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: The <code>CONCAT</code> function combines the <code>first_name</code> and <code>last_name</code> into a single column <code>full_name</code>.</li>
</ul>
</li>
<li>
<p><strong>SUBSTRING()</strong>: Extracts a portion of a string.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> SUBSTRING<span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> short_name <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: This extracts the first 3 characters of the <code>first_name</code> column.</li>
</ul>
</li>
<li>
<p><strong>UPPER() / LOWER()</strong>: Converts a string to uppercase or lowercase.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> UPPER<span class="token punctuation">(</span>first_name<span class="token punctuation">)</span><span class="token punctuation">,</span> LOWER<span class="token punctuation">(</span>last_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: This converts <code>first_name</code> to uppercase and <code>last_name</code> to lowercase.</li>
</ul>
</li>
<li>
<p><strong>LENGTH()</strong>: Returns the length (number of characters) of a string.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> LENGTH<span class="token punctuation">(</span>first_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: This query returns the <code>first_name</code> along with its length.</li>
</ul>
</li>
<li>
<p><strong>TRIM()</strong>: Removes leading and trailing spaces from a string.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> TRIM<span class="token punctuation">(</span>first_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: This removes any leading or trailing spaces from the <code>first_name</code> column.</li>
</ul>
</li>
<li>
<p><strong>REPLACE()</strong>: Replaces occurrences of a substring within a string.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> REPLACE<span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> <span class="token string">'John'</span><span class="token punctuation">,</span> <span class="token string">'Jack'</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: This replaces all instances of “John” with “Jack” in the <code>first_name</code> column.</li>
</ul>
</li>
</ul>
<h4 id="date-and-time-functions">2. <strong>Date and Time Functions</strong></h4>
<p>Date and time functions are essential for working with temporal data. These functions allow you to extract parts of a date, calculate intervals, and format dates for reporting.</p>
<ul>
<li>
<p><strong>CURRENT_DATE / CURRENT_TIME / CURRENT_TIMESTAMP</strong>: Returns the current date, time, or both.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">CURRENT_DATE</span><span class="token punctuation">,</span> <span class="token keyword">CURRENT_TIME</span><span class="token punctuation">,</span> <span class="token keyword">CURRENT_TIMESTAMP</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>NOW()</strong>: Returns the current date and time.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">NOW</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>DATEADD() / DATEDIFF()</strong>: These functions are used to perform date arithmetic.</p>
<ul>
<li>
<p><strong>DATEADD()</strong>: Adds a specific time interval to a date.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> DATEADD<span class="token punctuation">(</span>day<span class="token punctuation">,</span> <span class="token number">7</span><span class="token punctuation">,</span> <span class="token string">'2025-05-01'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">-- Adds 7 days to the given date</span>
</code></pre>
</li>
<li>
<p><strong>DATEDIFF()</strong>: Calculates the difference between two dates.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> DATEDIFF<span class="token punctuation">(</span><span class="token string">'2025-05-11'</span><span class="token punctuation">,</span> <span class="token string">'2025-01-01'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">-- Returns the number of days between the two dates</span>
</code></pre>
</li>
</ul>
</li>
<li>
<p><strong>EXTRACT()</strong>: Extracts a specific part (e.g., year, month, day) from a date.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> EXTRACT<span class="token punctuation">(</span>YEAR <span class="token keyword">FROM</span> hire_date<span class="token punctuation">)</span> <span class="token keyword">AS</span> hire_year <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>DATE_FORMAT()</strong> (for MySQL) or <strong>TO_CHAR()</strong> (for PostgreSQL/Oracle): Formats a date into a specific string format.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> DATE_FORMAT<span class="token punctuation">(</span>hire_date<span class="token punctuation">,</span> <span class="token string">'%Y-%m-%d'</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> formatted_date <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>NOW() and INTERVAL</strong>: Adding or subtracting time using <code>INTERVAL</code>.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">NOW</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-</span> INTERVAL <span class="token number">1</span> MONTH<span class="token punctuation">;</span>  <span class="token comment">-- Subtracts 1 month from the current date</span>
</code></pre>
</li>
<li>
<p><strong>DAYNAME(), MONTHNAME()</strong>: Extracts the name of the day or month.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> DAYNAME<span class="token punctuation">(</span>hire_date<span class="token punctuation">)</span><span class="token punctuation">,</span> MONTHNAME<span class="token punctuation">(</span>hire_date<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="mathematical-functions">3. <strong>Mathematical Functions</strong></h4>
<p>Mathematical functions allow you to perform calculations and work with numeric data.</p>
<ul>
<li>
<p><strong>ROUND()</strong>: Rounds a number to a specified number of decimal places.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">ROUND</span><span class="token punctuation">(</span>salary<span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Example</strong>: Rounds the <code>salary</code> column to two decimal places.</li>
</ul>
</li>
<li>
<p><strong>CEIL() / FLOOR()</strong>: Rounds a number up (to the nearest integer) or down (to the nearest integer).</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> CEIL<span class="token punctuation">(</span>salary<span class="token punctuation">)</span><span class="token punctuation">,</span> FLOOR<span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>ABS()</strong>: Returns the absolute value of a number.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> ABS<span class="token punctuation">(</span><span class="token operator">-</span><span class="token number">100</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>RAND() / RANDOM()</strong>: Generates a random number between 0 and 1.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> RAND<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>POW() / POWER()</strong>: Raises a number to a specified power.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> POWER<span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">-- 2 raised to the power of 3</span>
</code></pre>
</li>
<li>
<p><strong>SQRT()</strong>: Returns the square root of a number.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> SQRT<span class="token punctuation">(</span><span class="token number">16</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  <span class="token comment">-- Returns 4</span>
</code></pre>
</li>
</ul>
<h4 id="conditional-functions">4. <strong>Conditional Functions</strong></h4>
<p>Conditional functions enable you to return different results based on certain conditions, similar to <code>if-else</code> statements in programming.</p>
<ul>
<li>
<p><strong>CASE / CASE WHEN</strong>: Provides conditional logic directly in a query, returning different results based on conditions.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span>
       <span class="token keyword">CASE</span> 
           <span class="token keyword">WHEN</span> salary <span class="token operator">&gt;</span> <span class="token number">60000</span> <span class="token keyword">THEN</span> <span class="token string">'High'</span>
           <span class="token keyword">WHEN</span> salary <span class="token operator">BETWEEN</span> <span class="token number">40000</span> <span class="token operator">AND</span> <span class="token number">60000</span> <span class="token keyword">THEN</span> <span class="token string">'Medium'</span>
           <span class="token keyword">ELSE</span> <span class="token string">'Low'</span>
       <span class="token keyword">END</span> <span class="token keyword">AS</span> salary_category
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>COALESCE()</strong>: Returns the first non-NULL value from a list of arguments.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">COALESCE</span><span class="token punctuation">(</span><span class="token boolean">NULL</span><span class="token punctuation">,</span> <span class="token boolean">NULL</span><span class="token punctuation">,</span> <span class="token string">'Hello'</span><span class="token punctuation">,</span> <span class="token string">'World'</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> result<span class="token punctuation">;</span>  <span class="token comment">-- Returns 'Hello'</span>
</code></pre>
</li>
<li>
<p><strong>NULLIF()</strong>: Returns <code>NULL</code> if two expressions are equal, otherwise returns the first expression.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">NULLIF</span><span class="token punctuation">(</span>salary<span class="token punctuation">,</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="window-functions">5. <strong>Window Functions</strong></h4>
<p>Window functions allow you to perform calculations over a specific range of rows related to the current row, without collapsing the result into a single summary row. These are especially useful for running totals, ranking, and moving averages.</p>
<ul>
<li>
<p><strong>ROW_NUMBER()</strong>: Assigns a unique number to each row within a partition, starting at 1.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> ROW_NUMBER<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> rank
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>RANK() / DENSE_RANK()</strong>: Assigns a rank to each row, with <code>RANK()</code> giving gaps between equal values, and <code>DENSE_RANK()</code> giving consecutive ranks.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> RANK<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> salary_rank
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>NTILE()</strong>: Divides the result set into a specified number of roughly equal parts (bins).</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> NTILE<span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary <span class="token keyword">DESC</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> quartile
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>LEAD() / LAG()</strong>: Accesses the value of a row in the result set that comes before (LAG) or after (LEAD) the current row.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> LEAD<span class="token punctuation">(</span>salary<span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> next_salary
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>SUM() OVER()</strong>: Computes a cumulative sum across a range of rows.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> salary<span class="token punctuation">,</span> <span class="token function">SUM</span><span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">OVER</span> <span class="token punctuation">(</span><span class="token keyword">ORDER</span> <span class="token keyword">BY</span> salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> running_total
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="grouping-and-aggregating-with-advanced-functions">6. <strong>Grouping and Aggregating with Advanced Functions</strong></h4>
<p>In addition to standard aggregation functions like <code>COUNT()</code>, <code>SUM()</code>, and <code>AVG()</code>, there are other advanced ways to aggregate and group data.</p>
<ul>
<li>
<p><strong>GROUP_CONCAT()</strong> (MySQL) / <strong>STRING_AGG()</strong> (PostgreSQL, SQL Server): Concatenates values from multiple rows into a single string.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department_id<span class="token punctuation">,</span> GROUP_CONCAT<span class="token punctuation">(</span>first_name <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> first_name<span class="token punctuation">)</span> <span class="token keyword">AS</span> employee_names
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>ARRAY_AGG()</strong> (PostgreSQL): Aggregates values into an array.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department_id<span class="token punctuation">,</span> ARRAY_AGG<span class="token punctuation">(</span>first_name<span class="token punctuation">)</span> <span class="token keyword">AS</span> employee_names
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>JSON_AGG()</strong> (PostgreSQL): Aggregates rows into a JSON array.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department_id<span class="token punctuation">,</span> JSON_AGG<span class="token punctuation">(</span>first_name<span class="token punctuation">)</span> <span class="token keyword">AS</span> employee_names
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="user-defined-functions-udfs">7. <strong>User-Defined Functions (UDFs)</strong></h4>
<ul>
<li>In some databases (e.g., PostgreSQL, MySQL, SQL Server), you can create your own functions to perform custom logic in SQL queries. These functions can be scalar functions (returning a single value) or table-valued functions (returning a set of rows).</li>
</ul>
<p><strong>Example</strong>: Creating a simple function to calculate a bonus based on salary.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">FUNCTION</span> calculate_bonus<span class="token punctuation">(</span>salary <span class="token keyword">DECIMAL</span><span class="token punctuation">)</span>
<span class="token keyword">RETURNS</span> <span class="token keyword">DECIMAL</span> <span class="token keyword">AS</span> $$
<span class="token keyword">BEGIN</span>
  <span class="token keyword">RETURN</span> salary <span class="token operator">*</span> <span class="token number">0.1</span><span class="token punctuation">;</span>
<span class="token keyword">END</span><span class="token punctuation">;</span>
$$ LANGUAGE plpgsql<span class="token punctuation">;</span>
</code></pre>
<ul>
<li>
<p><strong>Using the UDF</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> calculate_bonus<span class="token punctuation">(</span>salary<span class="token punctuation">)</span> <span class="token keyword">AS</span> bonus
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h3 id="summary-8">Summary:</h3>
<p>Chapter 9 covers advanced SQL functions that give you enhanced control over data manipulation and analysis. You’ve learned how to work with <strong>string functions</strong>, <strong>date and time functions</strong>, <strong>mathematical functions</strong>, <strong>conditional functions</strong>, and <strong>window functions</strong>. Additionally, we explored advanced aggregation techniques like <code>GROUP_CONCAT()</code> and <code>STRING_AGG()</code>, as well as creating your own <strong>user-defined functions (UDFs)</strong> for custom logic. These advanced functions are vital for performing complex data analysis, reporting, and transformation tasks. Mastery of these functions allows you to leverage the full power of SQL for sophisticated database operations.</p>
<h3 id="chapter-10-database-design-and-normalization">Chapter 10: <strong>Database Design and Normalization</strong></h3>
<p>In this chapter, we will explore <strong>database design</strong> and <strong>normalization</strong>, two crucial concepts that help you create efficient, scalable, and maintainable databases. Proper database design ensures that your data is organized in a way that reduces redundancy, improves data integrity, and optimizes performance. Normalization is a key part of this process, as it helps break down complex data structures into simpler, more manageable tables while maintaining relationships between them.</p>
<h4 id="introduction-to-database-design">1. <strong>Introduction to Database Design</strong></h4>
<ul>
<li>
<p><strong>Database Design</strong> is the process of creating the structure of a database, which includes defining tables, columns, data types, relationships, and constraints. Good database design is essential for ensuring that data is stored efficiently and is easy to query, update, and maintain.</p>
</li>
<li>
<p><strong>Goals of Database Design</strong>:</p>
<ul>
<li>
<p><strong>Data Integrity</strong>: Ensuring that data is accurate, consistent, and reliable.</p>
</li>
<li>
<p><strong>Efficiency</strong>: Organizing data in a way that minimizes storage space and maximizes retrieval speed.</p>
</li>
<li>
<p><strong>Scalability</strong>: Ensuring that the database can grow and handle larger amounts of data.</p>
</li>
<li>
<p><strong>Maintainability</strong>: Designing the database in a way that is easy to update, modify, and scale over time.</p>
</li>
</ul>
</li>
</ul>
<h4 id="understanding-entities-and-relationships">2. <strong>Understanding Entities and Relationships</strong></h4>
<ul>
<li>
<p><strong>Entities</strong>: Entities are objects or concepts that have data stored about them. For example, in a database for an e-commerce system, <code>Customers</code>, <code>Orders</code>, and <code>Products</code> are entities.</p>
</li>
<li>
<p><strong>Attributes</strong>: Attributes are the data fields that describe an entity. For example, a <code>Customer</code> entity might have attributes such as <code>CustomerID</code>, <code>FirstName</code>, <code>LastName</code>, and <code>Email</code>.</p>
</li>
<li>
<p><strong>Relationships</strong>: Relationships describe how entities are connected. In a relational database, relationships are usually represented using <strong>foreign keys</strong>. For example:</p>
<ul>
<li>
<p>A <strong>one-to-many relationship</strong> between <code>Customers</code> and <code>Orders</code>: A customer can place many orders, but each order is placed by only one customer.</p>
</li>
<li>
<p>A <strong>many-to-many relationship</strong> between <code>Orders</code> and <code>Products</code>: An order can contain multiple products, and each product can appear in multiple orders. This is typically represented by creating a <strong>junction table</strong> to resolve the many-to-many relationship.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example of a Relationship</strong>:</p>
<ul>
<li>
<p><code>Customers</code> (CustomerID, FirstName, LastName)</p>
</li>
<li>
<p><code>Orders</code> (OrderID, OrderDate, CustomerID) — <strong>CustomerID</strong> is a foreign key referencing <code>Customers</code></p>
</li>
</ul>
<h4 id="normalization-the-process-of-organizing-data">3. <strong>Normalization: The Process of Organizing Data</strong></h4>
<p><strong>Normalization</strong> is the process of organizing data in a way that eliminates redundancy and dependencies. By following the rules of normalization, you can design databases that are easier to maintain, avoid anomalies, and improve performance.</p>
<ul>
<li><strong>Goal of Normalization</strong>: To remove data redundancy (repetition of data) and to ensure data integrity by organizing tables in such a way that updates, inserts, and deletes are efficient and consistent.</li>
</ul>
<p><strong>Normal Forms (NF)</strong>: Normalization involves splitting a database into multiple tables to achieve the following stages, called <strong>normal forms</strong>. There are several normal forms, but the first three (1NF, 2NF, and 3NF) are the most commonly used.</p>
<h4 id="first-normal-form-1nf-–-eliminate-repeating-groups">4. <strong>First Normal Form (1NF)</strong> – Eliminate Repeating Groups</h4>
<ul>
<li>
<p><strong>1NF Definition</strong>: A table is in <strong>First Normal Form (1NF)</strong> if it contains only atomic values (i.e., indivisible values), and each record (row) is unique.</p>
</li>
<li>
<p><strong>Issues Addressed by 1NF</strong>:</p>
<ul>
<li>
<p><strong>Repeating Groups</strong>: In a table, a column should not contain multiple values. For example, a <code>PhoneNumbers</code> column should not store multiple phone numbers in a single cell.</p>
</li>
<li>
<p><strong>Atomic Values</strong>: Each column should hold a single, indivisible value.</p>
</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>:</p>
<ul>
<li>
<p>Before 1NF:</p>
<pre><code>EmployeeID | Name        | PhoneNumbers
------------------------------------------
1          | John Smith  | 123-4567, 234-5678
2          | Jane Doe    | 345-6789
</code></pre>
</li>
<li>
<p>After 1NF (splitting the phone numbers into separate rows):</p>
<pre><code>EmployeeID | Name        | PhoneNumber
----------------------------------------
1          | John Smith  | 123-4567
1          | John Smith  | 234-5678
2          | Jane Doe    | 345-6789
</code></pre>
</li>
</ul>
<h4 id="second-normal-form-2nf-–-eliminate-partial-dependencies">5. <strong>Second Normal Form (2NF)</strong> – Eliminate Partial Dependencies</h4>
<ul>
<li>
<p><strong>2NF Definition</strong>: A table is in <strong>Second Normal Form (2NF)</strong> if it is in 1NF and all non-key attributes are fully functionally dependent on the primary key. In other words, if a table has a composite primary key (a primary key consisting of multiple columns), every non-key attribute must depend on all of the columns in the primary key, not just part of it.</p>
</li>
<li>
<p><strong>Issues Addressed by 2NF</strong>:</p>
<ul>
<li><strong>Partial Dependency</strong>: When non-key columns depend on only part of a composite primary key, it creates redundancy and anomalies. These dependencies should be removed.</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>:</p>
<ul>
<li>
<p>Before 2NF (composite primary key of <code>StudentID</code> and <code>CourseID</code>):</p>
<pre><code>StudentID | CourseID | Instructor   | InstructorPhone
-----------------------------------------------------
1         | 101      | Dr. Smith    | 123-4567
1         | 102      | Dr. Johnson  | 234-5678
2         | 101      | Dr. Smith    | 123-4567
</code></pre>
</li>
<li>
<p>After 2NF (splitting the instructor information into a separate table):</p>
<ul>
<li>
<p><code>Enrollments</code> table:</p>
<pre><code>StudentID | CourseID
---------------------
1         | 101
1         | 102
2         | 101
</code></pre>
</li>
<li>
<p><code>Instructors</code> table:</p>
<pre><code>CourseID | Instructor   | InstructorPhone
------------------------------------------
101      | Dr. Smith    | 123-4567
102      | Dr. Johnson  | 234-5678
</code></pre>
</li>
</ul>
</li>
</ul>
<h4 id="third-normal-form-3nf-–-eliminate-transitive-dependencies">6. <strong>Third Normal Form (3NF)</strong> – Eliminate Transitive Dependencies</h4>
<ul>
<li>
<p><strong>3NF Definition</strong>: A table is in <strong>Third Normal Form (3NF)</strong> if it is in 2NF and all of its non-key attributes are not transitively dependent on the primary key. In other words, there should be no indirect dependencies between non-key attributes.</p>
</li>
<li>
<p><strong>Issues Addressed by 3NF</strong>:</p>
<ul>
<li><strong>Transitive Dependency</strong>: When non-key columns depend on other non-key columns, it creates redundancy and unnecessary dependencies.</li>
</ul>
</li>
</ul>
<p><strong>Example</strong>:</p>
<ul>
<li>
<p>Before 3NF:</p>
<pre><code>EmployeeID | DepartmentID | DepartmentName | DepartmentLocation
---------------------------------------------------------------
1          | 101          | HR             | Building A
2          | 102          | IT             | Building B
</code></pre>
</li>
<li>
<p>After 3NF (moving <code>DepartmentName</code> and <code>DepartmentLocation</code> into a separate table):</p>
<ul>
<li>
<p><code>Employees</code> table:</p>
<pre><code>EmployeeID | DepartmentID
-------------------------
1          | 101
2          | 102
</code></pre>
</li>
<li>
<p><code>Departments</code> table:</p>
<pre><code>DepartmentID | DepartmentName | DepartmentLocation
---------------------------------------------------
101          | HR             | Building A
102          | IT             | Building B
</code></pre>
</li>
</ul>
</li>
</ul>
<h4 id="boyce-codd-normal-form-bcnf">7. <strong>Boyce-Codd Normal Form (BCNF)</strong></h4>
<ul>
<li>
<p><strong>BCNF Definition</strong>: A table is in <strong>Boyce-Codd Normal Form (BCNF)</strong> if it is in 3NF and if every determinant is a candidate key. A determinant is any attribute that can uniquely determine other attributes in the table.</p>
</li>
<li>
<p>BCNF is a stricter version of 3NF and deals with certain types of anomalies that can still occur in 3NF.</p>
</li>
</ul>
<p><strong>Example</strong>:</p>
<ul>
<li>If a table has a functional dependency where a non-key attribute determines another non-key attribute, it may violate BCNF, even though it is in 3NF.</li>
</ul>
<h4 id="fourth-normal-form-4nf">8. <strong>Fourth Normal Form (4NF)</strong></h4>
<ul>
<li>
<p><strong>4NF Definition</strong>: A table is in <strong>Fourth Normal Form (4NF)</strong> if it is in BCNF and there are no multi-valued dependencies. A multi-valued dependency occurs when one attribute in a table determines multiple independent attributes.</p>
</li>
<li>
<p><strong>Issues Addressed by 4NF</strong>:</p>
<ul>
<li><strong>Multi-Valued Dependency</strong>: This occurs when a single column determines multiple other columns, leading to data redundancy.</li>
</ul>
</li>
</ul>
<h4 id="fifth-normal-form-5nf">9. <strong>Fifth Normal Form (5NF)</strong></h4>
<ul>
<li><strong>5NF Definition</strong>: A table is in <strong>Fifth Normal Form (5NF)</strong> if it is in 4NF and cannot be decomposed further without losing information. This usually involves eliminating any remaining redundancy in the data through complex relationships.</li>
</ul>
<h4 id="denormalization">10. <strong>Denormalization</strong></h4>
<ul>
<li>
<p><strong>Definition</strong>: <strong>Denormalization</strong> is the process of combining tables that were split during normalization to improve read performance. This is typically done when performance needs outweigh the benefits of strict normalization, especially in data warehousing or reporting applications.</p>
</li>
<li>
<p><strong>Example</strong>: A query that joins multiple tables and performs complex aggregation might be slow, so denormalizing the data to store aggregated values can improve performance.</p>
</li>
</ul>
<h3 id="summary-9">Summary:</h3>
<p>Chapter 10 explores the principles of <strong>database design</strong> and <strong>normalization</strong>. We’ve discussed the importance of organizing data into well-defined tables, eliminating redundancy, and maintaining relationships between entities. By applying normalization techniques (1NF, 2NF, 3NF, BCNF, 4NF, 5NF), we ensure that the database is free from anomalies and maintains data integrity. Additionally, we explored <strong>denormalization</strong>, which may be used in certain cases to improve performance by reducing the need for complex joins and queries. Proper database design and normalization lead to efficient, reliable, and maintainable databases that scale as your application grows.</p>
<h3 id="chapter-11-sql-tips-and-tricks-for-efficient-querying-and-database-management">Chapter 11: <strong>SQL Tips and Tricks for Efficient Querying and Database Management</strong></h3>
<p>In this final chapter, we’ll cover some <strong>practical tips and tricks</strong> that will help you become more efficient with SQL. These tips will improve your query writing, performance optimization, and database management skills. They will also give you insights into best practices, common pitfalls, and ways to troubleshoot SQL queries and manage large datasets.</p>
<h4 id="use-aliases-for-readable-queries">1. <strong>Use Aliases for Readable Queries</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Aliases can make your queries easier to read and maintain, especially when working with complex joins or derived columns.</p>
</li>
<li>
<p><strong>Example</strong>: Instead of writing long table names repeatedly, use aliases.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token number">e</span><span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> <span class="token number">e</span><span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees <span class="token keyword">AS</span> <span class="token number">e</span>
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> departments <span class="token keyword">AS</span> <span class="token number">d</span> <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="use-explain-for-query-performance">2. <strong>Use <code>EXPLAIN</code> for Query Performance</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Use the <code>EXPLAIN</code> or <code>EXPLAIN ANALYZE</code> keyword before your query to view the query execution plan. This can help you identify performance bottlenecks such as full table scans or inefficient joins.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">EXPLAIN</span> <span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> salary <span class="token operator">&gt;</span> <span class="token number">50000</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Why it helps</strong>: This will show you how SQL is executing your query, which indexes are used, and how tables are joined. It’s invaluable for performance tuning.</p>
</li>
</ul>
<h4 id="avoid-select--in-production-queries">3. <strong>Avoid <code>SELECT *</code> in Production Queries</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Avoid using <code>SELECT *</code> unless necessary. Always specify the columns you need.</p>
</li>
<li>
<p><strong>Why it helps</strong>: Selecting unnecessary columns increases I/O and can slow down your query, especially if the table is large. It also ensures better control over the data retrieved.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary <span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="use-join-instead-of-subqueries-when-possible">4. <strong>Use <code>JOIN</code> Instead of Subqueries When Possible</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: In most cases, a <code>JOIN</code> is faster than a subquery because subqueries may result in multiple executions, which can impact performance.</p>
</li>
<li>
<p><strong>Why it helps</strong>: Joins allow the database engine to perform optimizations, reducing query time.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token comment">-- Using JOIN</span>
<span class="token keyword">SELECT</span> <span class="token number">e</span><span class="token punctuation">.</span>first_name<span class="token punctuation">,</span> <span class="token number">e</span><span class="token punctuation">.</span>last_name<span class="token punctuation">,</span> <span class="token number">d</span><span class="token punctuation">.</span>department_name
<span class="token keyword">FROM</span> employees <span class="token number">e</span>
<span class="token keyword">INNER</span> <span class="token keyword">JOIN</span> departments <span class="token number">d</span> <span class="token keyword">ON</span> <span class="token number">e</span><span class="token punctuation">.</span>department_id <span class="token operator">=</span> <span class="token number">d</span><span class="token punctuation">.</span>department_id<span class="token punctuation">;</span>
</code></pre>
<ul>
<li><strong>Vs</strong></li>
</ul>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token comment">-- Using Subquery</span>
<span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name 
<span class="token keyword">FROM</span> employees 
<span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">SELECT</span> department_id <span class="token keyword">FROM</span> departments <span class="token keyword">WHERE</span> department_name <span class="token operator">=</span> <span class="token string">'Sales'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="leverage-indexes-for-faster-lookups">5. <strong>Leverage Indexes for Faster Lookups</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Index columns that are frequently used in <code>WHERE</code>, <code>JOIN</code>, or <code>ORDER BY</code> clauses. Indexing speeds up data retrieval, but be mindful of adding too many indexes, as they can slow down <code>INSERT</code>, <code>UPDATE</code>, and <code>DELETE</code> operations.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">INDEX</span> idx_employee_department <span class="token keyword">ON</span> employees<span class="token punctuation">(</span>department_id<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="use-case-for-conditional-logic">6. <strong>Use <code>CASE</code> for Conditional Logic</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Use the <code>CASE</code> statement to implement conditional logic directly in your queries, rather than performing these operations in your application logic.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span>
       <span class="token keyword">CASE</span>
           <span class="token keyword">WHEN</span> salary <span class="token operator">&gt;</span> <span class="token number">100000</span> <span class="token keyword">THEN</span> <span class="token string">'High'</span>
           <span class="token keyword">WHEN</span> salary <span class="token operator">BETWEEN</span> <span class="token number">50000</span> <span class="token operator">AND</span> <span class="token number">100000</span> <span class="token keyword">THEN</span> <span class="token string">'Medium'</span>
           <span class="token keyword">ELSE</span> <span class="token string">'Low'</span>
       <span class="token keyword">END</span> <span class="token keyword">AS</span> salary_category
<span class="token keyword">FROM</span> employees<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="optimize-group-by-queries">7. <strong>Optimize <code>GROUP BY</code> Queries</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: When using <code>GROUP BY</code>, always ensure that the grouping column is indexed if possible. This will help in reducing the time required for grouping and aggregation.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> department_id<span class="token punctuation">,</span> <span class="token function">COUNT</span><span class="token punctuation">(</span><span class="token operator">*</span><span class="token punctuation">)</span> <span class="token keyword">AS</span> employee_count
<span class="token keyword">FROM</span> employees
<span class="token keyword">GROUP</span> <span class="token keyword">BY</span> department_id<span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="be-mindful-of-null-values">8. <strong>Be Mindful of NULL Values</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Be careful when dealing with <code>NULL</code> values, as they can lead to unexpected results. Always use <code>IS NULL</code> or <code>IS NOT NULL</code> when filtering for <code>NULL</code> values.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name<span class="token punctuation">,</span> last_name
<span class="token keyword">FROM</span> employees
<span class="token keyword">WHERE</span> middle_name <span class="token operator">IS</span> <span class="token boolean">NULL</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="batch-updates-and-inserts-for-large-datasets">9. <strong>Batch Updates and Inserts for Large Datasets</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: For large datasets, it’s better to batch <code>INSERT</code>, <code>UPDATE</code>, and <code>DELETE</code> operations to minimize the load on the database.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<ul>
<li>
<p>Instead of running multiple <code>INSERT</code> statements:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">)</span> <span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'John'</span><span class="token punctuation">,</span> <span class="token string">'Doe'</span><span class="token punctuation">,</span> <span class="token number">50000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">)</span> <span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'Jane'</span><span class="token punctuation">,</span> <span class="token string">'Doe'</span><span class="token punctuation">,</span> <span class="token number">60000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>Use a single batch insert:</li>
</ul>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> employees <span class="token punctuation">(</span>first_name<span class="token punctuation">,</span> last_name<span class="token punctuation">,</span> salary<span class="token punctuation">)</span>
<span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'John'</span><span class="token punctuation">,</span> <span class="token string">'Doe'</span><span class="token punctuation">,</span> <span class="token number">50000</span><span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token punctuation">(</span><span class="token string">'Jane'</span><span class="token punctuation">,</span> <span class="token string">'Doe'</span><span class="token punctuation">,</span> <span class="token number">60000</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<h4 id="use-limit-and-offset-for-pagination">10. <strong>Use <code>LIMIT</code> and <code>OFFSET</code> for Pagination</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: When dealing with large result sets, use <code>LIMIT</code> and <code>OFFSET</code> for pagination to improve performance and reduce memory usage.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">LIMIT</span> <span class="token number">10</span> <span class="token keyword">OFFSET</span> <span class="token number">0</span><span class="token punctuation">;</span>  <span class="token comment">-- First page</span>
<span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">LIMIT</span> <span class="token number">10</span> <span class="token keyword">OFFSET</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token comment">-- Second page</span>
</code></pre>
</li>
</ul>
<h4 id="avoid-complex-joins-on-large-tables">11. <strong>Avoid Complex Joins on Large Tables</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Avoid joining large tables without proper indexing or filtering. If possible, use smaller, pre-filtered datasets before performing joins.</p>
</li>
<li>
<p><strong>Why it helps</strong>: Joining large tables without filtering or indexing can result in very slow queries.</p>
</li>
<li>
<p><strong>Best Practice</strong>: Apply filters (<code>WHERE</code> conditions) early to limit the size of the datasets being joined.</p>
</li>
</ul>
<h4 id="avoid-functions-in-where-clauses">12. <strong>Avoid Functions in WHERE Clauses</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Avoid using functions (like <code>LOWER()</code>, <code>UPPER()</code>, or <code>DATE()</code>) in the <code>WHERE</code> clause as they can disable the use of indexes, leading to slower queries.</p>
</li>
<li>
<p><strong>Why it helps</strong>: Functions in the <code>WHERE</code> clause cause the database to scan all rows rather than using indexes effectively.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token comment">-- Bad practice (using functions in WHERE clause)</span>
<span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> LOWER<span class="token punctuation">(</span>first_name<span class="token punctuation">)</span> <span class="token operator">=</span> <span class="token string">'john'</span><span class="token punctuation">;</span>

<span class="token comment">-- Better practice</span>
<span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> first_name <span class="token operator">=</span> <span class="token string">'John'</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="use-union-vs-union-all-wisely">13. <strong>Use <code>UNION</code> vs <code>UNION ALL</code> Wisely</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Use <code>UNION ALL</code> when you don’t need to remove duplicates, as it’s faster than <code>UNION</code> because <code>UNION</code> performs an additional step of removing duplicates.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<ul>
<li>
<p><strong><code>UNION</code></strong> (removes duplicates):</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">1</span>
<span class="token keyword">UNION</span>
<span class="token keyword">SELECT</span> first_name <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong><code>UNION ALL</code></strong> (does not remove duplicates):</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> first_name <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">1</span>
<span class="token keyword">UNION</span> <span class="token keyword">ALL</span>
<span class="token keyword">SELECT</span> first_name <span class="token keyword">FROM</span> employees <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
</li>
</ul>
<h4 id="consider-denormalization-for-reporting">14. <strong>Consider Denormalization for Reporting</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: For read-heavy applications, such as reporting, consider denormalizing your data to reduce the need for complex joins. This can improve performance, though it comes at the cost of increased storage and potential for data inconsistency.</p>
</li>
<li>
<p><strong>Example</strong>: Store pre-aggregated data for reporting purposes to avoid recalculating the same values multiple times.</p>
</li>
</ul>
<h4 id="use-transactions-for-data-integrity">15. <strong>Use Transactions for Data Integrity</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: Always use transactions (<code>BEGIN</code>, <code>COMMIT</code>, <code>ROLLBACK</code>) when performing multiple data-modifying operations. This ensures that either all changes are applied or none, preserving data consistency.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">BEGIN</span> <span class="token keyword">TRANSACTION</span><span class="token punctuation">;</span>

<span class="token keyword">UPDATE</span> employees <span class="token keyword">SET</span> salary <span class="token operator">=</span> salary <span class="token operator">+</span> <span class="token number">5000</span> <span class="token keyword">WHERE</span> department_id <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span>
<span class="token keyword">INSERT</span> <span class="token keyword">INTO</span> audit_log <span class="token punctuation">(</span><span class="token keyword">action</span><span class="token punctuation">,</span> <span class="token keyword">timestamp</span><span class="token punctuation">)</span> <span class="token keyword">VALUES</span> <span class="token punctuation">(</span><span class="token string">'Salary Update'</span><span class="token punctuation">,</span> <span class="token function">NOW</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">COMMIT</span><span class="token punctuation">;</span>  <span class="token comment">-- If everything works as expected</span>
<span class="token comment">-- or</span>
<span class="token keyword">ROLLBACK</span><span class="token punctuation">;</span>  <span class="token comment">-- If something goes wrong</span>
</code></pre>
</li>
</ul>
<h4 id="optimize-large-join-queries-with-indexes">16. <strong>Optimize Large <code>JOIN</code> Queries with Indexes</strong></h4>
<ul>
<li>
<p><strong>Tip</strong>: When joining large tables, ensure the columns involved in the <code>JOIN</code> condition are indexed. This can drastically improve query performance.</p>
</li>
<li>
<p><strong>Example</strong>:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">CREATE</span> <span class="token keyword">INDEX</span> idx_employee_department <span class="token keyword">ON</span> employees<span class="token punctuation">(</span>department_id<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">CREATE</span> <span class="token keyword">INDEX</span> idx_department_id <span class="token keyword">ON</span> departments<span class="token punctuation">(</span>department_id<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="document-your-database-schema">17. <strong>Document Your Database Schema</strong></h4>
<ul>
<li><strong>Tip</strong>: Always document your database schema, relationships, and any important assumptions about your data model. This will make it easier for you and others to maintain and extend the database in the future.</li>
</ul>
<h3 id="summary-10">Summary:</h3>
<p>Chapter 11 offers a range of <strong>SQL tips and tricks</strong> to help you write efficient queries, optimize performance, and manage large datasets effectively. These best practices will help you avoid common pitfalls, ensure data integrity, and work more efficiently with SQL. By following these guidelines, you can improve the performance of your queries, make your database more maintainable, and develop better habits as you work with SQL on a daily basis.</p>

