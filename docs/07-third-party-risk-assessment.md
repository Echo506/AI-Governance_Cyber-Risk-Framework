# Third-Party AI Risk Assessment

## 1. Purpose

This assessment evaluates the risks associated with using a third-party AI provider for NovaAssist.

NovaConnect will not select or deploy an external AI provider until the provider completes due diligence and the relevant business, security, privacy, procurement, and legal stakeholders approve the relationship.

## 2. Assessment Information

| Field | Details |
|---|---|
| Assessment ID | TPRM-AI-001 |
| Service | Third-party generative AI platform for NovaAssist |
| Provider | To be selected |
| Service Criticality | Medium |
| Data Sensitivity | Medium to High |
| Deployment Model | Cloud-based AI service accessed through approved enterprise accounts and APIs |
| Business Owner | Director of Operations |
| Technical Owner | IT Automation and Security Team |
| Assessment Owner | Procurement and Third-Party Risk Management |
| Assessment Status | Pre-procurement / vendor selection stage |
| Review Frequency | Annually and upon material change |

## 3. Inherent Risk Profile

| Risk Area | Inherent Risk | Rationale |
|---|---|---|
| Data confidentiality | High | The system may process internal operational data and limited customer information |
| Privacy | High | Ticket content could include personal or customer contact information |
| Security | High | API integrations, identities, access permissions, and provider infrastructure may be targeted |
| Availability | Medium | Service disruption could affect support productivity but should not stop core operations |
| Compliance | Medium | Privacy, contractual, customer, and cross-border data requirements may apply |
| Model reliability | Medium | Generative AI can produce inaccurate, incomplete, or misleading output |
| Third-party concentration | Medium | Dependence on one provider may create resilience and negotiating risk |
| Reputational impact | Medium | Poor output or data exposure could harm customer trust |

## 4. Required Due Diligence

The provider must provide evidence or documented responses for the following areas before contract execution.

| Assessment Area | Required Question or Evidence | Minimum Expectation |
|---|---|---|
| Corporate Profile | Who owns and operates the service? What is the provider's financial and operational maturity? | Provider identity, operating history, relevant business information |
| Service Description | What model, platform, API, hosting model, and service features are provided? | Clear technical and commercial description |
| Data Ownership | Does NovaConnect retain ownership and control of submitted data and generated outputs? | Contractual confirmation |
| Data Use | Will NovaConnect data be used to train, fine-tune, evaluate, or improve the provider's models? | Default prohibition unless explicitly approved |
| Data Retention | How long are prompts, files, API requests, logs, and outputs retained? | Configurable and documented retention period |
| Data Deletion | Can NovaConnect request deletion of data, prompts, outputs, and account artifacts? | Defined deletion process and evidence |
| Data Residency | Where is data stored and processed? Are cross-border transfers involved? | Documented locations and applicable safeguards |
| Access Control | Does the service support SSO, MFA, RBAC, least privilege, and administrative controls? | Enterprise-grade identity controls |
| Encryption | Is data encrypted in transit and at rest? | Industry-standard encryption |
| API Security | How are API keys, service accounts, webhooks, and integration permissions secured? | Secure authentication and scoped permissions |
| Logging | Are user activity, administrative actions, API events, and security events logged? | Sufficient logs for investigation and monitoring |
| Security Assurance | Does the provider maintain recognized security assurance reports or certifications? | Current independent assurance evidence where available |
| Vulnerability Management | How does the provider identify, remediate, and disclose security vulnerabilities? | Documented vulnerability and patch-management process |
| Incident Notification | What are the notification timelines for security incidents, breaches, or service disruptions? | Contractual notification and escalation commitments |
| Subprocessors | Does the provider use subprocessors, and can NovaConnect review changes? | Subprocessor transparency and notification process |
| AI Model Changes | How are model updates, feature changes, safety changes, or behavior changes communicated? | Prior notice and change-management process |
| Reliability and SLAs | What availability, support, recovery, and service-credit commitments exist? | Defined SLA and support model |
| Responsible AI | How does the provider address security, privacy, safety, bias, transparency, and misuse? | Documented responsible-AI practices |
| Exit Strategy | How can NovaConnect export data, migrate services, and terminate access? | Contractual exit and data-return provisions |

## 5. Security and Privacy Requirements

The selected provider must support or contractually agree to:

- Enterprise identity federation using SSO and multi-factor authentication
- Role-based access control for users and administrators
- Encryption of data in transit and at rest
- Secure, scoped, and auditable API access
- Data minimization and configurable retention settings
- No training on NovaConnect confidential data without explicit written approval
- Prompt, file, and output deletion capabilities
- Logging of authentication, access, administrative activity, and relevant API events
- Incident notification and cooperation obligations
- Disclosure of material changes to data use, model behavior, security posture, hosting, or subprocessors
- Documented business continuity, disaster recovery, and service availability commitments
- Contractual rights to terminate the service and obtain data deletion confirmation

## 6. Vendor Risk Questionnaire Summary

| Question | Expected Response | Assessment Result |
|---|---|---|
| Does the provider use customer data to train models by default? | No | Pending vendor response |
| Can data retention be configured or disabled? | Yes | Pending vendor response |
| Does the service support SSO, MFA, and RBAC? | Yes | Pending vendor response |
| Are API permissions scoped and auditable? | Yes | Pending vendor response |
| Does the provider provide security assurance evidence? | Yes | Pending vendor response |
| Does the provider notify customers of incidents within contractually agreed timelines? | Yes | Pending vendor response |
| Does the provider disclose subprocessors and material changes? | Yes | Pending vendor response |
| Can NovaConnect export and delete its data at termination? | Yes | Pending vendor response |
| Are model changes communicated before implementation when possible? | Yes | Pending vendor response |
| Does the provider maintain continuity and recovery procedures? | Yes | Pending vendor response |

## 7. Required Contract Clauses

The contract, order form, or data processing agreement should address:

- Permitted use of NovaConnect data
- Data ownership and intellectual-property rights
- Prohibition or opt-out for model training using NovaConnect data
- Data processing locations and cross-border transfer safeguards
- Data retention, deletion, return, and destruction requirements
- Security control requirements and audit evidence
- SSO, MFA, RBAC, logging, and secure API requirements
- Incident notification, investigation, and cooperation obligations
- Subprocessor disclosure and change notification
- Service-level agreement, support, business continuity, and disaster recovery commitments
- Liability, indemnification, and regulatory cooperation provisions
- Termination rights and exit support
- Right to reassess the provider after a material change or security incident

## 8. Decision Criteria

The provider may be approved only if:

- The provider meets the minimum security, privacy, and contractual requirements.
- Identified risks are documented in the AI risk register.
- Unacceptable data-use, retention, or training practices are removed or contractually restricted.
- Required security controls are verified before production integration.
- The Business Owner, Information Security, Privacy/Legal, and Procurement functions approve the decision.
- Any remaining Medium or higher residual risks are formally accepted.

## 9. Preliminary Decision

**Decision:** Not approved for production use until vendor selection, due diligence, contractual review, security review, and privacy review are completed.

## 10. Reassessment Triggers

This assessment must be updated if the provider:

- Changes data retention, data use, hosting, model, or security practices
- Adds or changes subprocessors
- Experiences a security incident, privacy incident, or material service outage
- Changes ownership, financial condition, or service scope
- Introduces significant new AI features or autonomous capabilities
- Fails to meet service-level, security, or contractual commitments
