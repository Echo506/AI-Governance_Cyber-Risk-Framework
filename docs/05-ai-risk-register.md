# AI Risk Register

## 1. Risk Rating Methodology

### Likelihood Scale

| Score | Rating | Description |
|---|---|---|
| 1 | Rare | Unlikely to occur under normal conditions |
| 2 | Unlikely | Could occur, but not expected frequently |
| 3 | Possible | May occur during normal operations |
| 4 | Likely | Expected to occur without effective controls |
| 5 | Almost Certain | Expected to occur repeatedly or imminently |

### Impact Scale

| Score | Rating | Description |
|---|---|---|
| 1 | Insignificant | Minimal operational or business impact |
| 2 | Minor | Limited disruption; manageable within a team |
| 3 | Moderate | Noticeable operational, customer, or compliance impact |
| 4 | Major | Significant service, security, customer, or regulatory impact |
| 5 | Severe | Critical business disruption, major data exposure, or serious legal impact |

### Risk Score

Risk Score = Likelihood × Impact

| Score | Rating | Required Response |
|---|---|---|
| 1-4 | Low | Monitor and manage through standard procedures |
| 5-9 | Medium | Implement and track defined controls |
| 10-16 | High | Formal treatment plan and management oversight required |
| 17-25 | Critical | Do not deploy or continue use without executive authorization and immediate treatment |

## 2. Risk Register

| ID | Risk Description | Category | Likelihood | Impact | Inherent Risk | Existing / Planned Controls | Risk Owner | Residual Risk | Treatment Plan | Status |
|---|---|---|---:|---:|---|---|---|---|---|---|
| AI-R-001 | Sensitive customer, operational, or personal data is entered into an unapproved AI tool or processed beyond the approved purpose | Privacy / Data Protection | 3 | 4 | High (12) | Approved tools only, data-classification policy, user training, prompt guidance, DLP where available, privacy review | Privacy and AI Governance Owner | Medium (6) | Conduct quarterly user awareness reviews and monitor policy exceptions | Open |
| AI-R-002 | AI generates inaccurate, incomplete, or fabricated technical guidance that affects ticket handling or customer communication | Operational / Reliability | 4 | 3 | High (12) | Human review, approved knowledge-base grounding, quality sampling, user training, escalation process | NOC Operations Manager | Medium (6) | Establish monthly accuracy sampling and error-rate KPI | Open |
| AI-R-003 | Prompt injection or malicious ticket content manipulates the AI system or causes unsafe output | Cybersecurity | 3 | 4 | High (12) | Input validation, access restrictions, user training, prompt-injection testing, logging, least privilege | Information Security Manager | Medium (6) | Include adversarial testing before pilot and after material changes | Open |
| AI-R-004 | Excessive integration permissions allow unauthorized access to tickets, customer records, or operational systems | IAM / Cybersecurity | 3 | 5 | High (15) | RBAC, SSO, MFA, API scoping, least privilege, access reviews, secure secret management | Technical Owner | Medium (5) | Complete integration security review before deployment | Open |
| AI-R-005 | An external AI provider changes its retention, data-processing, security, or model behavior without adequate notice | Third-Party / Compliance | 3 | 4 | High (12) | Supplier due diligence, contract clauses, change notification requirements, periodic reviews, exit strategy | Procurement and Third-Party Risk Owner | Medium (6) | Complete supplier assessment and contract review | Open |
| AI-R-006 | Users treat AI output as verified information and bypass established troubleshooting, change, or incident procedures | Operational / Governance | 3 | 4 | High (12) | Policy, mandatory human validation, training, approval workflows, no autonomous actions | NOC Operations Manager | Medium (6) | Review usage patterns and reinforce training quarterly | Open |
| AI-R-007 | AI service outage, latency, or degradation disrupts support workflows and creates dependency on the tool | Resilience / Availability | 3 | 3 | Medium (9) | Manual fallback procedures, documented standard operating procedures, provider SLA review, business continuity planning | Technical Owner | Low (3) | Test manual fallback process during pilot | Open |
| AI-R-008 | Inadequate logs prevent investigation of misuse, data exposure, or harmful AI outputs | Detection / Incident Response | 2 | 4 | Medium (8) | Audit logging, SIEM integration, retention requirements, incident reporting process | Information Security Manager | Low (4) | Validate log coverage and alerting during security review | Open |
| AI-R-009 | AI is repurposed for high-impact decisions involving customers, employees, or service eligibility without appropriate approval | Legal / Ethical / Governance | 2 | 5 | High (10) | Explicit prohibited-use policy, intake and approval process, AI inventory, periodic review | AI Governance Owner | Low (2) | Monitor for scope changes and require reassessment before new use cases | Open |
| AI-R-010 | AI-generated customer content is inaccurate, misleading, or sent without authorized review | Customer / Reputational | 3 | 4 | High (12) | Mandatory human review, approved communication workflow, user training, quality checks | Technical Support Manager | Medium (6) | Audit a sample of AI-assisted communications monthly | Open |

## 3. Risk Treatment Priorities

### Priority 1: Before Pilot Deployment

- Complete security review for AI integrations, identity controls, API permissions, logging, and secrets management
- Complete privacy review and confirm prohibited-data handling requirements
- Complete third-party due diligence and contract review
- Perform prompt-injection, adversarial-input, and accuracy testing
- Train pilot users on permitted use, prohibited data, human validation, and incident reporting
- Establish manual fallback procedures

### Priority 2: During Pilot Deployment

- Monitor AI output accuracy and user feedback
- Review access logs, integration events, and security alerts
- Track policy violations, unsafe outputs, data-handling issues, and near misses
- Measure ticket-quality improvement and time savings without reducing review quality
- Update risks and controls based on observed results

### Priority 3: Before Production Expansion

- Review pilot results and residual-risk acceptance
- Confirm that controls are operating effectively
- Expand user access only after approval
- Reassess data categories, integrations, provider commitments, and regulatory requirements
- Define a formal monitoring, KPI, and KRI reporting process

## 4. Risk Review Schedule

| Activity | Frequency | Owner |
|---|---|---|
| AI risk-register review | Monthly during pilot; quarterly after deployment | AI Governance Owner |
| Access review | Quarterly | Technical Owner and Information Security |
| AI output-quality sampling | Monthly | NOC and Technical Support Operations |
| Security log and alert review | Continuous / operationally defined | Information Security / SOC |
| Provider risk review | Annually and upon material change | Procurement and Third-Party Risk |
| Policy review | Annually and upon material change | AI Governance Owner |
| Impact-assessment refresh | Annually and upon material change | AI Governance Owner |

## 5. Risk Acceptance

Residual risks rated Medium or higher require documented acceptance by the appropriate Business Owner and AI Governance Owner.

Residual risks rated High or Critical require executive approval and may require delaying deployment until controls reduce the risk to an acceptable level.
