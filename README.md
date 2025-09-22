# ElevateLabs
Task 1: Local Network Port Scanning
This repository documents the process of scanning a local network for open ports, an essential skill in network security and reconnaissance. The project was completed as part of a cybersecurity learning task.

🎯 Objective
The primary goal of this task was to learn how to identify open ports on devices within a local network. By understanding which services are exposed, one can assess the network's security posture and potential vulnerabilities.

🛠️ Tools Used
Nmap (Network Mapper): A powerful, free, and open-source utility for network discovery and security auditing. It was used to perform the port scanning.

Wireshark (Optional): A network protocol analyzer used to capture and analyze the packets generated during the scan for deeper insight.

📝 Process and Methodology
The following steps were executed to complete the task:

Step 1: Tool Installation

Installed Nmap from its official website.

Step 2: Finding the Local IP Range

Used the ipconfig (Windows) or ip addr (Linux/macOS) command to find my local IP address.

My local IP address was [Your Local IP Address]. Based on this, the local network range was identified as [Your IP Range, e.g., 192.168.1.0/24].

Step 3: Running the Scan

Executed a TCP SYN scan using sudo to gain the necessary root privileges. The command used was:

Bash
sudo nmap -sS [Your IP Range]
The -sS flag was chosen for its speed and stealth, as it performs a half-open scan without completing the full TCP handshake.

Step 4: Analyzing and Recording Results

After the scan completed, the output was analyzed to identify all IP addresses and their associated open ports. A summary of the findings is provided below:

[IP Address 1]: [List of open ports, e.g., 22 (SSH), 80 (HTTP)]

[IP Address 2]: [List of open ports, e.g., 443 (HTTPS), 3389 (RDP)]

[Add other results as needed]

The scan results were saved to a text file for documentation using the -oN flag:

Bash
sudo nmap -sS -oN scan_results.txt [Your IP Range]
Step 5: Research and Security Assessment

Each open port was researched to understand the common services running on them.

Based on the services identified, potential security risks were assessed. For example, an open RDP port (3389) could be a target for brute-force attacks if not properly secured with a strong password. Similarly, an unpatched web server on port 80 could be vulnerable to known exploits.

📈 Outcome and Key Takeaways
This task provided hands-on experience in network reconnaissance. I learned:

How to use Nmap for basic network discovery.

The difference between various scan types (e.g., SYN scan).

The importance of understanding what services are running on a network.

That open ports, while necessary for services, can also represent potential security risks if not managed properly.

This exercise is a fundamental step in any network security assessment and provides a solid foundation for more advanced penetration testing techniques.
