# AI Incident Response Plan

## 1. Purpose

This plan defines how NovaConnect Services detects, triages, contains, investigates, communicates, recovers from, and learns from AI-related incidents.

It applies to NovaAssist and any future AI system approved for use by NovaConnect.

## 2. Scope

An AI-related incident includes any event involving an AI system that may affect confidentiality, integrity, availability, privacy, safety, service quality, customer trust, legal obligations, or business operations.

Examples include:

- Unauthorized access to an AI platform or AI integration
- Exposure of confidential, customer, personal, or sensitive data
- Credentials, secrets, tokens, or API keys entered into an AI tool
- Prompt injection, jailbreak, adversarial input, or model manipulation
- Harmful, inaccurate, biased, misleading, or unsafe AI output
- Unapproved autonomous action or excessive AI integration permissions
- Material degradation in output quality, reliability, or system behavior
- AI provider security incident, breach, outage, or major service disruption
- Violation of the AI Governance Policy or approved use-case scope

## 3. Incident Severity Levels

| Severity | Description | Example | Response Target |
|---|---|---|---|
| SEV-1 Critical | Major data exposure, confirmed unauthorized access, serious service impact, or significant legal/regulatory risk | Sensitive customer data exposed through AI provider or compromised integration | Immediate escalation; begin response within 1 hour |
| SEV-2 High | Significant security, privacy, operational, or customer impact requiring urgent containment | Credentials submitted to an unapproved AI tool; prompt injection causes unsafe output | Escalate and begin response within 4 hours |
| SEV-3 Medium | Contained issue with moderate impact or credible potential for harm | Repeated inaccurate outputs affecting ticket quality; limited policy breach | Triage within 1 business day |
| SEV-4 Low | Minor issue, near miss, or improvement opportunity | Single inaccurate recommendation caught during review | Record and review within 5 business days |

## 4. Roles and Responsibilities

| Role | Responsibilities |
|---|---|
| Incident Commander | Coordinates response, assigns actions, confirms severity, and manages incident closure |
| AI Governance Owner | Assesses policy, risk, oversight, and use-case implications; coordinates post-incident review |
| Information Security / SOC | Investigates security events, preserves evidence, contains threats, and manages security escalation |
| Technical Owner | Disables integrations if needed, reviews configuration, preserves logs, and supports recovery |
| Business Owner | Evaluates operational impact, provides business decisions, and coordinates affected teams |
| Privacy / Legal / Compliance | Assesses privacy, contractual, notification, legal, and regulatory requirements |
| Procurement / Third-Party Risk | Coordinates with the AI provider and reviews supplier obligations |
| Communications Lead | Coordinates approved internal, customer, partner, or public communications when needed |
| End Users | Stop unsafe activity, preserve relevant details, and report suspected incidents immediately |

## 5. Detection and Reporting

AI incidents may be detected through:

- User reports
- Security alerts, SIEM monitoring, or DLP alerts
- AI platform audit logs
- API monitoring and integration logs
- Output-quality sampling
- Customer complaints or escalation tickets
- Privacy complaints or data-subject requests
- Provider notifications
- Internal audits, control reviews, or testing exercises

Anyone who suspects an AI incident must report it through the approved incident-management channel and include:

- Date and time of discovery
- AI system involved
- Description of the event
- Data, users, integrations, or customers potentially affected
- Screenshots, prompts, outputs, ticket IDs, logs, or other available evidence
- Immediate actions already taken

## 6. Response Procedure

### 6.1 Triage and Validation

1. Record the incident in the incident-management system.
2. Confirm whether the event involves an approved AI system, AI provider, user activity, integration, prompt, output, or data flow.
3. Assign an initial severity level.
4. Identify the AI system owner, technical owner, business owner, and relevant security or privacy contacts.
5. Preserve relevant evidence, including logs, prompts, outputs, timestamps, user identifiers, configuration details, and integration activity.
6. Escalate to the Incident Commander for SEV-1 and SEV-2 incidents.

### 6.2 Containment

Depending on the incident, containment actions may include:

- Disabling the affected user account or revoking active sessions
- Rotating exposed credentials, tokens, API keys, or secrets
- Disabling the AI integration, API connection, plugin, or workflow
- Temporarily suspending access to the AI platform
- Blocking unsafe prompts, inputs, data sources, or uploaded files
- Restricting permissions or reverting excessive access
- Pausing customer-facing or operational AI-assisted workflows
- Engaging the AI provider's security or support team
- Preserving a copy of evidence before changes are made

