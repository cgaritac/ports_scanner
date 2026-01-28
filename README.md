# Ports Scanner

A simple TCP port scanner written in Python. It scans all ports (1–65535) on a given IP address and reports which ones are open or closed.

## Features

- Scans all TCP ports from 1 to 65535
- Interactive: prompts for the target IP address
- Uses socket timeouts (0.5 s) for responsive scanning
- Clear output indicating open vs closed ports

## Requirements

- **Python 3.6+**
- No external dependencies (uses only the built-in `socket` module)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/ports_scanner.git
   cd ports_scanner
   ```

2. No package installation is required; the script uses only Python’s standard library.

## Usage

Run the script and enter the target IP when prompted:

```bash
python port_scanner.py
```

Example:

```
Enter the IP address to scan: 127.0.0.1
Port 22 is open
Port 80 is open
Port 443 is open
...
```

**Note:** Scanning many ports can take a long time. Use only on hosts and networks you are authorized to test.

## How It Works

The scanner uses Python’s `socket` module to attempt a TCP connection on each port. For each port it:

1. Creates a TCP socket
2. Sets a 0.5 second timeout
3. Tries to connect to the given IP and port
4. If the connection succeeds (`result == 0`), the port is reported as open; otherwise it is reported as closed

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Author

**Carlos Garita Campos**
