# AI System Inventory

## 1. Purpose

This inventory records AI systems used by NovaConnect Services and provides a baseline for governance, risk assessment, security reviews, privacy reviews, monitoring, and lifecycle management.

Each AI system must be entered into this inventory before production use or material modification.

## 2. System Record

| Field | Details |
|---|---|
| AI System ID | AI-001 |
| System Name | NovaAssist |
| System Type | Generative AI assistant |
| Status | Proposed portfolio use case / Pre-deployment |
| Business Unit | NOC and Technical Support Operations |
| Business Owner | Director of Operations |
| Technical Owner | IT Automation and Security Team |
| AI Governance Owner | GRC / Information Security Manager |
| Primary Users | NOC analysts, technical-support agents, service desk leads, SOC analysts |
| Deployment Model | Third-party cloud-based AI service integrated through approved APIs |
| Provider | To be selected and approved through third-party risk management |
| Hosting Location | Cloud environment; provider location and data residency must be documented before deployment |
| Date Added | 2026-08-19 |
| Review Frequency | Quarterly and upon material change |

## 3. Approved Business Purpose

NovaAssist is intended to support internal NOC and technical-support teams by:

- Summarizing support tickets and outage updates
- Drafting internal and customer-facing response suggestions
- Classifying ticket categories and priority recommendations
- Retrieving approved technical knowledge-base content
- Identifying incomplete ticket fields or missing troubleshooting details
- Assisting analysts with incident documentation and closure notes

NovaAssist is a decision-support tool. It does not independently execute changes, close incidents, modify network configurations, send customer communications, or make consequential decisions.

## 4. Data Classification

| Data Category | Examples | Classification | Approved for AI Processing? | Conditions |
|---|---|---|---|---|
| Public information | Published knowledge-base articles, public service notices | Public | Yes | Use approved sources only |
| Internal operational data | Ticket summaries, troubleshooting steps, non-sensitive outage details | Internal | Yes | Remove unnecessary identifiers |
| Customer business information | Company name, circuit reference, account contact details | Confidential | Conditional | Only through approved provider and approved workflow |
| Personal data | Names, email addresses, phone numbers, customer identifiers | Restricted | Conditional | Minimize, mask, and confirm privacy approval |
| Security event data | Alerts, IP addresses, indicators, incident notes | Restricted | Conditional | Security approval and controlled access required |
| Credentials and secrets | Passwords, tokens, API keys, private keys | Highly Restricted | No | Prohibited from prompts, files, and integrations |
| Regulated or sensitive data | Payment data, health data, identity documents | Highly Restricted | No | Prohibited unless formally approved through a separate assessment |

## 5. Data Flow Summary

1. An authorized user accesses NovaAssist through the approved company account.
2. The user submits approved ticket context, sanitized operational details, or a query against the approved knowledge base.
3. NovaAssist processes the input through the authorized AI provider and returns a draft, summary, classification suggestion, or knowledge response.
4. The user validates the output before using it in operational activities or customer communication.
5. System activity, access events, and relevant audit logs are retained according to approved logging and retention requirements.

## 6. Integrations

| Integration | Purpose | Data Exchanged | Approval Status | Security Requirement |
|---|---|---|---|---|
| Ticketing platform | Ticket summarization and categorization | Approved ticket metadata and sanitized content | Proposed | API authentication, least privilege, logging |
| Knowledge base | Retrieval of approved support procedures | Internal technical documentation | Proposed | Read-only access, content review |
| Identity provider | User authentication and role assignment | User identity and access attributes | Required | SSO, MFA, role-based access control |
| SIEM / logging platform | Monitoring and investigation | Access logs, API events, security alerts | Proposed | Secure log forwarding, retention, alerting |

## 7. Risk Classification

| Risk Domain | Initial Rating | Rationale |
|---|---|---|
| Cybersecurity | Medium | Risk of prompt injection, unauthorized access, insecure integrations, and data exposure |
| Privacy | Medium | The tool may process ticket information containing personal or customer-related data |
| Operational | Medium | Inaccurate summaries or recommendations may affect ticket handling and incident documentation |
| Legal and Compliance | Medium | The use case requires review of contractual, privacy, and customer-notification obligations |
| Third-Party | Medium | NovaConnect may depend on an external AI provider and cloud service |
| Bias and Fairness | Low | The system supports operational work and does not make employment, credit, eligibility, or other consequential decisions |
| Overall Classification | Medium | Deployment requires documented approval, security controls, user training, and ongoing monitoring |

## 8. Human Oversight Requirements

- Users must validate AI-generated outputs before acting on them.
- AI output must not be the sole basis for operational, security, customer, or business decisions.
- Customer-facing messages must be reviewed by authorized personnel before sending.
- Changes to network devices, security tools, access permissions, or production systems require existing change-management and authorization processes.
- Suspicious, inaccurate, biased, harmful, or unsafe outputs must be reported through the AI incident process.

## 9. Minimum Control Requirements

- Single sign-on and multi-factor authentication
- Role-based access control and least privilege
- Approved APIs and secure secret management
- Encryption in transit and at rest
- Audit logging for user access, integration calls, and administrative changes
- Data minimization, masking, and prompt-handling guidance
- Approved retention and deletion requirements
- Third-party due diligence and contract review
- User training on secure and responsible AI use
- Incident response and escalation procedures
- Quarterly access, performance, and risk reviews

## 10. Lifecycle Status

| Lifecycle Stage | Status | Required Evidence |
|---|---|---|
| Use case intake | Complete | Approved intake form |
| Inventory registration | Complete | This inventory record |
| AI impact assessment | Pending | `04-ai-impact-assessment.md` |
| Security review | Pending | Security review record |
| Privacy review | Pending | Privacy assessment record |
| Third-party review | Pending | Supplier assessment |
| Approval for deployment | Pending | Approval decision and risk acceptance, if needed |
| Production monitoring | Not started | KPI, KRI, and logging evidence |
| Retirement / decommissioning | Not applicable | Decommissioning plan when required |

## 11. Review and Change Management

This inventory record must be updated when there is a material change to:

- The AI model, provider, deployment environment, or hosting location
- The intended business purpose or user population
- Data categories, data sources, retention practices, or integrations
- Access roles, authentication methods, or permissions
- Security controls or monitoring capabilities
- Legal, regulatory, contractual, or customer requirements
- Risk classification, incidents, audit findings, or performance concerns
