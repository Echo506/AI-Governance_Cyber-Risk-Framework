# AI Monitoring, KPIs, and KRIs

## 1. Purpose

This document defines how NovaConnect Services will monitor NovaAssist after deployment.

Monitoring is designed to confirm that the AI system remains secure, reliable, useful, compliant with approved use, and aligned with the organization's risk tolerance.

## 2. Monitoring Objectives

NovaConnect will monitor NovaAssist to:

- Identify security events, misuse, unauthorized access, and abnormal integration activity
- Detect data-handling issues, policy violations, and potential privacy concerns
- Measure accuracy, reliability, output quality, and user reliance on AI-generated content
- Detect model drift, performance degradation, and changes in AI provider behavior
- Measure operational value without compromising customer service, security, or compliance
- Identify incidents, near misses, control gaps, and improvement opportunities
- Support periodic risk reviews and governance reporting

## 3. Monitoring Roles

| Role | Monitoring Responsibilities |
|---|---|
| AI Governance Owner | Reviews governance metrics, KRIs, risk trends, policy exceptions, and remediation progress |
| Technical Owner | Monitors integrations, system configuration, access, API activity, service performance, and platform changes |
| Information Security / SOC | Monitors security logs, access anomalies, alerts, suspicious activity, and AI-related incidents |
| NOC and Technical Support Operations | Performs output-quality sampling, tracks operational errors, validates user feedback, and identifies workflow issues |
| Privacy / Legal / Compliance | Reviews data-protection concerns, retention, complaints, regulatory changes, and material policy issues |
| Procurement / Third-Party Risk | Monitors supplier performance, material provider changes, contract obligations, and service issues |
| Business Owner | Reviews business value, operational impact, adoption, and risk acceptance decisions |

## 4. Key Performance Indicators

| KPI ID | Metric | Formula or Measurement | Target | Frequency | Owner |
|---|---|---|---|---|---|
| KPI-01 | AI output acceptance rate | Percentage of sampled AI outputs accepted after human review | At least 85% during mature operation | Monthly | NOC Operations |
| KPI-02 | Output correction rate | Percentage of sampled AI outputs requiring material correction | Less than 15% | Monthly | NOC Operations |
| KPI-03 | Ticket documentation time reduction | Average documentation time before AI versus after AI use | At least 20% improvement without quality loss | Monthly | Business Owner |
| KPI-04 | Ticket quality score | Quality score based on completeness, clarity, accuracy, and required fields | At least 90% compliance | Monthly | Technical Support Manager |
| KPI-05 | Human review compliance | Percentage of sampled material outputs with documented human validation | 100% | Monthly | AI Governance Owner |
| KPI-06 | Approved-use compliance | Percentage of usage activity within approved use-case scope | 100% | Monthly | AI Governance Owner |
| KPI-07 | User training completion | Percentage of authorized users completing required AI training | 100% before access; 100% annually | Monthly | AI Governance Owner |
| KPI-08 | AI service availability | Provider or integration availability during agreed service window | At least 99.5%, subject to contract | Monthly | Technical Owner |
| KPI-09 | Time to resolve AI issues | Average time from issue report to closure | Defined by severity target | Monthly | Incident Commander |
| KPI-10 | Remediation completion rate | Percentage of agreed AI control actions completed by due date | At least 90% | Quarterly | AI Governance Owner |

## 5. Key Risk Indicators

| KRI ID | Risk Indicator | Threshold | Escalation Action | Owner |
|---|---|---|---|---|
| KRI-01 | AI outputs requiring material correction | More than 15% in a monthly sample | Review use case, knowledge sources, user workflow, and controls | NOC Operations |
| KRI-02 | Confirmed data-policy violations | Any confirmed violation involving restricted or highly restricted data | Immediate incident triage and governance review | Information Security / Privacy |
| KRI-03 | Unauthorized access attempts | Repeated failed logins, abnormal location, impossible travel, or suspicious API use | SOC investigation and access review | Information Security / SOC |
| KRI-04 | Prompt-injection or adversarial-input events | Any confirmed event or repeated suspected attempts | Security assessment, containment, and control review | Information Security |
| KRI-05 | AI-related customer complaints | Two or more material complaints in a month | Customer-impact review and output-quality analysis | Business Owner |
| KRI-06 | Human-review noncompliance | Any evidence of unreviewed material output being used operationally or sent externally | Immediate corrective action and retraining | AI Governance Owner |
| KRI-07 | Provider material change | Any change in model, data-use, retention, hosting, subprocessors, or security posture | Third-party reassessment before continued use | Procurement / Third-Party Risk |
| KRI-08 | AI service availability degradation | Availability below contracted target or recurring performance problems | Activate fallback process and vendor escalation | Technical Owner |
| KRI-09 | Open high-risk actions | Any High or Critical risk without an active treatment plan | Escalate to leadership and pause expansion if needed | AI Governance Owner |
| KRI-10 | Unapproved use-case expansion | Any use outside documented purpose, data scope, or authorized user group | Suspend use, assess impact, and require new approval | AI Governance Owner |

