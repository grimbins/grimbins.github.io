---
description: |
  Secure Shell (SSH) is a network protocol for securely logging in and executing commands on a remote system. The user must authenticate using credentials or key files. SSH is generally used to access Unix-like operating systems, but it can also be used on Microsoft Windows. Windows 10 uses OpenSSH as its default SSH client and SSH server.
functions:
  shells:
    - description: Generate SSH key
      code: |
       ssh-keygen
       chmod 600 ~/.ssh/id_rsa
    - description: Connect using SSH public key
      code: ssh -i id_rsa user@203.0.113.10
    - description: todo - forwarding / pivoting with ssh
      code: ssh -D remote:local or something like that
---
