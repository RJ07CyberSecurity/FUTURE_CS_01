Task: -01
Vulnerability Assessment Report for a Live Website


•	Target Website: [https://owasp.org/www-project-juice-shop/]
•	Prepared by: RUDRAKUMAR JOSHI (Cyber security intern)	
•	Date: [16/03/2026]







Target Website: - OWSAP JUICE SHOP.









Executive Summary
Between March 12 and March 15, a vulnerability assessment was conducted on the web application testphp.vulnweb.com to analyze its security posture and identify potential security weaknesses. The objective of this assessment was to perform reconnaissance, network scanning, and vulnerability identification while maintaining a read-only testing scope.
During the assessment, several security testing tools were used to gather information and analyse the target system. Domain and ownership information was collected using WHOIS lookup services. Network scanning and service discovery were performed using Nmap, which helped identify open ports, running services, and possible entry points within the target system.

	Objectives of the Assessment
The key objectives of this vulnerability assessment were:
•	To identify open ports, running services, and accessible network components.
•	To detect known vulnerabilities in the web server, applications, and services.
•	To analyse security misconfigurations and weak security settings.
•	To assess the overall security posture of the target system.
•	To provide recommendations for improving the security of the website.
	High-Level Findings
The assessment revealed several potential security concerns that could impact the security of the system if left unaddressed. These include:
•	Presence of open ports exposing certain services to the public network.
•	Missing or improperly configured security headers.
•	Possible outdated software or server components.
•	Minor configuration weaknesses that may increase the attack surface.
Although no critical exploitation was performed during this assessment, the identified issues highlight areas where security improvements are recommended. Addressing these vulnerabilities will help strengthen the system against potential cyber threats and improve overall security resilience.

	Finding Severity Ratings
The following table defines levels of severity and corresponding CVSS score range that are used throughout the document to assess vulnerability and risk impact.

Severity	CVSS V3 Score Range	Definition
Critical	9.0-10.0	Exploitation is straightforward and usually results in system-level
compromise. It is advised to form a plan of action and patch immediately.
High	7.0-8.9	Exploitation is more difficult but could cause elevated privileges and potentially a loss of data or downtime. It is advised to form a plan of action and patch as soon as possible.
Moderate	4.0-6.9	Vulnerabilities exist but are not exploitable or require extra steps such as social engineering. It is advised to form a plan of action and patch after high-priority issues have been resolved.
Low	0.1-3.9	Vulnerabilities are non-exploitable but would reduce an organization’s
attack surface. It is advised to form a plan of action and patch during the next maintenance window.
Informational	N/A	No vulnerability exists. Additional information is provided regarding items noticed during testing, strong controls, and additional documentation.








Scope of Assessment
The scope of this vulnerability assessment defines the boundaries and limitations of the security testing performed on the target system. The assessment was conducted in a controlled and ethical manner to identify potential vulnerabilities without causing disruption to the target website or its services.

	Target Website
The vulnerability assessment was performed on the following target website:
Target URL: http://testphp.vulnweb.com/
The assessment focused on publicly accessible components of the website, including the web server, open ports, and HTTP security configurations.
	Assessment Type
The assessment was conducted as a Read-Only Vulnerability Assessment, meaning that the testing activities were limited to identifying vulnerabilities without attempting to exploit them.

	Allowed Activities
The following activities were permitted during the assessment:
•	Passive information gathering
•	Network scanning to identify active hosts
•	Port scanning to detect open ports and running services
•	Analysis of HTTP headers and security configurations
•	Identification of publicly exposed vulnerabilities


	Restricted Activities (Not Allowed)
To ensure the safety and availability of the target system, the following activities were strictly prohibited during the assessment:
•	Exploitation of identified vulnerabilities
•	Denial-of-Service (DoS) or stress testing
•	Brute force attacks on authentication systems
•	Any activity that could modify, delete, or disrupt system data or services


















Tools Used
During the vulnerability assessment, several cybersecurity tools were used to identify open ports, running services, and potential security vulnerabilities in the target website. These tools helped in gathering information, scanning the network, and analysing possible security weaknesses.
1. Nmap
Nmap (Network Mapper) is an open-source network scanning tool used to discover hosts and services on a computer network. It was used to identify active hosts, open ports, and running services on the target system.
Purpose:
•	Host discovery
•	Port scanning
•	Service and version detection













2. Nessus
Nessus is a widely used vulnerability scanning tool that detects security vulnerabilities, outdated software, and configuration issues. It helps identify known vulnerabilities in the target system.
Purpose:
•	Automated vulnerability scanning
•	Detection of security misconfigurations
•	Identification of outdated software components
Vulnerability:
•	Find the open port :443
•	Find host ip address:54.160.112.200
•	Detect os fingerprint

 





3. Nikto
Nikto is an open-source web server scanner used to detect vulnerabilities in web servers, including outdated software, insecure files, and dangerous configurations.
Purpose:
•	Web server vulnerability scanning
•	Detection of insecure files and configurations
•	Identification of outdated server components
Vulnerability: nikto find the vulnerability
•	This site is not present the anti-clickjacking X-Frame-Option in the security headers.
•	The X-Content-Type -Option header is not set.
Proof of Concept (PoC)
 








4. Zenmap
Zenmap is the graphical user interface for Nmap. It was used to visualize network scan results and understand the network topology more easily.
Purpose:
•	Network mapping visualization
•	Simplified scan configuration
•	Easy analysis of Nmap scan results
 
 
 












5. Browers DevTool 
Using Google Chrome DevTools, sensitive data was found in API responses and frontend code.
•	Steps to Reproduce:
1.	Open browser and inspect the page
2.	Go to Network tab
3.	Analyze Security Headers
•	Impact:
Attackers can access confidential user data
•	Recommendation:
o	Avoid exposing sensitive data in frontend
o	Implement proper access control
Vulnerability: Browser Developer Tools were used to identify potential vulnerabilities in the web application.
This site is Allow the Access-control-Allow the origin.
Proof of Concept (PoC)
 
Testing Methodology
The vulnerability assessment was conducted using a structured and systematic approach to identify potential security weaknesses in the target website. The testing followed standard penetration testing methodology while maintaining a read-only assessment scope. The main phases of the assessment are described below.
1. Reconnaissance (Information Gathering)
In this phase, publicly available information about the target website was collected. The objective was to understand the target system, its domain information, server details, and technology stack.
Activities performed:
•	Identifying the target domain and IP address
•	Gathering DNS and server information
•	Analysing publicly available data about the website
 
2. Network Scanning
Network scanning was performed to discover active hosts, open ports, and running services on the target system. This helps identify potential entry points that attackers may exploit.
Activities performed:
•	Host discovery
•	Port scanning
•	Service and version detection
Tools such as Nmap were used during this phase.
3. Vulnerability Identification
During this phase, the identified services and web components were analyzed to detect known vulnerabilities and security misconfigurations.
Activities performed:
•	Checking HTTP security headers
•	Identifying outdated software or services
•	Detecting misconfigured security settings
4. Analysis of Results
The scan results were carefully analysed to determine the potential security risks associated with the identified vulnerabilities. Each finding was reviewed and categorized based on its severity and potential impact.
5. Reporting
Finally, the results of the assessment were documented in a structured vulnerability assessment report. The report includes details of identified vulnerabilities, risk levels, and recommendations to improve the overall security posture of the target website.








1)	Clickjacking (Medium)
Description	The website is Vulnerable to clickjacking(an attack that tricks a user into clicking a webpage element which is invisible or disguised as another element). This can cause users to unwittingly download malware, visit malicious web pages, provide credentials or sensitive information, transfer money or purchase products online. The webpage was added to the “<iframe>” section of a test code and it was able to show the results
successfully.
Impact	Medium
System	https://juice-shop.herokuapp.com/'#/

Proof of Concept (PoC)
 
Recommendation: -
Implement X-frame-options header (Used to control whether a page can be placed in an <iframe>)
The syntax for adding xframe in Apache:
1)	Edit the httpd.conf file.
2)	Locate the section for your website or a virtual host.
3)	Add the following line inside the section:
Header always set X-Frame-Options "DENY"