## 6. Output Quality Sampling

NOC and Technical Support Operations will review a representative sample of AI-assisted tickets and outputs each month.

The sample must evaluate:

- Accuracy of ticket summary
- Completeness of incident and troubleshooting details
- Accuracy of technical guidance
- Appropriate classification and priority recommendation
- Presence of hallucinations, unsupported claims, or omitted critical information
- Appropriate data handling and absence of prohibited sensitive information
- Evidence of human validation
- Appropriateness of customer-facing language, when applicable

### Sample Quality Rating

| Rating | Description | Required Action |
|---|---|---|
| Acceptable | Output is accurate, complete, appropriate, and properly reviewed | No action required |
| Minor Correction | Output requires small edits but does not create material risk | Track trend and provide user feedback |
| Material Correction | Output contains significant omission, inaccurate information, or unsuitable recommendation | Log issue, investigate cause, and consider control improvements |
| Unsafe Output | Output could cause security, privacy, operational, customer, or legal harm | Stop use, report incident, and initiate response process |

## 7. Monitoring Sources

Monitoring evidence may include:

- AI platform audit logs
- Identity-provider authentication and access logs
- API gateway and integration logs
- SIEM alerts and security-event records
- Ticketing-system records and quality-assurance results
- User feedback, surveys, and reported issues
- Incident reports and post-incident reviews
- Provider security notices, change notifications, SLA reports, and service-status records
- Access-review evidence
- Training-completion records
- Risk-register updates and remediation-tracking records

## 8. Reporting Cadence

| Report | Audience | Frequency | Content |
|---|---|---|---|
| Operational AI Quality Report | NOC and Technical Support leadership | Monthly | Output quality, correction rate, adoption, workflow issues |
| AI Security and Access Report | Information Security / SOC | Monthly | Access events, anomalies, incidents, vulnerabilities, integration status |
| AI Governance Dashboard | AI Governance Owner and Business Owner | Quarterly | KPIs, KRIs, risks, exceptions, control status, supplier changes, remediation |
| Executive AI Risk Summary | Executive Sponsor | Quarterly or upon material issue | Residual risk, material incidents, decisions required, strategic recommendations |
| Third-Party AI Review | Procurement, Security, Privacy, Legal | Annually and upon material change | Provider performance, assurance, contract status, changes, open risks |

## 9. Escalation Criteria

The AI Governance Owner must initiate a formal review when:

- A KRI threshold is exceeded
- A SEV-1 or SEV-2 AI incident occurs
- A recurring SEV-3 event suggests a control weakness
- Output quality drops below the defined KPI target for two consecutive review periods
- A provider changes its data use, model, retention, hosting, security posture, or subprocessors
- A new data category, integration, or user population is introduced
- The use case is proposed for customer-facing automation or higher-impact decisions
- A legal, regulatory, contractual, or customer requirement changes

## 10. Continuous Improvement

Monitoring results must feed into continuous improvement activities, including:

- Updates to the AI system inventory
- Updates to the AI impact assessment
- Updates to the AI risk register
- Changes to prompts, workflows, access permissions, integrations, or knowledge sources
- Additional security testing or privacy review
- User training and awareness activities
- Provider remediation, escalation, or replacement
- Policy and control updates
- Risk acceptance or decision to restrict, suspend, or retire the AI system

## 11. Review Schedule

This monitoring plan must be reviewed quarterly and after any material incident, system change, provider change, or risk assessment update.
