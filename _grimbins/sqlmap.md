---
description: sqlmap automates the process of detecting and exploiting SQL injection flaws and taking over of database servers.
functions:
  sql-injection:
    - description: Testing if paramater `name` is injectable
      code: |
       python sqlmap -u "https://203.0.113.10/get_user.php?id=0&lang=en&name=*"
    - description: Using a saved request intercepted by Burp Suite
      code: |
       python sqlmap -r /get_user.req -p "name"
---
