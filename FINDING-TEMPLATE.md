# Finding template

Copy this document once per finding. Use “not reviewed” or “unknown” when evidence is unavailable. Do not leave a blank field that could be mistaken for a completed check.

## Record

| Field | Complete this |
| --- | --- |
| Finding ID and title | A stable ID and a specific observed concern. |
| Report date / reviewer | Who prepared it and when. |
| Product / review scope | Product, repository and agreed workflow. |
| Reviewed revision | Exact commit, build or dated snapshot. |
| Environment | Source only, named test environment or other explicitly authorised environment. |
| Evidence level | Source observation, reproduced behaviour or unverified tool signal. |
| Status | Open, investigating, repair proposed, awaiting verification, verified fixed or accepted risk. |
| Decision owner | Person accountable for the next decision. |

## Observation and evidence

**Expected behaviour:** What rule or agreed requirement should hold?

**Observed behaviour:** What did the reviewer actually inspect or observe?

**Evidence references:** Identify file/function and revision, or an authorised test record and environment. Keep confidential evidence in an access-controlled location. Include only the minimum redacted excerpt needed for the report.

**Test boundary:** State what was and was not executed. For runtime evidence, record authorisation, permitted identities, synthetic records, steps, expected result, actual result and test time. Do not put tokens, passwords or real customer records in the finding.

## Impact, confidence and priority

**Affected workflow / users / data:** Name the reachable scope supported by evidence. Mark potential reach as conditional.

**Business consequence:** Explain why the owner should care. Separate a possible consequence from an observed outcome.

**Confidence:** State confidence in the observation and confidence in runtime exposure separately, with reasons.

**Severity:** Apply the engagement's agreed scale and explain impact and likelihood. If reach is unresolved, label the assessment provisional and name the evidence needed to finalise it.

**Action priority:** Explain what should happen next and when. Investigation can be urgent even while severity remains provisional.

**Limits and alternatives:** What controls, configurations or unreviewed paths could change the conclusion?

## Proposed work

**Next step:** Repair, investigate, monitor or accept with a recorded reason.

**Recommended change:** Describe the intended behaviour and relevant related paths to inspect. Avoid prescribing a rewrite without evidence.

**Owner and dependencies:** Include access, design decisions, related teams and release constraints.

**Effort:** Give an estimate only when supported. Include investigation, implementation, tests, release and follow-up assumptions. Otherwise say “not estimated” and name what is needed first.

## Verification and closure

| Check | Expected result | Environment / evidence | Result |
| --- | --- | --- | --- |
| Intended permitted behaviour | Define the successful user journey. | To complete. | Not run. |
| Prohibited or invalid behaviour | Define the denied request or rejected state. | To complete. | Not run. |
| Relevant failure / retry / regression | Define the boundary case for this finding. | To complete. | Not run. |

**Verified revision / date / reviewer:** Complete after verification.

**Remaining risk and coverage gaps:** Include related work that remains open. A passing check covers the tested path and revision only.

**Closure decision:** Record the evidence and accountable owner. Keep “verified fixed” separate from “accepted risk”; attach a reason and revisit date for accepted risk. If evidence indicates actual exposure, arrange an appropriate separate investigation rather than treating a code change as a complete response.
