## Incident Summary

### Overview
The company’s website, **yummyrecipesforme.com**, was compromised following a successful brute-force attack targeting the administrative account. A former employee repeatedly attempted known default passwords until gaining unauthorized access to the admin panel.

### What Happened
After accessing the administrative interface, the attacker modified the website’s source code by injecting malicious JavaScript. This script prompted visitors to download a file that contained malware. Once executed, the malware redirected users from the legitimate website to a malicious external domain.

### Detection
The incident was identified after multiple customers contacted the help desk reporting unusual behavior. Users stated that they were prompted to download a file in order to access free recipes. After running the file, their devices became noticeably slower, and their browsers were redirected to a different website not associated with the company.

### Affected Assets
- Administrative account access (password was changed by the attacker)
- Website source code (JavaScript injection)
- End-user devices infected with malware
- Website availability and trustworthiness

### Network Protocols Involved
- **DNS** – Used to resolve domain names during redirection to the malicious website  
- **HTTP** – Used to request web pages and download the malicious file  
- **TCP** – Transport protocol used to establish connections  

DNS and HTTP operate at the **Application Layer**, while TCP operates at the **Transport Layer** of the TCP/IP model.

### Severity and Impact
**Severity: High**

The attacker gained administrative control of the website, injected malicious code, and exposed users to malware. The incident disrupted normal operations, compromised user safety, and resulted in loss of trust in the organization’s web services.

### Incident Scope
The scope of the incident included:
- The web server’s admin panel
- The website’s source code
- End-user systems affected by malware

### Current Status
The scenario did not explicitly state the final containment or recovery status at the time of investigation. However, a sandbox environment was established for monitoring, and efforts were underway to restore administrative access.
