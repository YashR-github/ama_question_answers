# AMA - Question- Answers

## Q1. What is a foreign key?

**Ans:**
A foreign key is a column (or group of columns) in one table that references the primary key (or unique key) of another table to create a relationship between the tables.

---

## Q2. Difference between Ctrl+D, Ctrl+Z, Ctrl+C in Linux?

**Ans:**

| Shortcut | Purpose                          |
| -------- | -------------------------------- |
| `Ctrl+C` | Terminates current process       |
| `Ctrl+Z` | Suspends process temporarily     |
| `Ctrl+D` | Sends EOF / exits terminal input |

---

## Q3. What are the different types of languages inside SQL?

**Ans:**

| Type | Purpose                                         |
| ---- | ----------------------------------------------- |
| DDL  | Defines structure (`CREATE`, `ALTER`, `DROP`)   |
| DML  | Manipulates data (`INSERT`, `UPDATE`, `DELETE`) |
| DQL  | Retrieves data (`SELECT`)                       |
| DCL  | Controls permissions (`GRANT`, `REVOKE`)        |
| TCL  | Manages transactions (`COMMIT`, `ROLLBACK`)     |

---

## Q4. Advantages of linked list over array?

**Ans:**
Below are some of the advantages of linked list over a list:
- Dynamic size allocation
- Faster insertion and deletion
- No need for contiguous memory
- Efficient memory utilization for frequent modifications

---

## Q5. What is indexing in SQL?

**Ans:**
Indexing improves data retrieval speed by allowing faster searching of rows instead of full table scans.

---

## Q6. Does COUNT(*) count NULL values?

**Ans:**
Yes. `COUNT(*)` counts all rows including rows containing NULL values.

---

## Q7. What is a database optimizer?

**Ans:**
A database optimizer chooses the most efficient execution plan for a SQL query.

---

## Q8. How do we connect to PostgreSQL using terminal?

**Ans:**
Using: 
```terminal
sudo -u postgres psql
```

---

## Q9. Difference between DROP, TRUNCATE and DELETE?

| Command  | Removes Data | Removes Structure | WHERE Allowed |
| -------- | ------------ | ----------------- | ------------- |
| DELETE   | Yes          | No                | Yes           |
| TRUNCATE | All rows     | No                | No            |
| DROP     | Entire table | Yes               | No            |

---

## Q10. Find employees starting with 'a' in case-insensitive manner

**Ans:**

```sql id="s3lk0x"
SELECT *
FROM employees
WHERE LOWER(employee_name) LIKE 'a%';
```

---

## Q11. Difference between abstraction and encapsulation

| Abstraction | Encapsulation |
|---|---|
| Abstraction hides implementation details and shows only essential features to the user. | Encapsulation hides internal data and restricts direct access to it. |
| Focuses on **what** an object does. | Focuses on **how** data is protected and managed internally. |
| Helps reduce complexity by exposing only relevant functionality. | Helps achieve data security and controlled access. |
| Achieved using abstract classes and interfaces. | Achieved using access modifiers like `private`, `protected`, and `public`. |
| Example: A user drives a car without knowing the internal engine mechanism. | Example: Private variables in a class accessed using getter/setter methods. |

---

## Q12. Difference between RANK and DENSE_RANK

**Ans:**
`RANK()` skips ranks after ties.
`DENSE_RANK()` does not skip ranks after ties.

Example:

```text id="s1qe7m"
Scores: 100,100,90
RANK: 1,1,3  # skips 2 after tie
DENSE_RANK: 1,1,2   # does not skip 2 after tie
```

---

## Q13. Fastest join in SQL

**Ans:**
Generally `INNER JOIN` is faster because it returns only matching rows and processes less data.

---

## Q14. Difference between candidate key and primary key

**Ans:**
A candidate key is any key that can uniquely identify a row.
A primary key is the candidate key selected as the main unique identifier of the table.
