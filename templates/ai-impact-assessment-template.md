# AI Impact Assessment Template

## 1. Assessment Details

| Field | Details |
|---|---|
| Assessment ID | |
| AI System Name | |
| AI System Owner | |
| Business Owner | |
| Technical Owner | |
| Assessment Owner | |
| Date Completed | |
| Deployment Stage | Proposed / Pilot / Production / Material Change |
| Overall Risk Rating | Low / Medium / High / Critical |

## 2. System Description

### Intended Purpose

Describe the AI system's business purpose and intended outputs.

### Context of Use

Describe where, when, and by whom the AI system will be used.

### System Boundaries

Describe what the system is allowed to do and what it must not do.

### Deployment Model

| Area | Details |
|---|---|
| AI type | |
| Provider or model | |
| Hosting model | |
| Integrations | |
| User groups | |
| Data sources | |
| Output types | |
| Autonomous actions | |
| Human-review points | |

## 3. Stakeholder Impact

| Stakeholder | Potential Benefit | Potential Harm | Mitigation |
|---|---|---|---|
| Employees / Internal Users | | | |
| Customers | | | |
| Affected Individuals | | | |
| Business Operations | | | |
| Security Team | | | |
| Privacy / Compliance Team | | | |
| Third Parties | | | |

## 4. Data and Privacy Assessment

| Question | Response | Evidence or Notes |
|---|---|---|
| What data categories are processed? | | |
| Does the system process personal data? | Yes / No | |
| Does the system process confidential or restricted data? | Yes / No | |
| Is the data necessary and proportionate to the purpose? | Yes / No | |
| Can data be minimized, masked, anonymized, or excluded? | Yes / No | |
| Are retention and deletion requirements defined? | Yes / No | |
| Are data residency and cross-border transfers understood? | Yes / No | |
| Does the provider use data for training or model improvement? | Yes / No / Unknown | |
| Is a privacy review or DPIA required? | Yes / No | |

## 5. Security Assessment

| Risk Area | Assessment | Risk Rating | Required Controls |
|---|---|---|---|
| Identity and access management | | | |
| API and integration security | | | |
| Data encryption | | | |
| Logging and monitoring | | | |
| Prompt injection and adversarial input | | | |
| Unauthorized data exposure | | | |
| Secrets and credential handling | | | |
| Provider security posture | | | |
| Vulnerability management | | | |
| Service availability and resilience | | | |

## 6. Reliability and Quality Assessment

| Question | Response | Mitigation |
|---|---|---|
| Could the system hallucinate or provide unsupported output? | | |
| Could the system produce incomplete or outdated information? | | |
| Could output errors create operational, customer, or security impact? | | |
| Is testing against representative scenarios planned? | | |
| Is human validation required before use of output? | | |
| Are quality metrics and thresholds defined? | | |
| Is there a fallback process if the system is unavailable or unreliable? | | |

## 7. Fairness, Transparency, and Human Oversight

| Question | Response | Mitigation |
|---|---|---|
| Could the system create discriminatory or unfair outcomes? | | |
| Does the system make or materially influence consequential decisions? | | |
| Are users informed when content or recommendations are AI-generated? | | |
| Can users challenge, reject, or override output? | | |
| Is a human responsible for final decisions? | | |
| Are known limitations documented and communicated? | | |
| Are customer-facing outputs reviewed before release? | | |

## 8. Third-Party Assessment

| Question | Response | Notes |
|---|---|---|
| Is an external provider involved? | Yes / No | |
| Has a supplier assessment been completed? | Yes / No | |
| Are security and privacy terms included in the contract? | Yes / No | |
| Are incident-notification requirements defined? | Yes / No | |
| Are subprocessors disclosed and monitored? | Yes / No | |
| Is there an exit or migration strategy? | Yes / No | |
| Are material provider or model changes reviewed? | Yes / No | |

## 9. Misuse and Incident Scenarios

| Scenario | Potential Impact | Likelihood | Controls | Residual Risk |
|---|---|---|---|---|
| Data leakage | | | | |
| Prompt injection | | | | |
| Unauthorized access | | | | |
| Harmful or inaccurate output | | | | |
| Excessive permissions | | | | |
| Provider outage | | | | |
| Policy violation | | | | |
| Unapproved use-case expansion | | | | |

## 10. Testing Requirements

- [ ] Accuracy and reliability testing
- [ ] Security and access-control testing
- [ ] Prompt-injection and adversarial-input testing
- [ ] Privacy and data-minimization validation
- [ ] Logging and monitoring validation
- [ ] Integration and API security testing
- [ ] User acceptance testing
- [ ] Human-oversight workflow testing
- [ ] Fallback and service-outage testing
- [ ] Third-party assurance review

## 11. Decision and Conditions

| Field | Details |
|---|---|
| Assessment Outcome | Approved / Conditionally Approved / Rejected / Pending |
| Required Conditions | |
| Residual Risk Rating | |
| Risk Acceptance Required? | Yes / No |
| Required Remediation Actions | |
| Deployment Restrictions | |
| Approval Authorities | |
| Assessment Review Date | |

## 12. Reassessment Triggers

This assessment must be reviewed after:

- A material model, provider, integration, data, or deployment change
- An AI-related security, privacy, operational, or customer incident
- A material decline in output quality or reliability
- A change in legal, regulatory, contractual, or customer requirements
- Addition of new user groups, data categories, or autonomous capabilities
- Expansion into customer-facing, high-impact, or consequential decisions
