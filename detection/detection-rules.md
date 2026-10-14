# Detection Rules – Waste Reporting Tool

## 1. Objective

The objective of this document is to describe basic security monitoring and detection queries for the simulated Waste Reporting Tool.

## 2. Detection Scenario: Failed Login Attempts

**Threat:** Brute Force / Password Guessing

**Description:** Repeated failed login attempts may indicate an attempt to guess user credentials.

**Log Source:** Simulated application HTTP logs

**Relevant Fields:**

* client_ip
* http_method
* endpoint
* status_code
* response_time

## 3. Kibana Detection Query

```text
endpoint: "/api/login" AND status_code: 401
```

**Purpose:** Identify failed login events in the application logs.

## 4. Expected Monitoring

A SOC Analyst can review:

* Source IP address
* Number of failed login events
* Login endpoint
* HTTP response status
* Event timestamps

Repeated failures from the same source IP should be investigated.

## 5. Investigation Recommendations

1. Identify the source IP address.
2. Review the number and timing of failed login events.
3. Check whether successful login events followed the failures.
4. Correlate events with other available security logs.
5. Escalate suspicious activity for further investigation.

## 6. Limitations

The application logs used in this project are simulated. The failed login events demonstrate a detection scenario and do not prove that a real brute-force attack occurred.

## 7. Conclusion

This detection scenario demonstrates how Kibana can be used to search and investigate failed login events as part of basic SOC monitoring.
