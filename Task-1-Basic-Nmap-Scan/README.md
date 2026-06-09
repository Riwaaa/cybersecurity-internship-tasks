Basic Network Scanning with Nmap
Objective
The objective of this task was to perform a basic network scan using Nmap to identify open ports and services running on the local machine.
Tools Used
•	Nmap 7.99
•	Windows Command Prompt
Scan Command
nmap 127.0.0.1
Scan Results
Target Host: 127.0.0.1 (localhost)
The scan identified the following open ports:
Port	State	Service
135/tcp	Open	msrpc
445/tcp	Open	microsoft-ds
1434/tcp	Open	ms-sql-m
Nmap reported:
•	Host is up
•	997 TCP ports were closed
•	3 TCP ports were open
Port Analysis
Port 135/tcp - MSRPC
MSRPC (Microsoft Remote Procedure Call) allows Windows applications and services to communicate across a network.
Security Significance
•	Required by many Windows services.
•	Can be targeted by attackers if exposed to untrusted networks.
•	Should be restricted through firewall rules when possible.
Port 445/tcp - Microsoft-DS
This port is used by SMB (Server Message Block) for file and printer sharing.
Security Significance
•	Commonly used in Windows file sharing.
•	Frequently targeted by malware and ransomware.
•	Access should be limited to trusted networks.
Port 1434/tcp - Microsoft SQL Monitor
This port is associated with Microsoft SQL Server services.
Security Significance
•	Used for SQL Server instance discovery.
•	May reveal information about database services.
•	Should not be exposed publicly without proper security controls.
Findings
The scan revealed that the localhost system is running Windows services related to RPC, SMB file sharing, and Microsoft SQL Server.
No unexpected services were identified during the scan.
Recommendations
1.	Disable unnecessary services.
2.	Restrict SMB access to trusted users and networks.
3.	Keep Windows and SQL Server updated.
4.	Use a firewall to limit exposure of network services.
5.	Regularly monitor open ports using security tools.
Conclusion
This task demonstrated how Nmap can be used to identify open ports and services on a host. Network scanning is an important first step in understanding the security posture of a system and identifying potential attack surfaces.

