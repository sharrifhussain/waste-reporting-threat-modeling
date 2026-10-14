# Risk Assessment – Waste Reporting Application

## Risk Scoring Method

Risk is calculated using the following formula:

Risk Score = Likelihood × Impact

Both likelihood and impact are rated from 1 to 5.

### Likelihood Scale

| Score | Description |
| ----- | ----------- |
| 1     | Very Low    |
| 2     | Low         |
| 3     | Medium      |
| 4     | High        |
| 5     | Very High   |

### Impact Scale

| Score | Description |
| ----- | ----------- |
| 1     | Very Low    |
| 2     | Low         |
| 3     | Medium      |
| 4     | High        |
| 5     | Very High   |

### Risk Rating

| Risk Score | Rating   |
| ---------- | -------- |
| 1–4        | Low      |
| 5–9        | Medium   |
| 10–16      | High     |
| 17–25      | Critical |

## Risk Assessment Table

| STRIDE Threat          | Likelihood | Impact | Risk Score | Rating |
| ---------------------- | ---------: | -----: | ---------: | ------ |
| Spoofing               |          4 |      4 |         16 | High   |
| Tampering              |          3 |      5 |         15 | High   |
| Repudiation            |          3 |      3 |          9 | Medium |
| Information Disclosure |          3 |      5 |         15 | High   |
| Denial of Service      |          3 |      4 |         12 | High   |
| Elevation of Privilege |          2 |      5 |         10 | High   |

## Risk Reasoning

### 1. Spoofing – 16 (High)

Login functionality may be targeted by attackers attempting to use stolen credentials. Successful account compromise could expose private reports.

### 2. Tampering – 15 (High)

Unauthorized changes to waste reports or collection status could affect data integrity and operational decisions.

### 3. Repudiation – 9 (Medium)

Insufficient audit logging could make it difficult to verify who performed an action or investigate an incident.

### 4. Information Disclosure – 15 (High)

Unauthorized access to user information or private reports could cause privacy and confidentiality issues.

### 5. Denial of Service – 12 (High)

Excessive requests could consume application resources and affect service availability.

### 6. Elevation of Privilege – 10 (High)

If access controls are weak, a normal user could potentially obtain administrator-level permissions, resulting in serious damage.

## Conclusion

The initial assessment identifies Spoofing, Tampering, Information Disclosure, and Denial of Service as high-priority risks. Repudiation is medium priority, while Elevation of Privilege requires further investigation.

These are preliminary scores based on assumed application functionality. They should be reviewed after security testing and evidence collection.
