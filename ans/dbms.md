# 📘 DBMS Viva Preparation Guide - Answers

## 🔹 Basics of DBMS

### Q: What is DBMS?
**A:** A DBMS (Database Management System) is software that allows users to create, retrieve, update, and manage data efficiently in databases.

### Q: Advantages of DBMS over File System
- Reduces data redundancy
- Ensures data consistency
- Better data security
- Easy data access and backup
- Supports multiple users

### Q: Types of DBMS
- **Hierarchical**: Tree-like structure
- **Network**: Graph-like, supports many-to-many
- **Relational**: Uses tables (most popular)
- **Object-Oriented**: Stores objects

### Q: Database vs DBMS vs RDBMS
- **Database**: Organized collection of data
- **DBMS**: Software to manage databases
- **RDBMS**: DBMS based on relational model (tables)

### Q: ACID Properties
- **Atomicity**: All or nothing
- **Consistency**: Valid state before/after transaction
- **Isolation**: Concurrent transactions don’t interfere
- **Durability**: Changes persist after commit

---

## 🔹 Data Models

### Q: Hierarchical Model
**A:** Data is organized like a tree with parent-child relationships.

### Q: Network Model
**A:** More complex; allows many-to-many relationships via graph structure.

### Q: Relational Model
**A:** Represents data using tables (relations).

### Q: ER Model
**A:** Uses entities and relationships to represent data logically.

---

## 🔹 Entity-Relationship (ER) Model

### Q: Entity & Entity Set
- **Entity**: Object with real-world existence
- **Entity Set**: Collection of similar entities

### Q: Attributes
- **Simple**: Cannot be divided (e.g., Age)
- **Composite**: Can be divided (e.g., Name → First, Last)
- **Derived**: Computed (e.g., Age from DOB)
- **Multivalued**: Multiple values (e.g., Phone numbers)

### Q: Relationships and Cardinality
- 1:1, 1:N, M:N defines how many entities relate

### Q: Strong vs Weak Entities
- **Strong**: Has primary key
- **Weak**: Relies on a strong entity

### Q: ER to Relational Mapping
1. Entity → Table
2. Attributes → Columns
3. Relationships → Foreign keys

---

## 🔹 Relational Model

### Q: Terms
- **Table**: Relation
- **Row**: Tuple
- **Column**: Attribute
- **Domain**: Allowed values

### Q: Keys
- **Primary Key**: Uniquely identifies row
- **Candidate Key**: All possible PKs
- **Super Key**: Candidate key + extra
- **Foreign Key**: Links to primary key in another table

### Q: Integrity Constraints
- **Domain**: Values must be valid type
- **Entity Integrity**: PK can't be null
- **Referential Integrity**: FK must match PK

---

## 🔹 SQL (Structured Query Language)

### DDL
- `CREATE TABLE students (id INT, name VARCHAR(50));`
- `ALTER TABLE students ADD age INT;`
- `DROP TABLE students;`

### DML
- `SELECT * FROM students;`
- `INSERT INTO students VALUES (1, 'John');`
- `UPDATE students SET name='Jane' WHERE id=1;`
- `DELETE FROM students WHERE id=1;`

### DCL
- `GRANT SELECT ON students TO user;`
- `REVOKE SELECT ON students FROM user;`

### TCL
- `COMMIT`, `ROLLBACK`, `SAVEPOINT`

### Clauses
- `WHERE`: Filters rows
- `GROUP BY`: Groups rows by column
- `HAVING`: Conditions on groups
- `ORDER BY`: Sorts results

### Joins
- **INNER**: Common rows
- **LEFT**: All from left + matches
- **RIGHT**: All from right + matches
- **FULL OUTER**: All rows with null where no match

### Subqueries and Nested Queries
**A:** A query inside another query
```sql
SELECT name FROM students WHERE id IN (SELECT student_id FROM marks);
```

### Aggregate Functions
- `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()` used for summary

