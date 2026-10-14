# STRIDE Threat Identification – Waste Reporting Application

## Project Overview

This threat model identifies potential security threats in a simulated Waste Reporting Application. The application allows users to log in, submit waste reports, and check collection status.

The system architecture consists of a frontend, backend/API, and database. Application logs are monitored using the ELK Stack.

## 1. Spoofing

**Threat:** An attacker may attempt to impersonate a legitimate user by using stolen or compromised login credentials.

**Example:** Repeated login attempts against the `/api/login` endpoint.

**Potential Impact:** Unauthorized access to user accounts and private reports.

**Possible Mitigation:** Strong passwords, multi-factor authentication, account lockout, and login monitoring.

## 2. Tampering

**Threat:** An attacker may attempt to modify waste reports or collection status without authorization.

**Example:** Unauthorized modification of a report through an API request.

**Potential Impact:** Incorrect waste collection records and loss of data integrity.

**Possible Mitigation:** Server-side authorization, input validation, database access controls, and audit logging.

## 3. Repudiation

**Threat:** A user may deny creating, modifying, or deleting a waste report.

**Example:** A user denies changing a report, and the application does not have sufficient audit records to verify the activity.

**Potential Impact:** Difficulty investigating incidents and identifying responsible users.

**Possible Mitigation:** Maintain timestamped audit logs, user IDs, activity records, and protected log storage.

## 4. Information Disclosure

**Threat:** An attacker may gain unauthorized access to sensitive user information or waste reports.

**Example:** Unauthorized access to private reports or user details through an API.

**Potential Impact:** Exposure of personal information and privacy violations.

**Possible Mitigation:** Authentication, authorization, HTTPS, encryption, and restricted database access.

## 5. Denial of Service

**Threat:** An attacker may send excessive requests to make the application unavailable.

**Example:** A large number of requests to the `/api/reports` endpoint.

**Potential Impact:** Slow application response or service unavailability for legitimate users.

**Possible Mitigation:** Rate limiting, traffic monitoring, request filtering, and infrastructure protection.

## 6. Elevation of Privilege

**Threat:** A normal user may attempt to gain administrator-level permissions.

**Example:** A user attempts to access an admin-only endpoint without authorization.

**Potential Impact:** Unauthorized administrative access and control over application data.

**Possible Mitigation:** Role-based access control, server-side permission checks, and privilege-change auditing.

## Conclusion

The STRIDE analysis identifies six potential security threat categories. These threats should be investigated through application testing, security logs, and appropriate monitoring controls.

