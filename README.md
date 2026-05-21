SQL Injection on DVWA (Low Security)

Introduction

SQL Injection is a web application vulnerability where attackers manipulate SQL queries through user input fields to access unauthorized data.

This project demonstrates a basic SQL Injection attack on DVWA (Damn Vulnerable Web Application) with the security level set to Low.

Objective

The objective of this task is to:
- Configure DVWA
- Set DVWA security to Low
- Perform SQL Injection
- Understand how SQL Injection vulnerabilities work

Tools Used

- DVWA
- Kali Linux
- Apache
- MySQL/MariaDB

SQL Injection Payload Used

' OR '1'='1


Explanation of the Attack

The SQL Injection payload modifies the SQL query executed by the application.

Example Vulnerable Query:

SELECT * FROM users WHERE user_id = '$id';

After SQL Injection:

SELECT * FROM users WHERE user_id = '' OR '1'='1';


Since the condition `'1'='1'` is always true, the database returns all available records.

Attack Result

The application displayed multiple user records, proving that the input field was vulnerable to SQL Injection.

Impact of SQL Injection

SQL Injection vulnerabilities may lead to:

* Unauthorized database access
* Data theft
* Authentication bypass
* Exposure of sensitive information
* Full database compromise

Prevention Methods

SQL Injection vulnerabilities can be prevented by:

* Using prepared statements
* Using parameterized queries
* Validating user input
* Escaping special characters
* Applying least privilege access control

Conclusion

This project successfully demonstrated SQL Injection on DVWA with low security settings. The task highlights the importance of secure coding practices and proper input validation in web applications.
