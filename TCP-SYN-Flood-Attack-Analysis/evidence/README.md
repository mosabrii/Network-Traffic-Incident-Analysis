# Evidence

This directory contains supporting evidence related to the TCP SYN Flood attack investigation.

## Network Traffic Capture

- **File:** HTTP-log.pdf
- **Source:** Wireshark packet capture (exported report)
- **Description:**
  The log shows a significant increase in TCP SYN packets originating primarily from the IP address `203.0.113.0` targeting the web server `192.0.2.1`.

## Key Observations

- Repeated TCP SYN requests without completing the three-way handshake.
- Legitimate HTTP traffic initially succeeded, then dropped significantly during the attack.
- Multiple `RST, ACK` responses and `504 Gateway Timeout` errors observed.
- Traffic patterns are consistent with a TCP SYN Flood Denial-of-Service (DoS) attack.

This evidence supports the findings documented in the incident report and incident summary.
