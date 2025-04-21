# 📘 DBMS Viva Preparation Guide

## 🔹 Basics of DBMS
- What is DBMS?
- Advantages of DBMS over File System
- Types of DBMS: Hierarchical, Network, Relational, Object-Oriented
- Database vs DBMS vs RDBMS
- ACID Properties (Atomicity, Consistency, Isolation, Durability)

## 🔹 Data Models
- Hierarchical Model
- Network Model
- Relational Model
- ER Model (Entity-Relationship Model)

## 🔹 Entity-Relationship (ER) Model
- Entity, Entity Set
- Attributes: Simple, Composite, Derived, Multivalued
- Relationships and Cardinality (1:1, 1:N, M:N)
- Strong vs Weak Entities
- ER to Relational Mapping

## 🔹 Relational Model
- Tables (Relations), Tuples, Attributes, Domains
- Primary Key, Candidate Key, Super Key, Foreign Key
- Integrity Constraints:
  - Domain Constraint
  - Entity Integrity
  - Referential Integrity

## 🔹 SQL (Structured Query Language)
- DDL Commands: `CREATE`, `ALTER`, `DROP`
- DML Commands: `SELECT`, `INSERT`, `UPDATE`, `DELETE`
- DCL Commands: `GRANT`, `REVOKE`
- TCL Commands: `COMMIT`, `ROLLBACK`, `SAVEPOINT`
- Clauses: `WHERE`, `GROUP BY`, `HAVING`, `ORDER BY`
- Joins: INNER, LEFT, RIGHT, FULL OUTER
- Subqueries and Nested Queries
- Aggregate Functions: `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()`

## 🔹 Normalization
- Need for Normalization
- 1NF, 2NF, 3NF, BCNF
- Functional Dependencies
- Anomalies in Unnormalized Tables (Insertion, Deletion, Update)

## 🔹 Transactions and Concurrency Control
- What is a Transaction?
- States of Transaction: Active, Partially Committed, Failed, Aborted, Committed
- Serializability: Conflict & View
- Concurrency Problems: Lost Update, Dirty Read, Unrepeatable Read
- Concurrency Control Techniques: Lock-based, Timestamp-based

## 🔹 Indexing
- What is Indexing?
- Types of Indexing: Single-level, Multi-level, B+ Tree
- Clustered vs Non-clustered Index

## 🔹 Storage and File Organization
- File Organization: Heap, Sequential, Hashing
- RAID Levels (Basic Idea)

## 🔹 Triggers and Views
- What is a View? How to create it?
- What is a Trigger? When are they used?

## 🔹 PL/SQL (if applicable)
- Structure of PL/SQL Block
- Cursors: Implicit vs Explicit
- Exception Handling

---

## 🔹 Common Viva Questions
- What is the difference between `DELETE`, `TRUNCATE`, and `DROP`?
- How does `GROUP BY` differ from `ORDER BY`?
- What is a foreign key with an example?
- Difference between `WHERE` and `HAVING`?
- What is normalization and why is it needed?
- Explain different types of JOINs with examples.
- How is a deadlock handled in DBMS?

---

> 💡 **Tip:** Always give real-life analogies where possible (like a library database, banking system, etc.) to impress your examiner!
