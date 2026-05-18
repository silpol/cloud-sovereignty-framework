# Actionable Cloud Sovereignty Framework Guide

This document turns the Cloud Sovereignty Framework summary published by ayedo into an implementation-oriented checklist and decision aid that is easy for humans and AI systems to parse and reuse.[page:1]

## Purpose

The referenced page describes the European Commission DG DIGIT Cloud Sovereignty Framework as an operational model for procuring sovereign cloud services using eight sovereignty objectives, five SEAL assurance levels, and a weighted scoring method.[page:1] In practice, this means buyers should not ask only whether a provider is "secure," but whether it can prove European control, legal protection, portability, transparency, and resilience with verifiable evidence.[page:1]

## Core model

The framework evaluates providers across eight objectives: strategic sovereignty, legal and jurisdictional sovereignty, data and AI sovereignty, operational sovereignty, supply-chain sovereignty, technology sovereignty, security and compliance sovereignty, and environmental sustainability.[page:1] It combines minimum thresholds through SEAL levels with a weighted total score so that procurement teams can both exclude unacceptable bids and rank acceptable ones.[page:1]

### Eight objectives in one table

| Objective | What it asks | Actionable interpretation |
|---|---|---|
| SOV-1 Strategic | Is control structurally anchored in the EU? [page:1] | Verify ownership, governance, financing, and continuity under external pressure. [page:1] |
| SOV-2 Legal & Jurisdictional | Is the service shielded from extraterritorial access? [page:1] | Require EU law, EU courts, and no legal, contractual, or technical channels for third-country access. [page:1] |
| SOV-3 Data & AI | Does the customer retain effective technical control of data and AI? [page:1] | Require key sovereignty, full logging, EU-only localization, AI auditability, and deletion proof. [page:1] |
| SOV-4 Operational | Can the service be operated and exited without vendor lock-in? [page:1] | Check exit runbooks, EU support, documentation, source transparency, and subcontractor control. [page:1] |
| SOV-5 Supply Chain | Are hardware and software dependencies traceable and governable? [page:1] | Require SBOMs, origin transparency, update control, minimized non-EU dependencies, and audit rights. [page:1] |
| SOV-6 Technology | Is the stack open, interoperable, and portable? [page:1] | Prefer open standards, open source access, architecture transparency, and low lock-in. [page:1] |
| SOV-7 Security & Compliance | Are security operations and compliance capabilities under EU control? [page:1] | Require EU-based SOC/IR, customer log access, EU incident reporting, certifications, and patch autonomy. [page:1] |
| SOV-8 Sustainability | Is the service operationally sustainable over time? [page:1] | Check PUE, renewable share, circularity, emissions and water transparency, and climate resilience. [page:1] |

## SEAL levels

The page defines five Sovereignty Effective Assurance Levels, from SEAL-0 (no sovereignty) to SEAL-4 (full digital sovereignty), and states that procurers should set minimum levels per objective; bids that fail those minimums are rejected.[page:1] A practical reading is that SEAL is a pass/fail gate per domain, not a single marketing badge for the whole provider.[page:1]

| Level | Meaning | Practical reading |
|---|---|---|
| SEAL-0 | Exclusive non-EU control. [page:1] | Reject for sovereignty-sensitive workloads. |
| SEAL-1 | Formal EU jurisdiction, but substantial non-EU control remains. [page:1] | Suitable only where sovereignty is not a core requirement. |
| SEAL-2 | Enforceable EU law, but material non-EU dependencies remain. [page:1] | Transitional level; acceptable only with explicit risk acceptance. |
| SEAL-3 | Substantial EU control, only marginal non-EU control. [page:1] | Reasonable target for many regulated workloads. |
| SEAL-4 | Complete EU control across technology, operations, governance, and supply chain. [page:1] | Target state for high-sovereignty procurement. |

## Weighted scoring

The framework also calculates a weighted total score by multiplying achieved points divided by maximum points for each objective by a target weighting, then summing across all eight objectives.[page:1] The published weighting is SOV-1 15%, SOV-2 10%, SOV-3 10%, SOV-4 15%, SOV-5 20%, SOV-6 15%, SOV-7 10%, and SOV-8 5%, which gives the strongest emphasis to supply chain, operations, and technology.[page:1]

### Procurement formula

Use the following evaluation formula as written on the page:[page:1]

\[
\text{Total Score} = \sum \left(\frac{\text{Achieved Points}}{\text{Max Points}}\right) \times \text{Weighting}
\]

### Scoring table

