# Python Honeypot

A simple multi-threaded honeypot written in Python designed to detect and log suspicious network activity.  
Great for learning about cybersecurity, socket programming, and threat intelligence!

## Features

- Listens on common ports (21/FTP, 22/SSH, 80/HTTP, 443/HTTPS) by default
- Emulates real service banners to attract attackers
- Logs all connection attempts and received data with timestamps
- Saves detailed activity logs in JSON format for easy analysis
- Multi-threaded to handle multiple connections simultaneously

## Usage

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/python-honeypot.git
    cd python-honeypot
    ```
    
2.  **Run the script (requires Python 3):**

    ```bash
    python3 honeypot.py
    ```

3.  **The honeypot will start listening. Stop it at any time with `CTRL + C`.**

## Example Output
[] Listening on 0.0.0.0:22
[] Listening on 0.0.0.0:80
[*] Accepted connection from 192.168.1.15:45562
[!] Error handling connection from 203.0.113.5:443 - [WinError 10054] An existing connection was forcibly closed by the remote host

Logs are saved in the `honeypot_logs/` directory as JSON files.

---

### How It Works

- Uses Python's `socket` and `threading` modules to create multi-threaded listeners on specified ports.
- When a connection is received, it sends a realistic service banner (e.g., mimics an SSH server).
- All data sent by the client is captured and logged to a JSON file with a timestamp, source IP, and port.
- The connection is kept open to gather more data and waste the attacker's time.

## Learning Outcomes

- Working with Python's `socket` library for network communication
- Multi-threading for handling concurrent connections
- Logging and data serialization using the `json` module
- Basics of cybersecurity monitoring and deception

## Next Steps

- Add support for custom port configurations via command-line arguments
- Implement email or SMS alerts for new connections
- Extend service emulation to interact more realistically with attackers
- Create a dashboard to visualize attack data from the log files

---

**Made by Mihai-Go**
