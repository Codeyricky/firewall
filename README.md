# firewall
simple linux firewall 
# Firewall with Server-Client Communication

This project implements a basic firewall using `iptables` rules and provides a simple client-server communication system using sockets in C.

## Features

- Firewall with options to ACCEPT, REJECT, or DROP packets based on IP address or port number.
- Uses `iptables` for network packet filtering.
- Password-protected rule flushing for security.
- Reads port information from a file.
- Simple TCP server and client for testing network communication.

## Prerequisites

Ensure you have the following installed on your system:

- GCC compiler (`gcc`)
- `iptables` (for firewall rules)
- Linux-based OS (tested on Ubuntu)

## Installation and Usage

### Firewall Setup

1. Clone the repository:
   ```sh
   git clone https://github.com/Codeyricky/firewall.git
   cd firewall_project
   ```
2. Compile the firewall code:
   ```sh
   gcc -o firewall firewall.c
   ```
3. Run the firewall:
   ```sh
   sudo ./firewall
   ```

### Server Setup

1. Compile the server code:
   ```sh
   gcc -o server server.c
   ```
2. Run the server on a specific port:
   ```sh
   ./server 8080
   ```

### Client Setup

1. Compile the client code:
   ```sh
   gcc -o client client.c
   ```
2. Run the client and connect to the server:
   ```sh
   ./client 127.0.0.1 8080
   ```
3. Enter a message to send to the server.

## File Descriptions

- `firewall.c`: Contains the main firewall implementation using `iptables`.
- `server.c`: Implements a basic TCP server.
- `client.c`: Implements a TCP client to communicate with the server.
- `shell.sh`: A script generated dynamically to execute `iptables` commands.
- `ipadd.txt`: Stores IP addresses mapped to different websites.

## Security Notes

- Ensure you have administrative privileges (`sudo`) to manipulate firewall rules.
- Use the correct password to flush `iptables` rules.
- Modify `ipadd.txt` carefully as it contains IP address mappings.

## Future Enhancements

- Implement logging for firewall rule changes.
- Add support for a configuration file instead of hardcoded rules.
- Introduce a GUI for easier firewall rule management.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contributions

Feel free to fork the repository and submit pull requests with improvements or fixes.

## Author

Codeyricky

