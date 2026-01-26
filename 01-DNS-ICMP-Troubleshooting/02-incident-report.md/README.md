# Incident Report – Network Traffic Analysis

## Incident Overview
Multiple customers reported being unable to access the website www.yummyrecipesforme.com.
Users encountered a "Destination Port Unreachable" error when attempting to load the website.
The incident affected the availability of the web service and required network-level investigation.

## Timeline of Events
- Customers reported the issue after repeated website access failures.
- Initial access attempts to the website failed from a user perspective.
- Network traffic was captured using tcpdump during troubleshooting.
- Multiple UDP packets were sent to the DNS server on port 53.
- ICMP error messages were received indicating that UDP port 53 was unreachable.

## Technical Analysis
The investigation focused on analyzing captured network traffic.
DNS resolution attempts were made using UDP traffic directed to the DNS server.
Instead of receiving valid DNS responses, ICMP error messages were returned.
The ICMP messages indicated that the destination port (UDP 53) was unreachable.
This suggests that DNS requests were not being processed by the DNS service.

## Root Cause
The suspected root cause is that the DNS service was unavailable or not listening on UDP port 53.
As a result, DNS queries could not be resolved, preventing users from accessing the website.
There is no direct evidence confirming whether a firewall or IDS was blocking the traffic.

## Impact
- Website www.yummyrecipesforme.com was completely inaccessible.
- Customers were unable to use the service.
- Business operations relying on the website were disrupted.

## Recommendations / Next Steps
- Verify that the DNS service is running and listening on UDP port 53.
- Review firewall and security rules to ensure DNS traffic is allowed.
- Confirm proper DNS configuration on the server.
- Implement monitoring to detect similar issues earlier in the future.
