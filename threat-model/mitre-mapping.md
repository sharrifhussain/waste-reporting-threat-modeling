# MITRE ATT&CK Mapping – Waste Reporting Application

This document maps potential STRIDE threats to relevant MITRE ATT&CK techniques.

| STRIDE Category        | Potential Threat                                       | MITRE Technique                       | Technique ID |
| ---------------------- | ------------------------------------------------------ | ------------------------------------- | ------------ |
| Spoofing               | Misuse of legitimate user credentials                  | Valid Accounts                        | T1078        |
| Tampering              | Exploitation of a vulnerable public-facing application | Exploit Public-Facing Application     | T1190        |
| Repudiation            | Deletion or clearing of Windows event logs             | Clear Windows Event Logs              | T1070.001    |
| Information Disclosure | Unauthorized access to information repositories        | Data from Information Repositories    | T1213        |
| Denial of Service      | Overloading an application endpoint                    | Endpoint Denial of Service            | T1499        |
| Elevation of Privilege | Exploiting a vulnerability to gain higher privileges   | Exploitation for Privilege Escalation | T1068        |

## Mapping Explanation

### 1. Spoofing – T1078

An attacker may misuse valid account credentials to impersonate an authorized user.

### 2. Tampering – T1190

An attacker may exploit a vulnerable public-facing application to compromise application data or functionality.

### 3. Repudiation – T1070.001

An attacker may clear Windows event logs to hide evidence of malicious activity. This is a possible evidence-removal scenario, not the same as ordinary user denial.

### 4. Information Disclosure – T1213

An attacker may access sensitive information stored in application data repositories.

### 5. Denial of Service – T1499

An attacker may overload application endpoints, affecting availability for legitimate users.

### 6. Elevation of Privilege – T1068

An attacker may exploit a software vulnerability to gain higher-level permissions.

## Important Note

These mappings represent potential attacker behaviors. They do not confirm that these attacks occurred in the simulated application. Technique relevance depends on the actual attack scenario and available evidence.

Reference: https://attack.mitre.org/
