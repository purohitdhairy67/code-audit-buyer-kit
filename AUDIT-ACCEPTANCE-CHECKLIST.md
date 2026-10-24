# Buyer acceptance checklist

Use this before commissioning a review and again when accepting its report. The checklist evaluates the agreed deliverable. It does not establish launch readiness or software security on its own.

## 1. Agree the brief

| Field | Your agreement |
| --- | --- |
| Decision to support | Launch, handover, targeted repair, rebuild decision or another named decision. |
| Product and stack | Main applications, frameworks and external dependencies. |
| Repositories / revision | Included repositories and the snapshot to review. |
| Priority workflows | Named journeys, account roles and important failure cases. |
| Review depth and time | Source review, sampling approach and time budget. |
| Environments | Source only or specifically authorised runtime environments. |
| Exclusions | Unreviewed repositories, flows, infrastructure and activities. |
| Deliverables / timing | Owner summary, finding register, coverage record, repair order and walkthrough. |
| Contacts | Business decision owner and technical contact. |

- [ ] The reviewer has explained what can reasonably be checked within the agreed time.
- [ ] Confidentiality and evidence handling are agreed before access is granted.
- [ ] Repository access uses the permissions needed for the review. Runtime checks, production access, infrastructure changes and load tests are separately specified where needed.
- [ ] Repairs and follow-up verification are explicitly included or excluded, with separate responsibilities and commercial terms where applicable.
- [ ] Penetration testing, investor due diligence and certification are named separately if required. They are not inferred from “code audit”.

## 2. Agree the coverage record

For each area below, record **included**, **sampled** or **excluded**, plus the evidence method and any limitation. Do not mark an area complete simply because a tool ran.

| Area | What the coverage record should identify |
| --- | --- |
| Access boundaries | Selected roles, server-side permission checks and account/workspace boundaries. |
| Sensitive data | Selected data paths, credential types, permissions and storage or logging concerns. |
| Critical flows | Journeys checked, failures and retries considered, and any runtime authorisation. |
| Architecture | Areas reviewed for change difficulty, coupling and missing ownership or documentation. |
| Dependencies | Manifests/versions inspected and whether a warning affects a reachable application path. |
| Performance | Source-based hypotheses versus behaviour confirmed under stated test conditions. |
| Tests | Important successful, failure and denied-access cases actually inspected or executed. |
| Deployment / recovery | Configuration, logging, backups and rollback evidence available to the reviewer. |

## 3. Assess the report

- [ ] An owner summary connects the main findings to the decision in the brief.
- [ ] Every finding names the reviewed revision and the evidence level.
- [ ] Findings distinguish observed facts, conditional consequences and unknowns.
- [ ] Tool warnings have been interpreted, or are clearly labelled unverified leads.
- [ ] Severity has a reason. Uncertain exposure is recorded rather than silently assumed.
- [ ] Priority explains the next action, including investigation where repair scope is unclear.
- [ ] The report names unavailable access, unreviewed paths and sampling limits.
- [ ] Recommendations support a practical choice between targeted work and deeper changes.
- [ ] Effort estimates include assumptions and dependencies, or say why work is not yet estimated.
- [ ] Findings can be handed to your own engineers without depending on a further purchase.

## 4. Accept the handover

- [ ] The reviewer has walked through the evidence, findings and limits with the responsible people.
- [ ] Each finding has a next action and owner: investigate, repair, schedule or accept with a reason.
- [ ] The repair order identifies dependencies and decision deadlines.
- [ ] Any repair scope states who implements, releases and verifies the work.
- [ ] Verification checks cover the intended behaviour and relevant denied, failure or retry cases.
- [ ] Evidence is handed over through the agreed access-controlled channel.
- [ ] Temporary access removal and evidence retention or deletion are assigned and dated.
- [ ] Unresolved questions have a named owner and next review date.

## Acceptance record

| Item | Record |
| --- | --- |
| Report version / reviewed revision | To complete. |
| Decision | Accepted, accepted with named open items, or clarification required. |
| Open items and due dates | Link each item to an owner and the agreed scope. |
| Accepted by / date | Business owner and technical reviewer, as applicable. |
| Next review | Date or trigger, such as a material code change. |

Accepting a report acknowledges the agreed assessment and its limits. It does not automatically accept every software risk, approve a release or verify repairs that have not been checked.
