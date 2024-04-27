# Deny-Ports

## Description
This script is designed to deny a list of specified port/protocol pairs using UFW (Uncomplicated Firewall). It iterates through an array of port/protocol pairs and denies each one individually, then reloads UFW to apply the changes and displays the updated rules.

## Usage
1. Ensure you have UFW installed and configured on your system.
2. Copy the script content into a file (e.g., `deny_ports.sh`) on your system.
3. Make the script executable using `chmod +x deny_ports.sh`.
4. Run the script using `./deny_ports.sh`.
5. After running the script, enable any desired network port using UFW commands.

## How to enable a desired network port?

To enable any desired network port after running the script, you can use the following command:
```
sudo ufw allow <port>/<protocol>
```

For example, to allow incoming connections on port 8080/tcp after running the denial script, execute:
```
sudo ufw allow 8080/tcp
```

Remember to reload UFW after making changes to apply the new rules:
```
sudo ufw reload
```

## Port/Protocol Pairs
- "22/tcp"    # SSH (Secure Shell)
- "22/udp"    # SSH (Secure Shell)
- "5800/tcp"  # VNC (Virtual Network Computing)
- "5800/udp"  # VNC (Virtual Network Computing)
- "5900/tcp"  # VNC (Virtual Network Computing)
- "5900/udp"  # VNC (Virtual Network Computing)
- "20/tcp"    # FTP (File Transfer Protocol) - Data
- "20/udp"    # FTP (File Transfer Protocol) - Data
- "21/tcp"    # FTP (File Transfer Protocol) - Control
- "21/udp"    # FTP (File Transfer Protocol) - Control
- "137/tcp"   # NetBIOS Name Service
- "137/udp"   # NetBIOS Name Service
- "138/tcp"   # NetBIOS Datagram Service
- "138/udp"   # NetBIOS Datagram Service
- "139/tcp"   # NetBIOS Session Service
- "139/udp"   # NetBIOS Session Service
- "445/tcp"   # Microsoft-DS (Microsoft Directory Services)
- "445/udp"   # Microsoft-DS (Microsoft Directory Services)
- "3389/tcp"  # RDP (Remote Desktop Protocol)
- "3389/udp"  # RDP (Remote Desktop Protocol)
- "23/tcp"    # Telnet
- "23/udp"    # Telnet
- "1900/tcp"  # UPnP (Universal Plug and Play)
- "1900/udp"  # UPnP (Universal Plug and Play)
- "80/tcp"    # HTTP (Hypertext Transfer Protocol)
- "80/udp"    # HTTP (Hypertext Transfer Protocol)
- "25/tcp"    # SMTP (Simple Mail Transfer Protocol)
- "143/tcp"   # IMAP (Internet Message Access Protocol)
- "993/tcp"   # IMAPS (IMAP Secure)
- "110/tcp"   # POP3 (Post Office Protocol - Version 3)
- "995/tcp"   # POP3S (POP3 Secure)
- "990/tcp"   # FTPS (File Transfer Protocol Secure)
- "389/tcp"   # LDAP (Lightweight Directory Access Protocol)
- "636/tcp"   # LDAPS (LDAP Secure)
- "3306/tcp"  # MySQL Database
- "5432/tcp"  # PostgreSQL Database
- "514/udp"   # Syslog
- "6881-6889/tcp"  # BitTorrent
- "161/udp"   # SNMP (Simple Network Management Protocol)
- "162/udp"   # SNMP Trap
- "179/tcp"   # BGP (Border Gateway Protocol)
- "465/tcp"   # SMTPS (SMTP Secure)
- "587/tcp"   # Submission (Mail Message Submission)
- "873/tcp"   # Rsync
- "1433/tcp"  # Microsoft SQL Server
- "1521/tcp"  # Oracle Database
- "2049/tcp"  # NFS (Network File System)
- "5901/tcp"  # VNC - Alternate port
- "8080/tcp"  # HTTP Alternate
- "8443/tcp"  # HTTPS Alternate

## Note
- This script requires superuser privileges to run as it utilizes `sudo` to interact with UFW.
- Review and customize the list of port/protocol pairs according to your specific firewall requirements before running the script.

## Disclaimer
Use this script responsibly and ensure that denying these ports aligns with your security policies and requirements. Misconfiguration may result in unintended consequences or loss of network connectivity.

