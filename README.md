Basic Network Scanning with Nmap

Project Overview

This project demonstrates basic network scanning using Nmap on a local Ubuntu virtual machine. The objective is to identify open ports, detect running services, perform OS detection, and analyze potential security risks.

Tools Used

- Ubuntu Linux
- Nmap 7.94SVN
- Oracle VirtualBox

Objective

To understand network reconnaissance and identify exposed services on a system in an authorized lab environment.

Scanning Activities

1. Basic Network Scan

nmap 10.124.173.210

2. Service Version Detection

nmap -sV 10.124.173.210

3. OS Detection

sudo nmap -O 10.124.173.210

4. Save Scan Results

sudo nmap -sV -O 10.124.173.210 -oN nmap_scan_results.txt

Scan Findings

Port| Service| Version / Details| Status
22/tcp| SSH| OpenSSH 9.6p1| Open
443/tcp| HTTPS| SSL/HTTPS| Open

OS detection estimated the target as a Linux system. The Linux 2.6.X fingerprint is an estimate, not a confirmed kernel version.

Security Analysis

Port 22 – SSH

- Purpose: Secure remote administration.
- Potential risk: Weak passwords and unauthorized login attempts.
- Recommendation: Use SSH keys and restrict remote access.

Port 443 – HTTPS

- Purpose: Secure web communication.
- Potential risk: Weak TLS configuration or invalid certificates.
- Recommendation: Use modern TLS settings and valid certificates.

Key Learnings

- Installed and used Nmap.
- Identified open and closed ports.
- Detected running services and versions.
- Performed OS fingerprinting.
- Saved scan results.
- Learned basic network security analysis.

Ethical Considerations

This scan was performed on my own local virtual machine for educational purposes. Network scanning should only be performed on systems you own or have explicit permission to test.

Conclusion

This project provided practical experience in network reconnaissance, port identification, service detection, and basic security analysis using Nmap.
