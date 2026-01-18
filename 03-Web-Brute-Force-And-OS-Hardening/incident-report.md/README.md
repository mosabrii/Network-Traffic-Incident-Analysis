# Incident Report  
## Web Brute Force Attack & Malware Injection

---

## 1. Incident Identification

A security incident occurred involving the company’s website **yummyrecipesforme.com**.  
The incident was caused by a successful brute-force attack targeting the administrative account, which resulted in unauthorized access, malicious JavaScript injection, and malware distribution to end users.

---

## 2. Attack Vector

The attacker, identified as a former employee, performed a **brute-force attack** against the administrator account.  
Because the admin account was using a **default and weak password**, the attacker successfully guessed the credentials and gained access to the admin panel.

After authentication, the attacker injected **malicious JavaScript** into the website’s source code.  
This JavaScript prompted visitors to download a malicious executable file, leading to malware infection and redirection to a malicious external website.

---

## 3. Timeline of Events

- Multiple failed login attempts were detected against the admin account.
- A successful login was recorded shortly after from a suspicious IP address.
- The attacker modified the website’s source code by injecting malicious JavaScript.
- Website visitors were prompted to download a suspicious file.
- After execution, users were redirected from `yummyrecipesforme.com` to `greatrecipesforme.com`.
- The redirection occurred on (IP address: **192.0.2.17**).
- Multiple customer complaints were received reporting unusual behavior and system slowdowns.
- The security team initiated an investigation using tcpdump logs and sandbox analysis.

---

## 4. Detection and Evidence

To verify the incident, a **sandbox environment** was created to observe the website’s behavior safely.  
Network traffic was captured and analyzed using **tcpdump**, revealing the following sequence:

- DNS request to resolve `yummyrecipesforme.com`
- DNS response returning the legitimate IP address
- HTTP request to the legitimate website
- Download of a malicious executable file (flagged in logs)
- DNS request for `greatrecipesforme.com`

These findings confirmed the presence of malicious behavior and unauthorized code injection.

---

## 5. Network Protocols Involved

- **DNS** – Used to resolve domain names during redirection
- **HTTP** – Used to request web pages and download the malicious file
- **TCP** – Transport protocol used to establish connections

DNS and HTTP operate at the **Application Layer**, while TCP operates at the **Transport Layer** of the TCP/IP model.

---

## 6. Impact Analysis

The incident had significant technical and business impact, including:

- Loss of administrative control over the website
- Injection of malicious JavaScript into the website’s source code
- Malware infections on end-user devices
- Website service disruption and loss of customer trust
- Interruption of normal business operations

---

## 7. Root Cause Analysis

The root cause of the incident was the use of a **default and weak administrator password**.  
Additional contributing factors included:

- Lack of brute-force protection mechanisms
- Absence of multi-factor authentication (MFA)
- No monitoring or alerting for suspicious login activity
- No restriction on login attempts from unfamiliar IP addresses

---

## 8. Current Status

The scenario does not explicitly state the final containment or recovery status at the time of investigation.  
However, the incident was fully confirmed through network traffic analysis and sandbox testing.

---

## 9. Recommendations

High-level security recommendations and mitigation steps are documented separately in the **remediation.md** file.
