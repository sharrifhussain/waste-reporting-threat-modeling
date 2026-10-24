## 11. Sigma Detection Rules

Sigma was used to define standardized detection logic for security monitoring.

### 11.1 Spoofing Detection

The failed login detection identifies unsuccessful login attempts against the application.

Detection criteria:
- Endpoint: `/api/login`
- Status code: `401`
- Correlation field: `client_ip`
- Threshold: 5 or more events within 5 minutes
- Severity: High
- MITRE ATT&CK: T1110 – Brute Force

Sigma files:
- `detection-rules/spoofing-base.yml`
- `detection-rules/spoofing-correlation.yml`

### 11.2 Tampering Detection

The tampering detection rule identifies HTTP methods commonly associated with resource modification or deletion.

Detection criteria:
- HTTP methods: PUT, PATCH, DELETE
- Severity: Medium

False positives may include authorized administrative changes, normal application workflows, and QA testing activities.

Investigation includes reviewing the source IP, user identity, endpoint, and application audit logs. A matching request is an indicator for investigation and does not automatically prove unauthorized activity.

Rule file: `detection-rules/tampering-rule.json`

## 12. Sigma Validation and Testing

Sigma rules were validated using the Sigma CLI.

Validation command:

` sigma check detection-rules/ `

The validation completed with zero rule errors, condition errors, and validation issues.

The failed login correlation logic was converted into Elasticsearch ES|QL and tested in Kibana Dev Tools.

The test identified 10 failed login events from source IP `192.168.1.25`, meeting the configured threshold of five events within five minutes.

Note: This confirms the query logic against the available sample logs. It does not represent an automatically configured Kibana alert.

## 13. Testing Evidence

The following screenshots provide evidence of the detection testing:

- `evidence/spoofing-sigma-kibana-test.png` – Failed login detection testing.
- `evidence/spoofing-correlation-esql-test.png` – Correlation query testing in Kibana.
