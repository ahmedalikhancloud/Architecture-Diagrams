# Interview preparation

Use the diagrams to explain your real contribution. Fill in actual dates, examples and evidence before rehearsing. A memorized service list is less convincing than explaining a decision and its consequences.

## A useful 90-second structure

1. Business problem and delivery constraint.
2. Your ownership and the team's other responsibilities.
3. One design decision and why it fit the constraint.
4. One failure or risk and the control you used.
5. Measured result, measurement period and limitation.

## Questions by story

| Story | Questions to rehearse |
|---|---|
| Proximate foundation | What did an import plan reveal? How did you prevent replacement? Who could change state? What counted as environment delivery? |
| Franklin landing zone | Which policy did you enforce? Why SCP versus IAM? What was your canary/exception process? What did Control Tower own? |
| CEO Foundry pilot | What happened on duplicate S3 events? How were failed refreshes visible? How did you distinguish manual effort from indexing latency? |
| Franklin runtime | What did the 99.9% measure? Which cache requests were unsafe? How did tools check user entitlement? What changed when AgentCore arrived? |
| Controlled remediation | What exactly did the human approve? What happens after a worker crashes following a write? How can a duplicate message be processed safely? |
| Release engineering | What blocked a release? What did a groundedness pass mean? How did you bind approval to the plan/artifact? How did infrastructure recovery differ from app rollback? |

## Bring evidence when possible

Use sanitized architecture notes, a sample before/after timing, a cost calculation, an evaluation rubric or a redacted finding record that you are entitled to share. Avoid client secrets or internal screenshots. If a detail is uncertain, explain the design at the level you remember rather than inventing a precise implementation.

## Hypothetical retail preparation

If practicing an unnamed home-retail scenario, label it hypothetical. A useful exercise is a support assistant that reads approved product/policy documents, with a separately approved order-change action. Discuss authorization, content freshness, access-safe caching and approval binding. Do not present this practice scenario as a real retailer engagement or insert invented revenue/savings into the employment record.
