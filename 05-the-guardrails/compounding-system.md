# Compounding System Design

## Feedback Loops

 

| Loop | Input | Output | Compounds? | Status |
|------|-------|-----------|----------|--------|
| Recursive Learning | Examiner decisions corrections overrides claim outcomes | Improved recommendations and handling of similar future claims | Y | missing |
| Cross-Domain Transfer | Claims learnings + Contract, Product, Customer, Beneficiary & Distributor context | Reusable intelligence and richer decision context across claims/workflows | Y | missing |
| Network Intelligence | Interactions across claims, users, workflows & connected enterprise data | Patterns, exceptions and insights that become stronger as participation grows | Y | missing |

 

**Broken loop identified by partner:** Cross-Domain Transfer Loop

**Fix plan:** Create a governed cross-domain knowledge layer with common CDE definitions, authoritative sources, lineage, reusable business rules, and feedback mechanisms so insights learned in Claims can flow back to contributing domains and be reused across future AI use cases

 

## Context Connectivity

<!-- How does knowledge flow across teams and domains? Where does it silo? -->

 

**How knowledge flows:** Knowledge currently flows through CDE mapping, domain-owner working sessions, data-product design, certification activities, and shared documentation. Claims consumes context from Contract, Product, Customer, Beneficiary, and Distributor to support end-to-end claim decisions

 

**Where it silos:** Knowledge silos at domain boundaries where ownership, business rules, metadata, lineage, and certification are managed independently. Insights generated during Claims processing are not yet systematically fed back into the other domains or made reusable across AI use cases

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Governance Policy

| Scope | 
|------|
| **Scope:** AI agents used to support annuity claim intake, document review, data validation, beneficiary and contract verification, business-rule evaluation, claim routing, recommendation generation, and preparation of claim servicing actions. Excludes: Final claim approval or denial, changes to contractual rights, beneficiary determinations, financial disbursement, fraud determinations, and customer communications that create a binding commitment without required human authorization.|

 
| Autonomy boundaries | 
| **Autonomy boundaries:** Routine data/document validation and information retrieval, auto. Claim eligibility or disposition recommendation, human approval required. Final denial, beneficiary change/dispute resolution, or financial disbursement, never auto.|

 
|Escalation Triggers | 
|**Escalation triggers:** 1.AI confidence falls below the approved production threshold. 2.Required claim, contract, beneficiary, or customer data is missing or conflicting across authoritative sources. 3.Business rules return conflicting or multiple possible outcomes. 4.Beneficiary information conflicts with contract or claim information. 5.Claim falls outside documented business rules or represents a previously unseen exception. 6.Customer communication contains fraud, legal, complaint, dispute, vulnerability, or distressed-language indicators. 7.AI recommendation conflicts with deterministic rules or authoritative source data. 8.Any action would deny a claim, change beneficiary rights, or initiate/release a financial payment.|

 
| Audit Cadence |
|**Audit cadence:** Real-time, Confidence threshold, rule conflicts, missing data, prohibited actions, access/security violations (Claims AI Platform/Product Owner). Weekly, Human overrides, AI errors, exception patterns, escalation rate and recommendation accuracy (Claims Business/Product Owner). Quarterly, Model performance, drift, governance, security, privacy, bias/fairness and regulatory controls (AI Governance / Model Risk Owner).|

 
| Regulatory Exposure | 
|**Regulatory exposure (EU AI Act / other):** Insurance regulatory requirements; enterprise data/privacy and AI governance; applicable U.S. state privacy/insurance requirements; GDPR where EU personal data is in scope; EU AI Act where the system/use falls within its territorial and use-case scope.. Risk tier: limited. Controls: Human-in-the-loop approval for consequential decisions; role-based access controls; approved authoritative data sources; data lineage; decision and prompt logging; explainability; confidence thresholds; automated escalation; model and data-quality monitoring; audit trails; version-controlled business rules; privacy controls; and periodic model-risk/governance review..|

 

## Agent Topology

 

Intake Agent

 

Can: classify incoming claim documents, extract information and identify missing documentation.

Can't: determine final claim eligibility.

Approval owner: Claims Examiner.

 

Data Validation Agent

 

Can: retrieve and validate Claims, Contract, Customer, Product, Beneficiary and Distributor data against approved authoritative sources.

Can't: change authoritative source data or resolve material conflicts independently.

Approval owner: Claims Examiner / appropriate Domain Owner.

 

Claims Decision Support Agent

 

Can: apply approved rules, identify exceptions and recommend claim disposition or next-best action.

Can't: independently approve or deny claims.

Approval owner: Authorized Claims Examiner.

 

Payment/Servicing Agent

 

Can: prepare approved servicing or payment actions for execution.

Can't: independently release funds or modify beneficiary/contract rights.

Approval owner: Authorized Claims Operations role.

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| Public generative AI tools (e.g., ChatGPT) used to summarize claim documents, interpret contract provisions, or draft claim recommendations | Claims Examiners | H | govern |
| Unapproved AI-powered PDF/OCR tools used to extract information from death certificates, beneficiary forms, and supporting claim documents | Claims Operations | H | govern |
| Personal AI assistants or browser extensions used to draft customer communications, summarize claim notes, or analyze claimant information | Claims / Customer Service | H | kill |

**Total tools found:** 3 potential tools/use cases identified for validation through employee surveys, interviews, and access-log reviews.
**Tools after triage:** 0 approved as-is; 2 candidates for governed use following security, privacy, and compliance review; 1 prohibited use case involving unapproved processing of sensitive customer information.
**Estimated hidden spend:**Unknown; requires review of employee subscriptions, expense reports, corporate card transactions, and reimbursed software expenses.





