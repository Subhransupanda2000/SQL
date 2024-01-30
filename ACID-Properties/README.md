# ACID PROPERTIES
* the term "ACID" refers to a set of properties that guarantee the reliability and consistency of transactions. ACID stands for Atomicity, Consistency, Isolation, and Durability. These properties ensure that database transactions are executed reliably in a way that maintains the integrity of the data. Let's explore each of the ACID properties:
# Atomicity:
Atomicity ensures that a transaction is treated as a single, indivisible unit of work. Either all the changes made by a transaction are committed to the database, or none of them are. If any part of the transaction fails, the entire transaction is rolled back to its initial state, ensuring that the database remains in a consistent state.
# Consistency:
Consistency ensures that a database remains in a valid state before and after the execution of a transaction. The transaction should adhere to the predefined rules and constraints of the database, preserving the integrity of the data. If a transaction violates any integrity constraints, the entire transaction is rolled back.
#  To ensure Consistency in a Database we should follow the below concepts.
* Define and Enforce Integrity Constraints
* Transaction Management
* Isolation Levels
* Concurrency Control
* Avoid Anomalies
* Data Validation
* Use Stored Procedures and Triggers
* Logging and Auditing
* Regular Maintenance and Monitoring
* Testing and Quality Assurance
# Isolation:
* Isolation ensures that the concurrent execution of multiple transactions does not result in interference or inconsistency. Each transaction should appear as if it is executed in isolation, without being affected by other concurrent transactions. Isolation is typically achieved through mechanisms like locks and isolation levels, preventing transactions from seeing intermediate or uncommitted changes made by other transactions.
#  Problems that arise due to lack of isolation in a database:
* Dirty Read
* Non-Repeatable Read
* Phantom Read
* Lost Update
* Concurrency Anomalies
* Inconsistent Aggregates
* Uncommitted Data Exposure
* Ineffective Locking
# To avoid the above problems we can implement isolation levels in our database.
* Isolation Levels :
* Read Uncommitted: Allows transactions to read uncommitted changes made by other transactions.
* Read Committed: Ensures that a transaction sees only committed changes made by other transactions.
* Repeatable Read: Guarantees that if a transaction reads a value, it will see the same value throughout the transaction, even if other transactions update the data.
* Serializable: Provides the highest level of isolation, ensuring that the results of concurrent transactions are as if they had executed serially.
# Durability:
* Durability guarantees that once a transaction is committed, its effects are permanent and survive any subsequent failures, such as power outages or system crashes. Committed changes are stored in non-volatile storage, ensuring that they persist even if the system restarts. This property ensures the long-term reliability and recoverability of data.
The ACID properties provide a framework for designing and implementing transactional systems, ensuring that database transactions maintain data integrity and consistency. ACID compliance is crucial in scenarios where data accuracy, reliability, and consistency are paramount, such as in financial systems, e-commerce platforms, and other mission-critical applications.

It's worth noting that while ACID properties offer strong guarantees, they can come at the cost of performance, especially in highly concurrent systems. In some cases, there may be trade-offs between ACID compliance and performance, leading to the consideration of alternative consistency models like BASE (Basically Available, Soft state, Eventually consistent) for certain distributed systems.