| Objective | Weight | Why it matters in practice |
|---|---:|---|
| SOV-1 | 15% [page:1] | Governance and ownership failures can override technical controls. |
| SOV-2 | 10% [page:1] | Jurisdiction determines exposure to foreign legal reach. |
| SOV-3 | 10% [page:1] | Data control is central for confidentiality and AI governance. |
| SOV-4 | 15% [page:1] | Exit capability reduces lock-in and supports resilience. |
| SOV-5 | 20% [page:1] | Supply-chain opacity can negate otherwise strong controls. |
| SOV-6 | 15% [page:1] | Openness and interoperability preserve long-term autonomy. |
| SOV-7 | 10% [page:1] | Security operations matter, but the page notes these are often already comparatively covered. [page:1] |
| SOV-8 | 5% [page:1] | Sustainability is part of resilience, though weighted lowest. |

## Action plan for buyers

The page says procurers should define minimum SEAL levels, require evidence, calculate a weighted score, and use a question catalog for structured evaluation.[page:1] Converted into an execution sequence, that becomes the following operating model.[page:1]

1. Classify workloads by sovereignty sensitivity, for example public website, internal business system, regulated data platform, or critical national capability.
2. Set minimum SEAL per objective before going to market, because changing thresholds after bids arrive weakens defensibility and fairness.[page:1]
3. Publish mandatory evidence requirements with the tender, including contracts, court venue, key-management architecture, data-flow diagrams, SBOMs, audit reports, and proof of EU locations and teams.[page:1]
4. Score only bids that pass all minimum SEAL thresholds, then rank surviving bids with the weighted score.[page:1]
5. Run a claims-versus-evidence review specifically to detect sovereign-washing, because the page warns that labels without real technical and organizational decoupling likely do not reach SEAL-4.[page:1]
6. Add contract clauses for drift control, requiring notification and approval for ownership changes, subcontractor changes, support-location changes, and architecture changes affecting data locality or key control.

## Action plan for providers

The page states that the framework shifts attention away from certification alone and toward demonstrable independence, control, and exit capability.[page:1] Providers therefore need to build both technical controls and evidence pipelines, not just compliance messaging.[page:1]

### Minimum provider backlog

- Map every service component to one of the eight objectives and identify the evidence that proves compliance for that component.[page:1]
- Build customer key sovereignty with BYOK or BYOHSM, no provider escrow, and verifiable deletion mechanisms if aiming for top-tier data sovereignty.[page:1]
- Create standardized exit runbooks that cover container images, Helm charts, infrastructure-as-code, secrets handling, configuration, databases, and object storage export.[page:1]
- Produce complete architecture diagrams, dependency maps, runbooks, disaster-recovery documentation, and source or source-equivalent transparency where promised.[page:1]
- Maintain complete signed SBOMs, update provenance, sub-supplier registers, and audit-rights clauses across the chain.[page:1]
- Prove strict EU localization for runtime data, backups, logs, and metrics, and remove non-EU administrative access paths if claiming strong sovereignty.[page:1]
- Staff SOC, NOC, incident response, and support from EU locations and expose logs, metrics, and alerts directly to customers where possible.[page:1]

## Machine-readable checklist

The following YAML is optimized for AI/LLM ingestion and can be reused in procurement workflows, internal audits, or vendor questionnaires.

