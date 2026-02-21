What is SQL Injection (SQLi)?

SQL Injection is a security vulnerability where an attacker injects malicious SQL code into user input (like forms, URLs, or login fields).

Because the application trusts the input blindly, the attacker can:

Read sensitive data (users, passwords, credit cards)

Modify or delete data

Bypass login (become admin)

Sometimes take full control of the database/server

👉 Root cause:
User input is directly added to SQL queries without proper protection.

Simple Example (Easy to Understand)
Normal Query
SELECT * FROM users WHERE user_id = '1';

Vulnerable Code
$id = $_GET['id'];
$query = "SELECT * FROM users WHERE user_id = '$id'";

Attacker Input
1' OR '1'='1

Final Query Becomes
SELECT * FROM users WHERE user_id = '1' OR '1'='1';


✅ '1'='1' is always true, so all users are returned.

Real-World Impact (Why It’s Dangerous)

Capital One breach (2019)
Over 100 million customers’ data leaked

Personal info, addresses, SSN, credit scores exposed

Massive financial loss + reputation damage

SQL Injection Security Levels (DVWA Example)
1️⃣ Low Security (Very Dangerous)

What happens

User input is directly placed into the query

No validation, no filtering

$id = $_GET['id'];
$query = "SELECT first_name FROM users WHERE user_id = '$id'";


Attacks

' → causes SQL error (reveals DB info)

1 OR 1=1 → returns all users

UNION SELECT user, password FROM users-- → leaks credentials

❌ Worst case scenario

2️⃣ Medium Security (Weak Protection)

What happens

Uses addslashes() to escape '

$id = addslashes($_GET['id']);


Why still vulnerable

Numeric input doesn’t need quotes

Attack still works

1 OR 1=1


⚠️ Partial protection only

3️⃣ High Security (Safe Way ✅)

Uses Prepared Statements

$stmt = $pdo->prepare(
  "SELECT first_name FROM users WHERE user_id = ?"
);
$stmt->execute([$id]);


Why it’s safe

SQL logic and data are separated

Input is treated as data only, not code

❌ Attacks like OR 1=1, ', UNION do not work

✅ Best practice

Types of SQL Injection (Very Important)
🔴 1. Error-Based SQL Injection

Idea:
Force the database to throw an error → error reveals information

Example Input

'


Result

SQL syntax error shown

Error reveals:

Database type (MySQL, Oracle, etc.)

Table/column names

Query structure

👉 Used when error messages are visible

🔵 2. Union-Based SQL Injection

Idea:
Use UNION to fetch data from another table

Conditions

Same number of columns

Compatible data types

Steps

Find number of columns:

1 ORDER BY 1
1 ORDER BY 2
1 ORDER BY 3


Error at ORDER BY 4 → means 3 columns

Extract data:

1 UNION SELECT user, password, NULL FROM users--


👉 Direct data extraction

🟠 3. Blind SQL Injection

Used when

No error messages

No data shown

Two Types

a) Boolean-Based
' AND 1=1 --


Page loads normally → True

' AND 1=2 --


Page behaves differently → False

b) Time-Based
' AND IF(1=1, SLEEP(5), 0) --


If page delays → condition is true

👉 Data extracted bit by bit, very slow but powerful

Impact of SQL Injection

🔓 Unauthorized data access

🗑️ Data deletion or modification

👑 Admin privilege escalation

🚫 Application crash or downtime

💔 Loss of user trust & legal trouble

How to Prevent SQL Injection (Exam + Interview Gold ⭐)
✅ 1. Prepared Statements (MOST IMPORTANT)
$stmt = $conn->prepare(
  "SELECT * FROM users WHERE username = ?"
);

✅ 2. Stored Procedures

Predefined queries

Avoid dynamic SQL

✅ 3. Input Validation (Whitelist)

Allow only expected formats

Example: numbers only for IDs

✅ 4. Use ORM Frameworks

Hibernate, Sequelize, Entity Framework

Automatically handle queries safely

✅ 5. Least Privilege Principle

App should NOT have DROP, ALTER permissions

✅ 6. Proper Error Handling

Don’t show DB errors to users

Log internally, show generic messages

One-Line Summary (Perfect for Viva)

SQL Injection occurs when untrusted user input is directly embedded into SQL queries, allowing attackers to manipulate the database. It is prevented using prepared statements and proper input validation.

