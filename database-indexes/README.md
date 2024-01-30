# Database-indexes
*  An index is a data structure that provides a quick and efficient way to look up records in a database table. The primary purpose of an index is to enhance the speed of data retrieval operations, making queries run more efficiently. Here's a comprehensive explanation of database indexes.
# Index Structure:
*  B-Tree:
* The most common type of index structure is the B-tree (Balanced Tree), which is well-suited for range queries and equality searches. B-trees maintain sorted data and provide efficient insertion, deletion, and search operations.
* Hash Index:
* Some databases use hash indexes, which are suitable for equality searches but not for range queries. Hash indexes use a hash function to map keys to index entries.
* Indexed Columns:
* Indexes are created on one or more columns of a table. The choice of columns depends on the types of queries frequently executed. Columns used in WHERE clauses, JOIN conditions, or ORDER BY clauses are good candidates for indexing.
# Index Types:
* Primary Index:
*  The primary index is created on the primary key of a table, ensuring that each row in the table is uniquely identified. It is typically implemented as a clustered index, determining the physical order of data.
* Unique Index:
* A unique index ensures that the indexed columns contain unique values. It is often used to enforce uniqueness constraints on specific columns.
* Composite Index:
*  An index created on multiple columns. It is useful for queries that involve conditions on multiple columns.
*  Trade-Offs:
* While indexes significantly improve query performance, they come with trade-offs. Indexes consume disk space, and their maintenance can impact the performance of insert, update, and delete operations. Striking a balance between the benefits of faster retrieval and the overhead of maintaining indexes is crucial.
* Query Performance:
* Indexes can dramatically improve the speed of SELECT queries by allowing the database engine to locate and retrieve relevant rows more quickly. However, their impact on query performance varies based on the specific query and data distribution.
# Clustered vs. Non-Clustered Index:
In some database systems, indexes can be categorized as clustered or non-clustered. A clustered index determines the physical order of data in the table, while a non-clustered index stores a separate structure pointing to the actual data.
* Query Optimization:
* The query planner of a database engine uses indexes to optimize query execution plans. It decides whether to perform a full table scan or use indexes based on factors like cardinality, selectivity, and cost estimation.
* Updating and Deleting Data:
* When data is updated or deleted, corresponding indexes need to be updated, which can introduce overhead. Bulk operations may benefit from temporarily disabling indexes and rebuilding them afterward.
```
-- Create employees table
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    email VARCHAR(255),
    department VARCHAR(100),
    salary DECIMAL(10, 2)
);

-- Insert sample data
INSERT INTO employees VALUES
    (1, 'John@ Doe', 'IT', 75000.00),
    (2, 'Jane@ Smith', 'HR', 60000.00),
    (3, 'Bob J@ohnson', 'Finance', 80000.00),
    (4, 'Alice@ Brown', 'IT', 70000.00),
    (5, 'Charlie@ Davis', 'Sales', 90000.00);

```
```
-- Create an index on the 'email' column
CREATE INDEX idx_email ON employees(department);

```






