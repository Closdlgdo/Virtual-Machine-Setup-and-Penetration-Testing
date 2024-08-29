Virtual Machine Setup and Penetration Testing

This project simulates a real-world penetration testing scenario by setting up a Windows 11 virtual machine (VM) and conducting penetration testing using Kali Linux. The goal is to identify vulnerabilities and explore cybersecurity practices.

Overview
Objective: Simulate a penetration test on a Windows 11 VM using Kali Linux.
Tools: UTM/VirtualBox, Windows 11, Kali Linux, Nmap, Metasploit, Nikto, DIRB, Wireshark.

Setup

Virtual Machines

Install UTM (or VirtualBox) on macOS.
Create VMs for Windows 11 and Kali Linux, allocating at least 4GB RAM and 2 CPU cores each.
Install OS on both VMs.

Networking

Set network type to "Internal Network" or "Host-Only Adapter" for both VMs.

Check IPs:

Windows: ipconfig

Kali: ifconfig
Test connectivity with ping.

Penetration Testing

Nmap Scan
Run Nmap from Kali to find open ports on the Windows VM:

Bash
nmap -sV 192.168.x.x

(Replace 192.168.x.x with the actual IP address of your Windows VM)

Exploitation

Launch Metasploit and use a relevant exploit based on the identified vulnerabilities from the Nmap scan.

Web Testing

(This section assumes a web server is running on the Windows VM)

Scan with Nikto:

Bash
nikto -h http://192.168.x.x:5357


(Replace 192.168.x.x with the actual IP address of your Windows VM and replace 5357 with the port your web server is running on)

Search for directories with DIRB:

Bash
dirb http://192.168.x.x:5357

(Replace 192.168.x.x with the actual IP address of your Windows VM and replace 5357 with the port your web server is running on)

Monitoring with Wireshark

Capture network traffic between VMs using Wireshark on Kali.
Analyze the packets to observe the attack's impact.

Conclusion

This project provides hands-on experience in cybersecurity, including VM setup, vulnerability scanning, exploitation, and traffic monitoring. It's an essential exercise for anyone looking to enhance their skills in network security.

Disclaimer: This project is for educational purposes only. Always ensure you have permission to test any system you do not own.

