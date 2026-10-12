# Design notes and measurement

These diagrams simplify the topology so that ownership and control boundaries are visible. Individual READMEs identify implementation choices to confirm against the actual project.

## Boundaries that matter

| Boundary | Interpretation |
|---|---|
| Organizations / Control Tower | Account governance and supported controls. Terraform also manages customer-owned workload baselines. |
| SCP / IAM | SCPs constrain available permissions; IAM policies grant access within those limits. |
| Deployment / runtime role | A workload does not inherit the pipeline's infrastructure privileges. |
| User / service identity | A service role does not prove a caller is entitled to every document or tool action. |
| Agent / remediation worker | Read-only diagnostics remain separate from explicitly approved writes. |
| EKS / AgentCore / Bedrock | Application hosting, later agent execution and managed model inference are different layers. |
| SQS / DynamoDB / target API | Queue delivery, durable status and idempotent external effects are separate responsibilities. |

Generic resource names do not describe an exact account inventory. No particular identity provider, cache store, policy product or approval interface is inferred. The early Knowledge Bases pilot belongs late in the CEO Foundry engagement; AgentCore belongs to the later Franklin architecture. Proximate's import example uses the historical Terraform CLI, rather than later import-block features.

## Measurement definitions

| Result | Measurement to explain |
|---|---|
| Approximately 30% lower monthly AI platform run cost | Same cost scope before/after, measurement period, traffic and model mix. |
| Approximately 70% faster environment setup | Comparable setup work with explicit start/end; separate from account-vending time. |
| 99.9% service availability | End-to-end success definition and observation window; more than pod health. |
| Groundedness pass rate approximately 70% to 90% | Versioned fixed evaluation set, rubric and retained run evidence. |
| Approximately 45% less diagnostic effort | Incident classification/evidence timing; separate from overall resolution time. |
| Under 20 minutes per content refresh | Manual effort; separate from asynchronous indexing latency. |
| Approximately 40% faster AWS delivery | Comparable environment delivery over the three-account footprint. |
| Approximately 25 hours/month recovered | Task frequency multiplied by measured effort saved; capacity rather than assumed cash savings. |

For cost comparisons, use actual billed usage or approved cost exports:

`reduction_percent = (baseline_cost - comparison_cost) / baseline_cost * 100`

When query volume changes, report both total cost and cost per comparable query. Separate routing/cache changes from price, volume or model-mix changes. An annualized dollar estimate needs a real spend baseline and stated run-rate assumptions.
