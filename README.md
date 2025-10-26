**Vulnerability Scanning Using Nessus Essentials**

Objective:

To use Nessus Essentials (a free vulnerability scanner) to identify common vulnerabilities present on a personal computer (local system).
This exercise provides hands-on experience in performing vulnerability assessments and understanding basic system risks.

Tools Used:

Tool: Nessus Essentials

Developer: Tenable Inc.

Platform: Windows 11

Setup and Installation:

Download Nessus Essentials
Visit the official Tenable website and download the Nessus Essentials installer for Windows.
Register with your email to receive a free activation code.

Install Nessus
Run the downloaded installer and follow on-screen instructions.
Once installed, open the browser and navigate to:
https://localhost:8834


Activate Nessus using your code and wait for the plugin updates to complete (may take 10–20 minutes).

Run Nessus as Administrator
Launch Nessus with administrative privileges to ensure full system scanning capability.

Identifying the Local Machine IP:

Open Command Prompt → type:

ipconfig


Note the IPv4 Address under your active adapter (e.g., 192.168.1.5).

This will be your target IP for scanning.

Performing the Vulnerability Scan:

Log in to the Nessus web interface:
https://localhost:8834


Go to Scans → New Scan → Basic Network Scan.

Enter details:

Name: Localhost Vulnerability Scan / basic scan (used here)

Targets: Your IPv4 address (e.g., 192.168.1.5) or localhost

Click Save → Launch Scan.

Wait for the scan to complete (approx. 30–60 minutes).

<img width="1902" height="918" alt="image" src="https://github.com/user-attachments/assets/876a4d78-adf0-4986-86e7-e79c68bca38c" />



*PDF attached but heres a screenshot*

<img width="1127" height="733" alt="image" src="https://github.com/user-attachments/assets/f513a182-d70f-4468-a6c3-0637ecc62f2c" />

Findings :

1. SSL Certificate Cannot Be Trusted

Plugin ID: 51192

Severity: Medium (CVSS 6.5)

Description: The SSL certificate used by the host is not signed by a trusted Certificate Authority (CA).

Impact: Attackers could perform man-in-the-middle (MITM) attacks.

Recommendation: Use a certificate issued by a trusted CA or configure the system to use valid internal PKI certificates.


2.SMB Signing Not Required

Plugin ID: 57608

Severity: Medium (CVSS 5.3)

Description: The SMB server does not require message signing, which makes it vulnerable to tampering or relay attacks.

Impact: Attackers can intercept and modify SMB communications.

Recommendation: Enable SMB signing to ensure message integrity.



Questions: 
1.What is vulnerability scanning?

Vulnerability scanning is an automated process used to find security weaknesses in computers, networks, or applications. It checks for outdated software, missing patches, weak configurations, and other flaws that attackers could exploit.

2.Difference between vulnerability scanning and penetration testing

Vulnerability scanning identifies known weaknesses automatically, while penetration testing actively tries to exploit them to see how serious they are. Scanning is broad and non-intrusive, while penetration testing is deeper, more manual, and simulates real attacks.

3.What are some common vulnerabilities in personal computers?

Common vulnerabilities include outdated operating systems, weak passwords, open ports, unpatched software, malware infections, and improperly configured firewalls or security settings.

4.How do scanners detect vulnerabilities?

Scanners compare system details like software versions and configurations against known vulnerability databases. They check for open ports, missing patches, default passwords, and insecure settings using automated tests and signature-based detection.

5.What is CVSS?

CVSS stands for Common Vulnerability Scoring System. It provides a standardized score from 0 to 10 to indicate how severe a vulnerability is, helping organizations decide which issues to fix first.

6.How often should vulnerability scans be performed?

Vulnerability scans should be done regularly, such as monthly or quarterly, and also after major system changes, new software installations, or network updates. They should also be done before audits or compliance reviews.

7.What is a false positive in vulnerability scanning?

A false positive happens when a scanner reports a vulnerability that isn’t actually present. For example, a scanner might flag a patched system as still vulnerable.

8.How do you prioritize vulnerabilities?

Vulnerabilities are prioritized based on their severity (using CVSS scores), the importance of the affected system, whether an exploit is publicly available, and the potential impact on business operations.
