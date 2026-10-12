# Architecture Diagrams

Cloud and AI platform architecture notes for Ahmed Ali Khan. These logical reconstructions explain the platform responsibilities, security boundaries and operating decisions behind the work described in my resume. They use generic resource names and simplified topology.

## Choose a story

| Diagram | Experience | Main discussion |
|---|---|---|
| [AWS foundation](01-proximate-aws-foundation/) | Proximate | Organizations, console-to-Terraform adoption and repeatable provisioning. |
| [Landing-zone governance](02-franklin-landing-zone-governance/) | Franklin | Control Tower, organization policies and separate deployment/runtime identities. |
| [Early RAG pilot](03-ceo-foundry-rag-pilot/) | CEO Foundry | Event-driven content refresh and managed retrieval infrastructure. |
| [Secure AI runtime](04-franklin-ai-runtime/) | Franklin | EKS, later AgentCore execution, cost controls and authorization boundaries. |
| [Controlled remediation](05-franklin-controlled-actions/) | Franklin | Read-only diagnostics, bound human approval and safe asynchronous writes. |
| [Release engineering](06-franklin-release-engineering/) | Franklin | Terraform plans, GitOps delivery and AI regression gates. |

Every folder includes a basic README, editable Mermaid source, vector SVG and presentation-ready PNG. The README explains ownership, tradeoffs and failure cases, rather than merely listing services.

## Use in an interview

Open the relevant PNG or SVG. Explain the business problem and your contribution before walking through the arrows. Give one implementation decision, one failure case and how you measured the result. Keep the distinction between what you personally built, what a team owned and what the managed service provided.

The drawings are logical reconstructions, not exports from an employer environment. Implementation choices that need project confirmation are listed in the individual READMEs. [Design notes and measurement](docs/design-notes.md) explain the boundaries and metric definitions.

## Preparation notes

- [Design notes and measurement](docs/design-notes.md)
- [Practices from experienced cloud engineers](docs/engineer-practices.md)
- [Interview prompts](docs/interview-prep.md)

These diagrams cover cloud infrastructure and AI platform operations. They do not claim model training, custom model development or a production Databricks platform from an accreditation alone. No infrastructure is deployed by this repository.
