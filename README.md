# Scan-_Your-_Local-_Network-_for-_Open_Ports
Used Nmap to scan the local network (TCP SYN scan) and identify active hosts with open ports. Learned basic network reconnaissance, service enumeration, and potential security risks. Optional traffic analysis done using Wireshark.

**Network Reconnaissance using Nmap and Wireshark**

---

## Objective  
Perform network reconnaissance on the local network using Nmap to find open ports and identify running services. Optionally analyze packet capture with Wireshark.

---

## Tools Used  
- [Nmap](https://nmap.org/)  
- [Wireshark](https://www.wireshark.org/) (optional)

---

## Steps Performed  

1. **Find Local IP Range**  
   Used `ip a` command to find the subnet (e.g., `192.168.1.0/24`).

2. **Run TCP SYN Scan with Nmap**  
   ```bash
   nmap -sS 192.168.1.0/24 -oN scan_results.txt
   This scans all devices in the subnet for open TCP ports and saves output to scan_results.txt.

3.Note Down IPs and Open Ports
Example output: Nmap scan report for 192.168.1.1
PORT    STATE SERVICE
22/tcp  open  ssh
80/tcp  open  http
443/tcp open  https

4.Research Common Services

Port 22: SSH (secure remote login)

Port 80: HTTP (web traffic)

Port 443: HTTPS (secure web traffic)

Port 53: DNS (domain name service)

Port 139: NetBIOS/SMB (file sharing)

5.Identify Potential Security Risks

SSH: risk of brute-force attacks

HTTP: unencrypted traffic vulnerabilities

DNS: potential for amplification attacks

SMB: possible exploitation of Windows services

6.Optional Packet Capture Analysis with Wireshark
Captured packets during scan to observe TCP SYN packets and responses.

Scan Results

Please see the file scan_results.txt for the detailed scan output.

Conclusion

This task helped in understanding basic network reconnaissance, identifying open ports and associated services, and recognizing security risks posed by exposed network services.

How to Run On Manjaro

Install Nmap:
sudo pacman -S nmap

Find your subnet:
ip a

Run the scan:
nmap -sS <your_subnet> -oN scan_results.txt

Prepared by Vikas

---

If you want, I can now guide you step-by-step on pushing this to GitHub with commands!
