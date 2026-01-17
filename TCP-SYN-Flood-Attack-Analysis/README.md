# TCP SYN Flood Attack – Network Incident Analysis

## Overview
This lab simulates a real-world network attack scenario where a company website becomes unavailable due to a malicious network-based attack. The objective is to analyze captured network traffic, identify the type of attack, understand how it impacted the web server, and document the incident in a structured security report.

The scenario reflects common incidents handled by SOC and Blue Team analysts in production environments.

---

## Scenario
Employees at a travel agency regularly access the company’s web application to review sales and promotional offers. One afternoon, an automated monitoring alert indicated an issue with the web server.

When attempting to access the website, users received a connection timeout error. Initial investigation revealed an unusually large number of incoming TCP SYN requests from an unfamiliar IP address. The web server became overwhelmed by the volume of requests and was unable to respond to legitimate traffic.

Network traffic was captured using a packet analysis tool to investigate the incident and determine the nature of the attack.

---

## Objectives
- Analyze network traffic related to a service outage
- Identify malicious network behavior
- Determine the type of network attack involved
- Understand how the attack affected server availability
- Practice structured incident documentation and reporting

---

## Attack Focus
- Network-layer attack analysis
- TCP connection behavior
- Denial of Service (DoS) techniques
- Impact of excessive SYN requests on web servers

---

## Lab Structure
Each lab artifact is organized as follows:

- `incident-summary.md`  
  A high-level executive summary describing what happened, who was affected, and the suspected cause.

- `incident-report.md`  
  A detailed technical incident report including timeline, traffic analysis, root cause, impact, and recommendations.

- `evidence/`  
  Supporting materials such as network traffic logs and packet captures used during the investigation.

---

## Skills Demonstrated
- Network traffic analysis
- Identifying Denial of Service attacks
- TCP/IP protocol understanding
- Incident response documentation
- SOC / Blue Team analytical thinking

---

## Disclaimer
This lab is created for educational and portfolio purposes only.  
All systems, logs, IP addresses, and scenarios are fictional and used solely to demonstrate cybersecurity concepts.
