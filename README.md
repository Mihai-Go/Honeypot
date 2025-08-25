PYTHON HONEYPOT

A simple Python script that emulates common network services (FTP, SSH, HTTP, HTTPS) and logs all incoming connections.
Great for learning Python networking, threading, and basic cybersecurity concepts.

FEATURES
Listen on multiple ports at the same time
Emulate realistic service banners to trick attackers
Log all incoming traffic in JSON format for easy analysis
Lightweight and easy to run from the command line
Handles multiple connections simultaneously using threads
Automatically creates daily log files

USAGE
1. Clone the repository:
git clone https://github.com/<your-username>/python-honeypot.git
cd python-honeypot

2. Run the script:
python3 honeypot.py

Note: Ports below 1024 require root privileges. To test without sudo, change the ports in honeypot.py to higher numbers (e.g., 2222, 8080, 8443).

Example output:
[*] Listening on 0.0.0.0:22
[*] Accepted connection from 192.168.1.10:54321

Logs are saved in the honeypot_logs folder in JSON format, for example:
{ "timestamp": "2025-08-25T15:30:12.345678", "remote_ip": "192.168.1.10", "port": 22, "data": "SSH-2.0-OpenSSH_7.6p1 Ubuntu-4ubuntu0.3" }

HOW IT WORKS
Uses Python’s socket module to listen for incoming connections
Uses threads to handle multiple clients simultaneously
Sends fake banners for FTP, SSH, HTTP, and HTTPS services
Logs every command or handshake attempt with timestamp, IP, and port
Easily extensible for additional services

LEARNING OUTCOMES
Understand Python networking and socket programming
Learn multithreading and concurrency
Practice logging and analyzing network data in JSON
Gain insight into honeypot design and cybersecurity concepts
Improve file handling, exception handling, and debugging skills

NEXT STEPS
Add support for more protocols (SMTP, Telnet, MySQL)
Implement automatic log rotation and archiving
Add real-time alerts for suspicious activity
Build a simple GUI for monitoring connections
Make service responses more realistic
Integrate with analytics tools to visualize traffic patterns

MADE BY MIHAI-GO
