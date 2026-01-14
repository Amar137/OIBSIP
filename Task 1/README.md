# Basic Network Scanning with Nmap

## Objective
To perform a network scan to identify open ports and running services using Nmap.

## Tool Used
- Nmap

## Environment
- Kali Linux
- Local lab network (Private IP range)

## Methodology
- Performed service detection using Nmap
- Identified open TCP ports and associated services
- Analyzed results from a defensive security perspective

## Key Findings
- Multiple Windows-related services were detected
- Services included RPC, NetBIOS, SMB, and an SSL-enabled service
- The system was identified as a Windows host

## Notes
- Scan was conducted on an authorized local lab environment
- No exploitation was performed
- IP addresses were private and non-routable

## Commands Used

```bash
# Update system packages
sudo apt update

# Install Nmap
sudo apt install nmap

# Verify Nmap installation
nmap --version

# Perform a basic scan on a private IP
nmap <Target_IP>

# Perform service and version detection
nmap -sV <Target_IP>
```

## Demo Video
A short demonstration showing how to perform a basic network scan using Nmap:  
https://drive.google.com/file/d/1hsEwRQGzPdI3SL3JCWrQwW4Br_iM5CMX/view?usp=drive_link

## Conclusion
This task demonstrated how Nmap can be used to perform basic network scanning to identify open ports and running services on a target system. The scan was conducted in an authorized local lab environment and provided insight into network reconnaissance from a defensive security perspective.

