---
description: Gobuster is a tool used to brute-force URIs, DNS subdomains, and Virtual Hostnames. 
functions:
  fuzzing:
    - description: Fuzzing for Local File Inclusion
      code: |
       gobuster dir -u "http://203.0.113.10/view.php?page=" -w /usr/share/wordlists/lfi_list.txt
  enum-dirs:
    - description: Using `dir` mode, specify wordlist, extensions, and thread count
      code: |
       gobuster dir -u "http://203.0.113.10/files_directory/" -w /usr/share/wordlists/apache_file_list.txt -x php,js,txt -t 18
---
