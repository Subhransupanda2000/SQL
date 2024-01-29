# ACID PROPERTIES
ACID properties are a set of characteristics that ensure the reliability and consistency of transactions in a database system. These properties are essential for maintaining the integrity of data and ensuring that transactions are processed reliably, even in the face of system failures. The term "ACID" stands for:
* Atomicity:

Definition: Atomicity ensures that a transaction is treated as a single, indivisible unit of work.
Characteristic: Either all the operations within a transaction are executed, or none of them are. If any part of the transaction fails, the entire transaction is rolled back to its previous state (undo operation).
* Consistency:

Definition: Consistency ensures that a transaction brings the database from one valid state to another.
Characteristic: The database must remain in a consistent state before and after the transaction. If a transaction violates any integrity constraints, it is rolled back.
* Isolation:

Definition: Isolation ensures that the execution of one transaction is isolated from the execution of other transactions.
Characteristic: Even though multiple transactions may be executing concurrently, each transaction should appear as if it is the only transaction being executed. This prevents interference or data corruption caused by concurrent transactions.
* Durability:

Definition: Durability guarantees that once a transaction is committed, its effects are permanent, and they survive any subsequent system failures.
Characteristic: Once the database system acknowledges the successful completion of a transaction (commit), the changes made by that transaction are stored permanently and will not be lost, even in the event of a power failure, system crash, or other catastrophic events.
