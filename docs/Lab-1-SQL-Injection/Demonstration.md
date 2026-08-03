# 📋 Demonstration Guide – Forensic Investigation of a SQL Injection Attack

This guide demonstrates how SQL Injection vulnerabilities can affect a web application by manipulating backend database queries. Participants will observe the application's behavior, understand what happens behind the scenes, and learn how secure coding practices prevent such attacks.

---

# 🎯 Objective

The objective of this demonstration is to understand how SQL Injection modifies SQL queries, observe its impact on a vulnerable web application, and recognize the importance of proper input validation.

> **⚠️ Educational Notice**
>
> This demonstration is performed using **DVWA (Damn Vulnerable Web Application)**, an intentionally vulnerable application designed for cybersecurity education. Never perform SQL Injection testing on systems without explicit authorization.

---

# Step 1 – Launch DVWA

## Instructions

1. Start **Apache** and **MySQL** from the XAMPP Control Panel.
2. Open your preferred web browser.
3. Navigate to:

```
http://localhost/dvwa
```

4. Log in using your DVWA credentials.

<img width="788" height="356" alt="image" src="https://github.com/user-attachments/assets/727c2049-bd9a-4056-b058-7356af8a8c19" />

### Explanation

DVWA is an intentionally vulnerable web application used to safely demonstrate common web application vulnerabilities in a controlled environment.

### Expected Result

The DVWA dashboard opens successfully.

---

# Step 2 – Configure the Security Level

## Instructions

1. Click **DVWA Security** from the left navigation menu.
2. Set the Security Level to:

```
Low
```

3. Click **Submit**.

<img width="791" height="355" alt="image" src="https://github.com/user-attachments/assets/02dc22f0-6753-4b9a-800c-21d36a8a938e" />


### Explanation

The **Low** security setting disables input validation and other security controls, allowing SQL Injection vulnerabilities to be demonstrated for educational purposes.

### Expected Result

The security level is updated successfully.

---

# Step 3 – Open the SQL Injection Module

## Instructions

1. Click **SQL Injection** from the left navigation menu.

<img width="788" height="356" alt="image" src="https://github.com/user-attachments/assets/e41eda20-5e82-4c46-b4e9-33be37bc9344" />


### Explanation

This module contains a vulnerable input field that interacts directly with the backend database.

### Expected Result

The SQL Injection page opens successfully.

---

# Step 4 – Perform the SQL Injection Demonstration

## Instructions

In the **User ID** field, enter the following value:

```
1' OR '1'='1
```

Click **Submit**.

<img width="787" height="358" alt="image" src="https://github.com/user-attachments/assets/9eeb4df2-a228-4f63-9d9d-1bd205d55ff6" />


### What Happens in the Backend?

The application constructs the following SQL query:

```sql
SELECT first_name, last_name
FROM users
WHERE user_id = '1' OR '1'='1';
```

The injected condition:

```sql
'1'='1'
```

always evaluates to **TRUE**.

As a result, the SQL query effectively becomes:

```
WHERE TRUE
```

Instead of returning only one user's information, the database returns every record stored in the `users` table.

---

### Behind the Scenes

```
                User Input
                     │
                     ▼
             1' OR '1'='1
                     │
                     ▼
    Application inserts the input directly
        into the SQL query without validation
                     │
                     ▼
SELECT first_name, last_name
FROM users
WHERE user_id='1'
OR '1'='1'
                     │
                     ▼
      Condition always evaluates TRUE
                     │
                     ▼
     Database returns all user records
                     │
                     ▼
   Multiple user records displayed
```

### Explanation

The vulnerability exists because the application directly concatenates user input into the SQL query without validating or sanitizing it. Instead of treating the input as plain text, the database interprets part of it as executable SQL code, allowing the original query to be modified.

### Expected Result

Multiple user records are displayed instead of a single user's information.

---

# Step 5 – Recommended Mitigation Techniques

## Explanation

SQL Injection vulnerabilities can be prevented by implementing secure coding practices such as:

- Prepared Statements (Parameterized Queries)
- Input Validation
- Stored Procedures
- Least Privilege Database Accounts
- Web Application Firewalls (WAF)

Instead of writing:

```sql
SELECT * FROM users
WHERE user_id = '$id';
```

Developers should use parameterized queries.

Example (PHP PDO):

```php
$stmt = $pdo->prepare("SELECT first_name, last_name FROM users WHERE user_id = ?");
$stmt->execute([$id]);
```

Prepared statements ensure that user input is always treated as **data**, preventing it from being interpreted as executable SQL code.



### Expected Result

Participants understand how secure coding practices eliminate SQL Injection vulnerabilities.

---

# 📝 Summary

In this demonstration, you successfully:

- Configured DVWA for SQL Injection testing
- Executed a SQL Injection attack in a controlled laboratory environment
- Observed how user input modifies backend SQL queries
- Understood why the application returned multiple records
- Learned how developers can prevent SQL Injection using secure coding practices

---

# 🎓 Learning Outcome

After completing this demonstration, participants should be able to:

- Explain how SQL Injection vulnerabilities occur
- Understand how insecure SQL queries are manipulated
- Interpret the backend SQL query executed by the application
- Recognize the risks associated with improper input validation
- Recommend industry-standard mitigation techniques to prevent SQL Injection
