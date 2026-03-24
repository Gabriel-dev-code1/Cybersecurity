📌 Overview

This lab demonstrates the exploitation of a SQL Injection vulnerability to retrieve hidden data from the application.

The vulnerability allows manipulation of the backend SQL query, enabling access to unintended data.

🎯 Objective
- Identify a vulnerable parameter
- Manipulate the SQL query
- Retrieve hidden data from the database

🛠️ Tools Used
- Burp Suite (Proxy & Repeater)
- Web Browser (Chrome)


🔍 Steps Performed

1. Normal Application Behavior

The application initially displays filtered results based on a selected category.

This represents the normal behavior before any manipulation.

2. Intercepting and Modifying the Request

The request was intercepted using Burp Suite and the parameter was modified to inject a SQL payload.

Example payload used:

' OR 1=1--

This payload forces the query to return all records.

3. Exploiting the Vulnerability

After sending the modified request, the application returned additional data that should not be accessible.

This confirms that the input is not properly sanitized.

4. Lab Successfully Completed

The lab environment confirms that the SQL Injection was successfully executed.

⚠️ Vulnerability Explanation

SQL Injection occurs when:

User input is directly included in SQL queries
No proper validation or sanitization is applied

Attackers can manipulate queries to:
- Bypass filters
- Access unauthorized data
- Modify or delete database contents

🔒 Mitigation
Use prepared statements (parameterized queries)
Implement input validation
Apply least privilege to database users
Use ORM frameworks when possible

📚 Key Takeaways
Even simple payloads can break query logic
Input validation is critical for database security
Burp Suite is effective for testing and exploitation

📸 Screenshots Description
