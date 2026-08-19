# AI Governance Control Mapping

## 1. Purpose

This document maps NovaConnect AI governance controls to the NIST AI Risk Management Framework, NIST Cybersecurity Framework 2.0, ISO/IEC 42001 principles, and selected regulatory expectations.

This mapping is a portfolio implementation example. It is not a certification, legal opinion, or statement of compliance.

## 2. Control Mapping

| Control ID | Control Requirement | Evidence | NIST AI RMF | NIST CSF 2.0 | ISO/IEC 42001 Alignment | Regulatory Relevance |
|---|---|---|---|---|---|---|
| AIG-01 | Maintain an AI governance policy defining scope, principles, roles, approval requirements, prohibited uses, and review cycles | Approved AI Governance Policy | Govern | GV.PO, GV.RR, GV.OV | AI policy, leadership, roles and responsibilities | AI governance accountability |
| AIG-02 | Assign a business owner, technical owner, and AI governance owner for every AI system | AI system inventory and approval record | Govern | GV.RR | Roles, accountability, organizational responsibilities | Accountability and oversight |
| AIG-03 | Maintain a complete inventory of AI systems, providers, users, data categories, integrations, and risk classifications | AI System Inventory | Govern, Map | ID.AM, GV.OC | AI system lifecycle and documented information | Transparency and AI system documentation |
| AIG-04 | Require risk classification and AI impact assessment before deployment or material modification | AI impact assessment and approval decision | Map, Measure, Manage | ID.RA, GV.RM | AI risk assessment and treatment | Impact assessment and risk management |
| AIG-05 | Apply human oversight to AI outputs that may affect customers, operations, security, or business continuity | Workflow design, training records, review logs | Govern, Map, Manage | GV.PO, PR.AT, RS.MA | Human oversight and operational controls | Human review and accountability |
| AIG-06 | Prohibit entry of credentials, secrets, payment data, and unapproved sensitive information into AI tools | AI governance policy, training, DLP configuration where available | Govern, Map | PR.DS, PR.AT | Data governance and data protection | Privacy and confidentiality |
| AIG-07 | Enforce IAM controls, MFA, RBAC, least privilege, access reviews, and secure API key management | IAM configuration, access review records, integration documentation | Govern, Manage | PR.AA, PR.PS | Access control and operational security | Security safeguards |
| AIG-08 | Protect AI-related data through encryption, data minimization, retention controls, and approved data flows | Data-flow documentation, provider configuration, privacy review | Map, Measure | PR.DS, ID.AM | Data management and privacy controls | Data protection principles |
| AIG-09 | Test for accuracy, reliability, hallucinations, prompt injection, privacy exposure, and security weaknesses before deployment | Test plan, results, remediation log | Measure | ID.RA, PR.PS, DE.AE | Performance evaluation and AI system validation | Reasonable care and risk mitigation |
| AIG-10 | Monitor AI performance, drift, anomalies, access activity, integration events, and harmful outputs | Monitoring dashboards, SIEM logs, KPI/KRI reports | Measure, Manage | DE.CM, DE.AE, GV.OV | Monitoring, measurement, continual improvement | Ongoing review |
| AIG-11 | Conduct third-party due diligence before onboarding an AI provider and monitor the relationship throughout its lifecycle | Supplier assessment, contract review, risk record | Govern, Map, Manage | GV.SC, ID.RA | Supplier and third-party management | Vendor due diligence and provider accountability |
| AIG-12 | Include security, privacy, data-use, retention, incident notification, audit, subcontractor, and exit requirements in AI contracts | Signed contract, data processing agreement, SLA | Govern, Manage | GV.SC | Third-party contractual controls | Contractual and regulatory obligations |
| AIG-13 | Maintain an AI incident-response process for data exposure, prompt injection, unsafe outputs, model drift, misuse, and vendor incidents | AI incident response plan, incident reports, exercises | Manage | RS.MA, RS.AN, RS.CO, RS.MI | Incident management and corrective actions | Incident handling and notification |
| AIG-14 | Maintain fallback procedures so operations can continue if an AI service is unavailable, unreliable, or disabled | Business continuity procedure, test records | Manage | PR.IR, RC.RP, RC.CO | Operational continuity and improvement | Operational resilience |
| AIG-15 | Train users on secure AI use, data handling, output validation, prompt injection, prohibited uses, and incident reporting | Training materials, attendance records, acknowledgments | Govern | PR.AT | Competence and awareness | Awareness and responsible use |
| AIG-16 | Reassess AI systems after material changes, incidents, major complaints, provider changes, or new legal requirements | Updated assessment, change record, review log | Govern, Map, Measure, Manage | ID.IM, GV.OV, ID.RA | Continual improvement and change management | Ongoing compliance |

## 3. Implementation Status

| Control Status | Definition |
|---|---|
| Not Started | Control has not been designed or assigned |
| Planned | Control is defined but not yet implemented |
| In Progress | Implementation activities are underway |
| Implemented | Control is operating and evidence is available |
| Needs Improvement | Control exists but has a known gap or weakness |
| Not Applicable | Control does not apply to the approved use case |

## 4. NovaAssist Baseline Status

| Control ID | Status | Priority | Target Evidence |
|---|---|---|---|
| AIG-01 | Implemented | High | `02-ai-governance-policy.md` |
| AIG-02 | Implemented | High | `03-ai-system-inventory.md` |
| AIG-03 | Implemented | High | `03-ai-system-inventory.md` |
| AIG-04 | Implemented | High | `04-ai-impact-assessment.md` |
| AIG-05 | Implemented | High | Policy and documented review workflow |
| AIG-06 | Implemented | High | Policy and user-training record |
| AIG-07 | Planned | High | IAM and integration security review |
| AIG-08 | Planned | High | Data-flow and privacy-review record |
| AIG-09 | Planned | High | Pre-deployment testing report |
| AIG-10 | Planned | Medium | Monitoring and KPI/KRI report |
| AIG-11 | In Progress | High | `07-third-party-risk-assessment.md` |
| AIG-12 | Planned | High | Supplier contract and DPA checklist |
| AIG-13 | Implemented | High | `08-ai-incident-response-plan.md` |
| AIG-14 | Planned | Medium | AI outage fallback procedure |
| AIG-15 | Planned | High | Training completion evidence |
| AIG-16 | Planned | Medium | Quarterly AI governance review record |

## 5. Notes

Control mappings are not one-to-one compliance determinations. They are designed to show how NovaConnect can operationalize AI governance requirements across cybersecurity, privacy, operational risk, third-party risk, and incident management.
