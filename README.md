# nmap

## Objective

The objective of this project was to practice network reconnaissance by using Nmap from a Kali Linux environment and Zenmap (the Nmap GUI) from a Windows 10 host to scan and enumerate a target. The project demonstrates both command-line and graphical workflows for discovering open ports, identifying running services and versions, and interpreting scan outputs.

### Skills Learned

- Running Nmap scans from Kali Linux
- Using Zenmap GUI on Windows for visualization and profiles
- Performing host discovery and port/service enumeration
- Interpreting and comparing CLI vs GUI scan results
- Documenting and exporting scan findings
- Recognizing how network/firewall settings impact scan results

### Tools Used

- VirtualBox (VM host)
- Kali Linux (VM) — attacker/scanning machine
- Windows 10 (VM) — target machine/attacker
- Nmap (command-line) — network scanner/enumerator
- Zenmap (Windows GUI for Nmap) — profiles, visualization, and GUI scanning
- Virtual network adapters (Host-only / NAT / Bridged) — VM networking configuration used to control visibility
- Terminal (Kali) / Command Prompt (Windows) — running commands and basic network checks

---
<img width="1920" height="1013" alt="Installed NMap" src="https://github.com/user-attachments/assets/d18f1963-7f09-44b2-8423-9dcd20ef15ce" />

Installed Nmap on the Windows 10 VM.

<img width="1920" height="1042" alt="Ran netdiscover command with wireshark running" src="https://github.com/user-attachments/assets/f171a08e-c094-4634-b845-f8907cd3ecb0" />

Ran netdiscover.
Bonus: I had Wireshark running in the background to observe how ARP and other network traffic flowed while discovering hosts.

<img width="1920" height="1039" alt="Ran nmap -sn command on 192-168-56-0--24" src="https://github.com/user-attachments/assets/a5f78d45-d897-4ac8-9d7e-716107ed780b" />

Ran nmap -sn 192.168.56.0/24.
Performed a host discovery (ping/ARP) sweep across the subnet to identify which IPs are live without doing a port scan.

<img width="1920" height="1039" alt="Ran nmap -sV command on 192-168-56-118" src="https://github.com/user-attachments/assets/fe9a467d-c42b-47a7-8369-81ecb4fb776b" />

Ran nmap -sV 192.168.56.118.
Performed service and version detection on the Windows VM to determine which services are running on open ports and attempt to identify their versions.

<img width="1917" height="1039" alt="Ran nmap -O command on 192-168-56-118" src="https://github.com/user-attachments/assets/ce461662-91bf-4741-b19c-44ec1ebe5da4" />

Ran nmap -O 192.168.56.118.
Attempted OS detection to infer the operating system of the target host based on TCP/IP stack fingerprinting.

<img width="1920" height="1036" alt="Using Zenmap" src="https://github.com/user-attachments/assets/c51f4370-f4cb-4709-a118-7125c42e9b68" />

Used Zenmap to practice the GUI side of Nmap.
Created and ran profiles, compared visual output to CLI results.
