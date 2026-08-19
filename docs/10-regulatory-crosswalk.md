# AI Governance Regulatory Crosswalk

## 1. Purpose

This document identifies selected regulatory and standards-based considerations relevant to NovaConnect's AI governance framework.

It is a portfolio crosswalk for educational purposes. It is not legal advice, a legal compliance assessment, or a certification statement.

## 2. Applicability Statement

NovaAssist is an internal generative AI assistant used to support NOC and technical-support operations.

The intended use case does not make autonomous or consequential decisions about employment, credit, insurance, housing, education, healthcare, legal status, customer eligibility, service termination, or access to essential services.

Therefore, some obligations intended for high-risk or consequential AI systems may not directly apply to NovaAssist. However, the governance concepts are used as practical controls and as preparation for future use cases that could involve higher risk.

## 3. Crosswalk

| Source | Relevant Concept | NovaConnect Implementation | Evidence |
|---|---|---|---|
| NIST AI RMF | Govern: policies, accountability, risk culture, training, documentation, and oversight | AI Governance Policy; defined owners; approval workflow; user training | `02-ai-governance-policy.md`, `03-ai-system-inventory.md` |
| NIST AI RMF | Map: context of use, stakeholders, impacts, data, human oversight, third-party context | Document business purpose, data categories, stakeholders, limits, and human review | `03-ai-system-inventory.md`, `04-ai-impact-assessment.md` |
| NIST AI RMF | Measure: testing, evaluation, validation, privacy, security, reliability, monitoring, and drift | Perform accuracy, security, prompt-injection, privacy, and quality testing; monitor KPIs and KRIs | `04-ai-impact-assessment.md`, `09-monitoring-and-kpis.md` |
| NIST AI RMF | Manage: treatment, response, monitoring, third-party management, incidents, and improvement | Maintain risk register, supplier review, incident response, escalation, and reassessment process | `05-ai-risk-register.md`, `07-third-party-risk-assessment.md`, `08-ai-incident-response-plan.md` |
| NIST CSF 2.0 | Govern: policy, roles, oversight, risk strategy, and supply-chain risk management | AI policy, assigned owners, risk methodology, provider assessment, and executive reporting | `02-ai-governance-policy.md`, `06-control-mapping.md` |
| NIST CSF 2.0 | Identify: asset inventory, data inventory, data flows, risk assessment, supplier assessment | Inventory NovaAssist, integrations, data categories, providers, risks, and lifecycle status | `03-ai-system-inventory.md`, `05-ai-risk-register.md` |
| NIST CSF 2.0 | Protect: access control, training, data security, secure configuration, resilience | RBAC, MFA, least privilege, encryption, data minimization, user training, secure APIs | `02-ai-governance-policy.md`, `06-control-mapping.md` |
| NIST CSF 2.0 | Detect, Respond, Recover: monitoring, event analysis, incident handling, recovery, communications | SIEM and audit logging, incident severity, containment, recovery validation, post-incident review | `08-ai-incident-response-plan.md`, `09-monitoring-and-kpis.md` |
| ISO/IEC 42001 | AI management system, governance, risk management, lifecycle management, performance evaluation, continual improvement | Establish documented governance, risk assessment, controls, roles, monitoring, review, and improvement | Entire project repository |
| ISO/IEC TR 24368 | Ethical and societal concerns, including privacy, transparency, fairness, and human impacts | Evaluate intended use, stakeholders, privacy, limitations, human oversight, quality, and potential misuse | `04-ai-impact-assessment.md` |
| GDPR | Lawfulness, fairness, transparency, purpose limitation, data minimization, security, accountability, and data-subject rights when personal data is processed | Limit data processing, protect personal data, use approved providers, conduct privacy review, apply retention and access controls | `02-ai-governance-policy.md`, `03-ai-system-inventory.md`, `04-ai-impact-assessment.md` |
| EU AI Act | Risk-based approach, human oversight, documentation, transparency, data governance, risk management, and monitoring; applicability depends on role and system classification | Classify the use case, preserve documentation, require human review, monitor material changes, reassess if use evolves toward high-risk functions | `03-ai-system-inventory.md`, `04-ai-impact-assessment.md`, `09-monitoring-and-kpis.md` |
| Colorado SB24-205 | For high-risk systems: reasonable care, risk-management policy and program, impact assessment, annual review, consumer notice, and human appeal where applicable | Maintain a risk-management program, impact assessment, monitoring, documentation, and human oversight; reassess if a future use case could make consequential decisions | `02-ai-governance-policy.md`, `04-ai-impact-assessment.md`, `09-monitoring-and-kpis.md` |

## 4. GDPR Considerations

When NovaAssist processes personal data, NovaConnect should confirm:

- A valid legal basis for processing exists
- Processing has a defined and documented purpose
- Only data necessary for the approved purpose is processed
- Personal data is protected through appropriate technical and organizational measures
- Retention periods are defined and enforced
- Data-subject rights can be supported where applicable
- Cross-border data transfers are assessed when provider processing occurs outside the relevant jurisdiction
- Privacy impact assessment requirements are evaluated when processing may create high risk for individuals
- Processor or vendor contracts address data processing, confidentiality, security, and breach notification

## 5. EU AI Act Considerations

NovaConnect should reassess applicability if it becomes a provider, deployer, importer, distributor, or authorized representative in relation to an AI system covered by the EU AI Act.

Additional review is required if the AI use case:

- Makes or materially influences a consequential decision about an individual
- Is used in employment, recruitment, worker management, education, credit, insurance, law enforcement, migration, essential public services, or critical infrastructure
- Uses biometric information or processes sensitive data in a way that increases risk
- Interacts directly with customers or the public without adequate disclosure
- Changes from internal decision support to automated customer-facing action
- Is materially modified, expanded, or integrated into higher-impact operational processes

## 6. Colorado SB24-205 Considerations

If NovaConnect conducts business in Colorado and deploys a high-risk AI system, it should evaluate whether the system is used to make or be a substantial factor in making consequential decisions.

Where applicable, the organization should be prepared to demonstrate:

- A risk-management policy and program
- An impact assessment
- Ongoing or annual review of the system
- Measures to identify and mitigate algorithmic discrimination
- Appropriate consumer notifications and transparency
- A method to correct incorrect personal data when relevant
- A human appeal or review process for adverse consequential decisions when technically feasible
- Incident and issue management processes
- Documentation supporting reasonable care and corrective action

## 7. Control Gaps and Next Actions

| Area | Current Portfolio Status | Next Action |
|---|---|---|
| Governance policy | Documented | Obtain formal stakeholder approval in a real-world deployment |
| AI inventory | Documented for NovaAssist | Expand inventory for each future AI system |
| Impact assessment | Documented for proposed use case | Repeat before any material change or production deployment |
| Security controls | Defined conceptually | Validate implementation through technical design and security testing |
| Privacy controls | Defined conceptually | Complete formal privacy review and data-flow validation |
| Third-party due diligence | Assessment template completed | Select vendor and collect actual evidence |
| Monitoring | KPI and KRI plan documented | Configure reporting, logs, alerts, and quality sampling |
| Regulatory review | Crosswalk documented | Obtain jurisdiction-specific legal review where needed |

## 8. Conclusion

NovaConnect's framework uses a risk-based approach to AI adoption. The organization will apply governance, documentation, security, privacy, human oversight, monitoring, supplier management, incident response, and continuous improvement in proportion to the AI system's intended use and risk level.
