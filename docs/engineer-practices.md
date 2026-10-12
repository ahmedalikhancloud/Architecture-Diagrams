# Practices from experienced cloud engineers

The research used first-person writing from AWS-recognized community engineers and official implementation documentation. It contributes engineering patterns, not borrowed career achievements.

| Source | Practice used in this pack | Limit |
|---|---|---|
| [Aidan Steele: AWS federation comes to GitHub Actions](https://awsteele.com/blog/2021/09/15/aws-federation-comes-to-github-actions.html) | Prefer short-lived federation to static deployment credentials; scope trust and retain audit context. | Use [current GitHub OIDC guidance](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) for audience and subject conditions; early example syntax may differ. |
| [Chris Farris: philosophy of prevention](https://www.chrisfarris.com/post/philosphy-of-prevention/) | Choose useful preventive guardrails and test that they block the risky action without breaking legitimate work. | SCPs are permission ceilings, with exceptions and evaluation limits; they are not user authorization. |
| [HashiCorp: build an AWS landing zone with Terraform](https://developer.hashicorp.com/validated-patterns/terraform/build-aws-lz-with-terraform) | Modular account/workload baselines, reviewed plans, state ownership and policy enforcement. | No HCP Terraform, Sentinel or AFT experience is added without project confirmation. |
| [AWS: Control Tower controls through Terraform](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/deploy-and-manage-aws-control-tower-controls-by-using-terraform.html) | Manage supported controls and customer-owned baselines at the right boundary. | Avoid competing Terraform ownership of Control Tower-managed resources. |

AWS recognition references: [Aidan Steele, AWS Heroes March 2023](https://aws.amazon.com/blogs/aws/meet-the-newest-aws-heroes-march-2023/) and [Chris Farris, first AWS Security Heroes](https://aws.amazon.com/blogs/aws/introducing-the-first-aws-security-heroes/). These references establish relevant public experience, not an objective ranking of the “best” engineers.

## How this changes the resume

The stronger cloud signal is safe adoption of existing infrastructure, clear policy ownership and separation of deployment/runtime permissions. Tools support that story. AI evaluation, traces and controlled tools then show how the same platform discipline extended to AI services.