---

## 🔹 Normalization

### Q: Need for Normalization
**A:** Removes redundancy, avoids anomalies, improves integrity

### Forms:
- **1NF**: Atomic values
- **2NF**: No partial dependency (PK)
- **3NF**: No transitive dependency
- **BCNF**: Stronger form of 3NF

### Q: Functional Dependencies
**A:** A → B means B is functionally dependent on A

### Anomalies
- **Insertion**: Can’t add data due to missing fields
- **Deletion**: Removing one causes loss of unrelated data
- **Update**: Multiple rows to update same info

---

## 🔹 Transactions and Concurrency Control

### Q: What is a Transaction?
**A:** A sequence of DB operations that form a logical unit of work.

### States:
- Active → Partially Committed → Committed / Failed → Aborted

### Serializability
- **Conflict**: Order doesn't affect result
- **View**: Same final state and reads

### Concurrency Problems
- **Lost Update**: Overwritten by concurrent update
- **Dirty Read**: Read uncommitted data
- **Unrepeatable Read**: Same query gives different results

### Concurrency Control
- **Lock-based**: Shared/Exclusive locks
- **Timestamp-based**: Based on transaction timestamps

---

## 🔹 Indexing

### Q: What is Indexing?
**A:** Improves retrieval speed using data structures

### Types
- **Single-level**: Simple index table
- **Multi-level**: Tree-structured (better performance)
- **B+ Tree**: Balanced, used in most RDBMS

### Clustered vs Non-clustered
- **Clustered**: Sorts actual table
- **Non-clustered**: Separate index structure

---

## 🔹 Storage and File Organization

### Q: File Organization
- **Heap**: Unordered
- **Sequential**: Sorted
- **Hashing**: Key-based placement

### Q: RAID Levels
- Improves performance and fault tolerance
- E.g., **RAID 0** (striping), **RAID 1** (mirroring), **RAID 5** (parity)

---

## 🔹 Triggers and Views

### Q: View
**A:** Virtual table created using query
```sql
CREATE VIEW high_scores AS SELECT name FROM students WHERE marks > 90;
```

### Q: Trigger
**A:** Procedure that executes automatically on event
```sql
CREATE TRIGGER trg AFTER INSERT ON students FOR EACH ROW BEGIN ... END;
```

---

## 🔹 PL/SQL (if applicable)

### Q: Structure of PL/SQL Block
```sql
DECLARE
  var_name datatype;
BEGIN
  -- statements
EXCEPTION
  -- error handling
END;
```

### Q: Cursors
- **Implicit**: Auto-handled by SQL
- **Explicit**: Declared and managed manually

### Q: Exception Handling
```sql
BEGIN
  -- code
EXCEPTION
  WHEN OTHERS THEN
    DBMS_OUTPUT.PUT_LINE('Error');
END;
```

---

## 🔹 Common Viva Questions

### Q: `DELETE` vs `TRUNCATE` vs `DROP`
- `DELETE`: Removes rows, can rollback
- `TRUNCATE`: Removes all rows, can’t rollback
- `DROP`: Deletes table structure

### Q: `GROUP BY` vs `ORDER BY`
- `GROUP BY`: Group rows
- `ORDER BY`: Sort rows

### Q: Foreign Key Example
```sql
FOREIGN KEY (dept_id) REFERENCES departments(id);
```

### Q: `WHERE` vs `HAVING`
- `WHERE`: Before grouping
- `HAVING`: After grouping

### Q: Normalization
**A:** Process of structuring data to minimize redundancy and dependency

### Q: Types of JOINs
```sql
SELECT * FROM A INNER JOIN B ON A.id = B.id;
```
- Explained in joins section

### Q: Deadlock Handling
- Timeout
- Wait-Die / Wound-Wait protocols
- Deadlock Detection and Recovery

---

> 💡 **Tip:** Use examples like student-course database or ATM transaction system to explain answers better!

