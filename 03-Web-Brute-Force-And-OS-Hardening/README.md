# Web Brute Force Attack & OS Hardening Analysis

## Overview
This project documents a cybersecurity incident involving a brute force attack against a web server hosting the website **yummyrecipesforme.com**.  
The incident resulted in unauthorized access to the administrative panel, malicious code injection, and redirection of users to a fake website distributing malware.

The purpose of this project is to simulate a real-world security incident investigation and demonstrate how such incidents are analyzed, documented, and mitigated.

## Scenario Summary
A former employee launched a brute force attack by repeatedly attempting known default administrative passwords until successful access was gained.  
After compromising the admin account, the attacker modified the website’s source code by injecting malicious JavaScript that prompted users to download and execute a file.

Once executed, users were redirected from the legitimate website to a malicious clone website containing malware.

## Objectives
- Identify the network protocols involved in the incident
- Analyze captured network traffic
- Document the incident in a structured and professional manner
- Recommend security measures to prevent brute force attacks in the future

## Tools Used
- tcpdump
- Wireshark
- JavaScript (malicious code analysis)
- Linux Server

## Contents Description
- **incident-summary.md**  
  A high-level summary describing what happened, how it was detected, and the overall impact.

- **incident-report.md**  
  A detailed technical analysis of the incident, including timelines, protocols used, attack type, and root cause.

- **remediation.md**  
  Recommended security controls and hardening techniques to prevent similar attacks in the future.

- **evidence/**  
  Supporting materials such as traffic logs, templates, and reference documents used during the investigation.

## Skills Demonstrated
- Incident response documentation  
- Network traffic analysis  
- Brute force attack identification  
- Security hardening recommendations  
- Professional cybersecurity reporting

## Disclaimer
This project is for educational and portfolio purposes only.  
All scenarios are simulated and do not represent real organizations or active security incidents.
