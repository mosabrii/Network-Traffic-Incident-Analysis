# Security Risk Assessment Report

## Organization Type
Social media organization.

## Reason for Assessment
The organization previously experienced a data breach that exposed customer personal information. This assessment was conducted to identify existing security weaknesses and reduce the likelihood of future incidents.

## Affected Data
- User names
- User addresses

## Critical Assets
- User personal data (PII)
- Database server
- Administrative and privileged accounts
- Network infrastructure
- Internal systems and services

## Identified Vulnerabilities
- Employees share passwords.
- The database administrator account uses a default password.
- Firewall rules are not configured to filter incoming and outgoing traffic.
- Multi-Factor Authentication (MFA) is not implemented.

## Potential Threats
- Unauthorized access
- Data breach
- Credential compromise
- Insider threats
- External attacks exploiting weak security controls

## Risk Analysis
- Default database administrator password: **High risk**
- Lack of firewall traffic filtering: **High risk**
- Password sharing among employees: **Medium risk**
- Absence of MFA: **Medium risk**

## Impact Assessment
If these vulnerabilities are not addressed, attackers could gain unauthorized access to sensitive data, leading to additional data breaches, reputational damage, and potential legal consequences.

## Current Security Posture
The organization lacks several fundamental security controls, increasing exposure to internal and external threats.

## Recommendations

Security recommendations and remediation actions have been documented separately to maintain clarity and separation of concerns.

Please refer to the **remediation-strategy.md** file for detailed security controls, mitigation steps, and long-term hardening recommendations related to this incident.