```yaml
cloud_sovereignty_framework:
  source: "ayedo summary of EU Commission DG DIGIT Cloud Sovereignty Framework"
  source_url: "https://ayedo.de/en/cloud-sovereignty-framework/"
  version_note: "Page states framework version 1.2.1, October 2025"
  objectives:
    - id: SOV-1
      name: Strategic Sovereignty
      checks:
        - EU headquarters and decision-making bodies
        - Protection against non-EU change of control
        - EU-based financing and value creation
        - Continuity under external pressure
      evidence:
        - ownership chart
        - shareholder register
        - board composition
        - financing disclosures
        - continuity plans
    - id: SOV-2
      name: Legal and Jurisdictional Sovereignty
      checks:
        - EU law governs contracts
        - EU court venue
        - no extraterritorial access channels
        - export-control compliance
        - IP under EU jurisdiction
      evidence:
        - master service agreement
        - DPA
        - legal opinions
        - access-control architecture
    - id: SOV-3
      name: Data and AI Sovereignty
      checks:
        - customer key sovereignty
        - complete access logs
        - EU-only data localization
        - AI transparency and auditability
        - verifiable deletion proof
      evidence:
        - KMS and HSM architecture
        - sample audit logs
        - residency controls
        - AI system documentation
        - deletion proof design
    - id: SOV-4
      name: Operational Sovereignty
      checks:
        - exit and migration capability
        - EU-based support and operations
        - complete technical documentation
        - source transparency
        - auditable subcontractors
      evidence:
        - exit runbooks
        - export procedures
        - support operating model
        - architecture docs
        - subcontractor register
    - id: SOV-5
      name: Supply Chain Sovereignty
      checks:
        - hardware origin transparency
        - signed complete SBOM
        - EU control of updates
        - minimized non-EU dependencies
        - contractual audit rights
      evidence:
        - supplier inventory
        - SBOM exports
        - update pipeline records
        - dependency matrix
        - audit clauses
    - id: SOV-6
      name: Technology Sovereignty
      checks:
        - open standards and non-proprietary APIs
        - open source access rights
        - architecture transparency
        - portability and low lock-in
        - EU control of critical compute where relevant
      evidence:
        - API documentation
        - OSS licenses
        - architecture diagrams
        - portability test results
    - id: SOV-7
      name: Security and Compliance Sovereignty
      checks:
        - EU certifications and standards mapping
        - GDPR NIS2 DORA alignment
        - EU-based SOC and IR teams
        - direct log access for customers
        - EU-compliant incident reporting
        - patch autonomy
      evidence:
        - certificates
        - control matrix
        - SOC roster and locations
        - logging interface samples
        - incident procedures
    - id: SOV-8
      name: Environmental Sustainability
      checks:
        - PUE and efficiency metrics
        - renewable energy share
        - recycling and reuse practices
        - CO2 water and energy transparency
        - climate resilience planning
      evidence:
        - sustainability reports
        - utility metrics
        - renewable certificates
        - resilience scenarios
  seal_levels:
    - level: 0
      name: No Sovereignty
    - level: 1
      name: Jurisdictional Sovereignty
    - level: 2
      name: Data Sovereignty
    - level: 3
      name: Digital Resilience
    - level: 4
      name: Full Digital Sovereignty
  scoring_weights:
    SOV-1: 0.15
    SOV-2: 0.10
    SOV-3: 0.10
    SOV-4: 0.15
    SOV-5: 0.20
    SOV-6: 0.15
    SOV-7: 0.10
    SOV-8: 0.05
  procurement_workflow:
    - define minimum seal per objective
    - request verifiable evidence
    - reject bids failing minimum seal
    - score remaining bids with weighted formula
    - validate evidence against marketing claims
    - monitor contract and architecture drift over time
```

## Suggested tender questions

The page mentions a question catalog with examples such as where decision-making bodies are located, what key management is used for customer data, and whether there are non-EU sub-suppliers.[page:1] The following expanded list is suited for RFI, RFP, or due-diligence interviews.[page:1]

- Who ultimately controls the provider, and what protections exist against non-EU change of control?
- Which law governs the contract, and which courts have exclusive venue?
- Can any non-EU entity compel access through ownership, support channels, subcontracting, or technical administration?
- Who controls encryption keys, and can the provider recover or escrow them?
- Can the provider prove that runtime data, backups, logs, and metrics stay in the EU at all times?
- What is the tested time to migrate workloads to another Kubernetes-compatible environment?
- Which APIs, data formats, and orchestration interfaces are proprietary?
- Can the provider deliver a complete, signed SBOM for the full service stack?
- Where are SOC, NOC, and incident response teams located, and is there any offshore escalation path?
- Which sustainability metrics are published, and how often are they independently verified?

## Red flags

The page explicitly warns against sovereign-washing and says providers with non-EU control may achieve at most SEAL-2 despite marketing claims.[page:1] In evaluations, the following patterns should trigger escalation or rejection.[page:1]

- EU branding, but non-EU parent control or decisive investor rights.
- EU contract paper, but non-EU support, admin, or incident-response paths.
- Claims of data residency, but logs, backups, telemetry, or support tooling leave the EU.
- BYOK claims, but provider escrow, recovery backdoors, or opaque HSM operations remain.
- Open standards claims, but migration depends on undocumented proprietary APIs or hidden managed services.
- Security certifications presented as proof of sovereignty, even though the framework distinguishes sovereignty from classic security assurance.[page:1]

## Recommended implementation pattern

For organizations pursuing European digital sovereignty, the page strongly favors open standards, open source accessibility, standardized APIs, source transparency, traceable supply chains, EU-based operations, and strong exit capability.[page:1] A practical target architecture is therefore Kubernetes-native, infrastructure-as-code managed, fully documented, cryptographically customer-controlled, and continuously evidenced through auditable artifacts rather than policy statements alone.[page:1]
