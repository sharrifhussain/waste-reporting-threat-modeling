# Waste Reporting Tool – Threat Modeling & Security Monitoring

## 1. Project Overview

This project focuses on threat modeling and security monitoring for a simulated Waste Reporting Tool.

The objective is to identify potential security threats, analyze them using the STRIDE framework, map relevant threats to MITRE ATT&CK techniques, and assess their risk levels.

The project also uses the ELK Stack (Elasticsearch, Logstash, and Kibana) to collect, process, search, and visualize simulated application logs.

**Note:** The application architecture represents an assumed logical design for threat modeling. The application itself is simulated through generated HTTP logs.

## 2. Project Objectives

* Understand the system architecture.
* Identify potential security threats using STRIDE.
* Map threats to relevant MITRE ATT&CK techniques.
* Evaluate risks based on likelihood and impact.
* Process simulated application logs using Logstash.
* Store and search logs using Elasticsearch.
* Visualize security events using Kibana.
* Identify opportunities for security monitoring and detection.

## 3. System Architecture

The assumed application architecture includes:

* Frontend: User interface for submitting waste reports.
* Backend: Handles authentication, report submission, and application logic.
* Database: Stores user information and waste reports.
* ELK Stack: Monitors simulated application logs.

See `threat-model/system-diagram.png` for the architecture diagram.

## 4. STRIDE Threat Modeling

The STRIDE framework was used to identify six categories of potential threats:

* Spoofing
* Tampering
* Repudiation
* Information Disclosure
* Denial of Service
* Elevation of Privilege

Detailed analysis is available in `threat-model/stride-threats.md`.

## 5. MITRE ATT&CK Mapping

Potential threats were mapped to relevant MITRE ATT&CK techniques to support threat understanding and detection planning.

See `threat-model/mitre-mapping.md`.

## 6. Risk Assessment

Each identified threat was assessed using:

* Likelihood: 1–5
* Impact: 1–5
* Risk Score: Likelihood × Impact

See `threat-model/risk-assessment.md`.

## 7. ELK Stack Integration

The ELK Stack was configured using Docker Compose.

* Elasticsearch: Stores and indexes application logs.
* Logstash: Reads and parses simulated HTTP logs.
* Kibana: Provides log searching and visualization.

The simulated logs include client IP, HTTP method, endpoint, status code, and response time.

## 8. Detection and Monitoring

Example monitoring query for failed login attempts:

`endpoint: "/api/login" AND status_code: 401`

This query can help identify repeated failed login events in the simulated dataset.

See `detection/detection-rules.md` for detection documentation.

## 9. Screenshots

Project screenshots will demonstrate:

* System architecture diagram.
* STRIDE threat analysis.
* Kibana Discover log events.
* Kibana security monitoring dashboard.

## 10. Conclusion

This project demonstrates a basic threat modeling and security monitoring workflow for a simulated web application.

It combines STRIDE analysis, MITRE ATT&CK mapping, risk assessment, and ELK-based log monitoring to develop a foundational understanding of application security and SOC monitoring.

