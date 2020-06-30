---
description: |
  MSFvenom is a combination of Msfpayload and Msfencode, used to generate and output all of the various types of shell code that are available in Metasploit.
functions:
  obfuscation:
    - description: Encode and Decode string
      code: |
       echo -n "ping /n 1 198.51.100.2" | base64
       > cGluZyAvbiAxIDE5Mi4wLjIuMg==
       echo -n "cGluZyAvbiAxIDE5Mi4wLjIuMg==" | base64 -d
       > ping /n 1 198.51.100.2
    - description: Execute encoded Powershell command
      code: |
       echo -n "ping /n 1 198.51.100.2" | base64
       > cGluZyAvbiAxIDE5Mi4wLjIuMg==
       PS C:\> powershell.exe -ec cGluZyAvbiAxIDE5Mi4wLjIuMg==
---
