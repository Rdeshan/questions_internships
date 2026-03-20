| Code | Name        | Meaning / When it happens                                   |
|------|-------------|------------------------------------------------------------ |
| 104  | ECONNRESET  | Connection reset by peer (remote closed abruptly)           |
| 110  | ETIMEDOUT   | Connection timed out (no response)                          |
| 111  | ECONNREFUSED| Connection refused (port closed or server not running)      |
| 32   | EPIPE       | Broken pipe (writing to a connection that was closed)       |
| 13   | EACCES      | Permission denied (trying to access file or port without permission) |
| 98   | EADDRINUSE  | Address already in use (port already taken)                 |
| 101  | ENETUNREACH | Network unreachable (no route to host)                      |
| 113  | EHOSTUNREACH| Host unreachable (remote server cannot be contacted)        |


Codes 104, 110, 111, 32 → usually network/socket connection issues
Codes 13, 98 → usually permissions or resource conflicts
Codes 101, 113 → usually network routing or host availability problems


1. 104 — ECONNRESET

Meaning: Connection reset by peer.
When it happens: The remote side of a TCP connection (server or client) closed the connection unexpectedly while you were still trying to read or write data.
Example: You are downloading a file from a server, and the server crashes or forcibly closes the connection mid-transfer.

2. 110 — ETIMEDOUT

Meaning: Connection timed out.
When it happens: Your system tried to reach a remote host, but didn’t get a response in time.
Example: You try to ping a server or make an HTTP request, but the server is down or the network is slow.

3. 111 — ECONNREFUSED

Meaning: Connection refused.
When it happens: There’s nothing listening on the port you’re trying to connect to, or a firewall is blocking it.
Example: You try to connect to a web server on port 8080, but the server is not running or port 8080 is closed.

4. 32 — EPIPE

Meaning: Broken pipe.
When it happens: Your program is trying to write to a connection that has already been closed by the other side.
Example: You send data to a socket after the server has disconnected.

5. 13 — EACCES

Meaning: Permission denied.
When it happens: You don’t have permission to access a file, directory, or port.
Example: Trying to bind a web server to port 80 without root privileges, or trying to read a protected file.

6. 98 — EADDRINUSE

Meaning: Address already in use.
When it happens: You try to bind to a port that is already being used by another process.
Example: Starting a second web server on port 3000 when one is already running there.

7. 101 — ENETUNREACH

Meaning: Network unreachable.
When it happens: Your machine cannot reach the remote network, often due to no valid route or disconnected network.
Example: Trying to access a server on a private network while your computer is offline.

8. 113 — EHOSTUNREACH

Meaning: Host unreachable.
When it happens: Your machine can reach the network but cannot contact the specific host.
Example: The server’s IP exists on the network but is down or blocked by a firewall.


