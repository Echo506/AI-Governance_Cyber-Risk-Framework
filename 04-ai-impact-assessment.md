# AI Impact Assessment

## 1. Assessment Information

| Field | Details |
|---|---|
| Assessment ID | AIA-001 |
| AI System | NovaAssist |
| Assessment Date | 2026-08-19 |
| Assessment Owner | AI Governance Owner |
| Business Owner | Director of Operations |
| Technical Owner | IT Automation and Security Team |
| Assessment Status | Initial pre-deployment assessment |
| Risk Level | Medium |

## 2. Purpose of the AI System

NovaAssist is a generative AI assistant designed to support internal NOC and technical-support operations.

Its intended functions are ticket summarization, ticket classification suggestions, knowledge retrieval, response drafting, incident documentation support, and identification of missing troubleshooting information.

The system is intended to improve documentation quality and reduce administrative workload. It is not intended to replace technical judgment, execute changes, communicate autonomously with customers, or make high-impact decisions.

## 3. Stakeholders

| Stakeholder | Potential Impact |
|---|---|
| NOC analysts | Faster documentation and knowledge retrieval; risk of relying on inaccurate recommendations |
| Technical-support agents | Improved response drafting; risk of sending inaccurate or incomplete communications |
| SOC analysts | Assistance with summarization and triage context; risk of mishandling sensitive security information |
| Customers | Potentially faster responses; risk of exposure of customer information or inaccurate service updates |
| Operations leadership | Improved efficiency metrics; risk of overreliance on AI performance claims |
| Privacy and compliance teams | Need visibility into data processing, retention, provider practices, and regulatory obligations |
| AI provider | Must meet contractual, security, privacy, and incident-notification requirements |

## 4. Context of Use

NovaAssist will be used by trained internal personnel through an approved enterprise account.

The system will process approved operational information and selected ticket data. Users must follow data-classification rules and may not submit passwords, tokens, API keys, private keys, payment data, or other prohibited sensitive information.

All outputs require human review before operational use.

## 5. Impact Areas

| Impact Area | Assessment | Risk Level | Required Mitigations |
|---|---|---|---|
| Security | Prompt injection, insecure API use, unauthorized access, and data leakage are possible | Medium | MFA, RBAC, approved integrations, logging, secure API key management, security monitoring |
| Privacy | Tickets may contain personal or customer information | Medium | Data minimization, masking, privacy review, approved retention, vendor contractual controls |
| Accuracy and Reliability | The model may hallucinate, omit facts, or provide outdated technical guidance | Medium | Human validation, knowledge-base grounding, sampling, quality testing, escalation process |
| Operational Continuity | Incorrect recommendations may delay troubleshooting or create poor customer communication | Medium | Human approval, no autonomous actions, fallback to established procedures |
| Transparency | Users may not recognize that a draft or summary contains AI-generated content | Low | User training, labeling where appropriate, documented workflow |
| Fairness and Bias | The use case does not determine eligibility, employment, pricing, credit, or other consequential decisions | Low | Restrict use case, monitor feedback, prohibit high-impact decision use |
| Legal and Compliance | Contractual, privacy, data-transfer, and regulatory obligations may apply | Medium | Legal and privacy review, documented approval, vendor due diligence |
| Third-Party Dependency | Availability, model changes, data processing, and security practices depend on a provider | Medium | Supplier assessment, contract clauses, monitoring, exit strategy |
| Reputational Impact | Poor outputs or information leakage could affect customer trust | Medium | Review workflow, incident process, clear ownership, customer communication procedures |

## 6. Foreseeable Misuse Scenarios

| Scenario | Potential Harm | Preventive Control |
|---|---|---|
| User submits credentials or secrets in a prompt | Credential compromise or unauthorized access | Policy prohibition, user training, data-loss prevention controls |
| User accepts an inaccurate AI response without validation | Incorrect troubleshooting or customer guidance | Mandatory human review and validation |
| Prompt injection is introduced through ticket content or uploaded data | Manipulated output or data exposure | Input filtering, user awareness, least privilege, testing |
| AI output is sent directly to a customer | Incorrect, misleading, or unauthorized communication | Require authorized human approval |
| AI integration receives excessive permissions | Unauthorized access to tickets, data, or systems | RBAC, least privilege, periodic access review |
| Provider changes model behavior or retention terms | Reduced reliability or increased privacy risk | Vendor monitoring, change notification, reassessment |
| Users apply the tool to employment or customer eligibility decisions | Discrimination or consequential decision risk | Explicitly prohibited use and governance review |

## 7. Human Oversight Assessment

| Question | Response |
|---|---|
| Does the system make autonomous decisions? | No |
| Does the system execute actions in production systems? | No |
| Does the system send customer communications automatically? | No |
| Is human validation required before use of outputs? | Yes |
| Can a user override or reject AI recommendations? | Yes |
| Is there an escalation process for unsafe or inaccurate outputs? | Yes |
| Is the system approved for consequential decisions? | No |

## 8. Pre-Deployment Testing Requirements

The following testing must be completed before production deployment:

- Accuracy testing using representative and sanitized support-ticket scenarios
- Testing for hallucinations, incomplete summaries, and misleading troubleshooting recommendations
- Security testing of authentication, access control, APIs, logging, and integrations
- Prompt-injection and adversarial-input testing
- Privacy validation for data minimization, masking, retention, and deletion
- Usability testing with NOC and technical-support personnel
- Review of fallback procedures when the AI service is unavailable or produces unreliable output
- Verification that the system cannot execute privileged or production changes without approved human authorization

## 9. Assessment Decision

**Decision:** Conditionally approved for controlled pilot deployment.

The system may proceed only after completion of the required security, privacy, third-party, and testing activities. NovaAssist must remain limited to internal decision support and documentation assistance.

The following conditions apply:

- No autonomous actions or privileged production access
- No use for high-impact or consequential decisions
- No submission of credentials, secrets, payment information, or prohibited sensitive data
- Mandatory human validation of all material outputs
- Quarterly review of performance, security events, privacy concerns, and supplier changes
- Immediate reassessment after a material change, incident, or significant complaint

## 10. Residual Risk Statement

With the proposed controls, the residual risk is assessed as **Medium** and may be accepted for a limited pilot by the Business Owner, AI Governance Owner, and Information Security function.

Risk acceptance must be documented before production deployment.

## 11. Review Triggers

This assessment must be reviewed when:

- The provider, model, integrations, or deployment model changes
- New data categories or new user groups are added
- The system is connected to additional operational platforms
- An AI-related incident, privacy concern, security event, or material complaint occurs
- Regulatory, contractual, or policy requirements change
- Quarterly monitoring identifies degradation, drift, recurring inaccuracies, or control failures
