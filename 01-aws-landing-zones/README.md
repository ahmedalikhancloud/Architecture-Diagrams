# AWS landing zones with reviewed infrastructure changes

An account layout and delivery path for governing AWS infrastructure through code. The same controls apply across the workload accounts, while each environment has its own state and deployment permissions.

![AWS landing zone architecture](diagram.svg)

## Walkthrough

1. Existing resources are imported into Terraform before their configuration is changed. A pull request exposes the proposed change and its plan.
2. GitHub Actions runs TFLint and Checkov. An approved workflow exchanges its OIDC token for the IAM role allowed to change the target environment. The production path is shown in the diagram.
3. Organizations and Control Tower provide the account foundation. SCPs limit which actions are possible. IAM policies and Identity Center permission sets supply the actual permissions.
4. CloudTrail, AWS Config and Wiz provide evidence for access investigations and remediation. Scheduled plans help identify changes made outside Terraform.

## Design decision

Separate account state and deployment roles keep a development change from inheriting production access. Code checks catch problems early, but AWS policies remain the enforcement boundary at runtime.

Platform scope: account design, Terraform adoption, deployment access and policy remediation. Client identifiers and policy documents are omitted.
