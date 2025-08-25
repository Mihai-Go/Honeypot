# Python Honeypot

A simple Python script that emulates common network services (FTP, SSH, HTTP, HTTPS) to log and analyze suspicious activity.  
Great for learning Python networking, threading, and basic cybersecurity concepts!

## Features

- Listen on multiple ports simultaneously
- Emulate service banners to trick attackers
- Log all incoming connections and commands in JSON format
- Lightweight and easy to run from the command line

## Usage

Clone the repository:


git clone https://github.com/<your-username>/python-honeypot.git
cd python-honeypot

Run the script:
python3 honeypot.py
Note: Ports below 1024 require root privileges.
To test without sudo, change the ports in honeypot.py to higher numbers (e.g., 2222, 8080, 8443).

Example Output:
[*] Listening on 0.0.0.0:22
[*] Accepted connection from 192.168.1.10:54321

Logs are automatically saved in the honeypot_logs/ directory in JSON format:
JSON:
{
  "timestamp": "2025-08-25T15:30:12.345678",
  "remote_ip": "192.168.1.10",
  "port": 22,
  "data": "SSH-2.0-OpenSSH_7.6p1 Ubuntu-4ubuntu0.3"
}

How It Works

Uses Python’s socket module to listen for incoming connections

Uses threading to handle multiple clients simultaneously

Sends fake banners for FTP, SSH, HTTP, and HTTPS services

Logs all received data with timestamp, IP, and port

Learning Outcomes

Working with Python networking (socket) and multithreading (threading)

File handling and JSON logging

Basic emulation of network services

Understanding honeypot concepts for cybersecurity

Next Steps

Add more service emulations (SMTP, Telnet, etc.)

Rotate log files automatically daily

Add alert notifications for suspicious activity

Build a simple GUI for monitoring connections

Made by Mihai-Go