### 6.3 Investigation and Analysis

The response team must determine:

- What happened and when it began
- Which users, systems, data, integrations, or customers were affected
- Whether confidential, personal, restricted, or highly restricted data was exposed
- Whether the event involved unauthorized access, misuse, prompt injection, provider failure, policy violation, or model behavior
- Whether the AI output was relied upon and what operational or customer impact resulted
- Whether the incident is isolated or indicates a broader control failure
- Root cause, contributing factors, and required corrective actions

### 6.4 Eradication and Remediation

Actions may include:

- Removing malicious prompts, files, integrations, or configurations
- Revoking and replacing compromised credentials or secrets
- Correcting access-control, logging, retention, or configuration weaknesses
- Updating prompts, guardrails, knowledge sources, or user workflows
- Applying provider fixes or security updates
- Retraining users or restricting access
- Updating the AI risk register, impact assessment, and control mapping
- Initiating vendor remediation or contractual escalation

### 6.5 Recovery

Before restoring or expanding use of the affected AI system:

1. Verify that containment and remediation actions are complete.
2. Confirm that access, credentials, integrations, and configurations are secure.
3. Validate output quality, reliability, and safety through testing.
4. Confirm that required logs, monitoring, and alerting are operational.
5. Obtain approval from the Technical Owner, Information Security, and AI Governance Owner.
6. Restore service gradually when the incident involved significant risk.
7. Confirm normal operational status and document the recovery decision.

## 7. Communications and Notifications

Communications must be accurate, timely, and coordinated through approved channels.

| Audience | When to Notify | Owner |
|---|---|---|
| Information Security / SOC | All suspected security-related AI incidents | Incident Reporter or Technical Owner |
| AI Governance Owner | All SEV-1, SEV-2, and material governance incidents | Incident Commander |
| Business Owner | Incidents affecting operations, customers, or service quality | Incident Commander |
| Privacy / Legal / Compliance | Potential personal-data exposure, contractual, legal, or regulatory impact | Incident Commander |
| AI Provider | Provider-related incident, suspected platform weakness, outage, or data-processing issue | Procurement / Technical Owner |
| Customers or Partners | When required by contract, law, regulation, or approved incident communications process | Communications Lead with Legal approval |
| Executive Leadership | SEV-1 incidents and significant SEV-2 incidents | Incident Commander |

## 8. Evidence Preservation

The response team must preserve relevant evidence, including:

- Incident tickets and timeline
- User prompts, AI outputs, and uploaded content where legally and operationally appropriate
- Access logs, API logs, audit logs, and SIEM events
- Identity, entitlement, and configuration records
- Screenshots, system messages, alerts, and provider notices
- Communications with the provider and affected stakeholders
- Decisions, approvals, containment actions, and recovery actions

Evidence must be handled according to NovaConnect information-security, privacy, legal-hold, and record-retention requirements.

## 9. Post-Incident Review

A post-incident review is required for all SEV-1 and SEV-2 incidents and for recurring SEV-3 events.

The review must include:

- Incident summary and timeline
- Root cause and contributing factors
- Data, customer, operational, security, and compliance impact
- Effectiveness of detection, containment, response, and recovery
- Control gaps and corrective actions
- Updates needed to policies, procedures, training, inventories, assessments, risk registers, or supplier requirements
- Assigned owners and due dates for remediation actions
- Lessons learned shared with relevant stakeholders

## 10. Testing and Exercises

NovaConnect will test this plan at least annually and after significant changes to AI systems, integrations, providers, or risk exposure.

Exercises may include:

- Prompt-injection scenario
- Sensitive data submitted to an unapproved AI tool
- Compromised AI API key
- Provider outage or service degradation
- Harmful or inaccurate customer-facing AI output
- Excessive AI permissions or unauthorized integration access
- Suspected provider data-processing or retention violation

## 11. Framework Alignment

This plan supports:

- NIST AI RMF: Manage, Measure, Govern
- NIST CSF 2.0: Detect, Respond, Recover
- AI governance requirements for monitoring, incident handling, accountability, and continuous improvement

## 12. Plan Review

This plan must be reviewed annually and whenever a major AI incident, material system change, provider change, regulatory change, or significant control gap occurs.
