# Fictional finding: export lookup may cross workspace boundaries

This entire example is invented for teaching. It is not a finding in Ekyon's software or a client system. No repository was inspected and no runtime request was made for this example. Names, paths and revision labels below are fictional. The scenario illustrates the difference between source evidence and confirmed exposure.

## Record

| Field | Fictional record |
| --- | --- |
| Finding ID | EX-001 |
| Product | Sample workspace reporting application. |
| Agreed scope | Selected export route and its immediate permission checks. |
| Revision | `fictional-snapshot-01`, an illustrative label, not a real commit. |
| Source location | `example/export-route.ts`, function `getWorkspaceExport`. This file does not exist in this kit. |
| Environment / evidence level | Source review only within the invented scenario. |
| Status | Investigating. |
| Decision owner | Product engineering owner, a fictional role. |

## Observation and evidence

**Expected behaviour:** A signed-in member may request only exports for a workspace they are permitted to access.

**Illustrative source observation:** The fictional route checks whether the requester is signed in and then looks up an export using a supplied workspace identifier. No membership decision is visible in the route or its immediate helper. The wider middleware chain, data-access policies and export storage controls are outside this fictional review scope.

**Evidence limit:** This description stands in for an observation in a real report. It supplies no actual code or runtime proof. A real finding would reference the inspected revision, relevant code and any separately authorised test evidence. A missing visible check does not establish that every layer lacks a control.

## Impact, confidence and priority

**Potential consequence:** If no other control blocks the request, a signed-in user could receive records from a workspace they do not belong to. Data returned and reachable accounts would determine the impact. No disclosure or incident is claimed.

**Confidence:** Within the invented scenario, confidence is high that the selected route lacks a visible membership decision. Confidence in actual exposure is unresolved because other controls and runtime behaviour have not been checked.

**Severity:** Provisional. Potential cross-workspace disclosure deserves prompt investigation, but final severity requires evidence about effective controls, reachable records and realistic access conditions. No numeric score is assigned without that evidence.

**Next priority:** Before relying on the export path for a release decision, inspect the request's permission boundary and arrange a bounded test if authorised. This is a proposed decision sequence, not an assertion that an actual release is unsafe.

## Proposed work

1. Inspect the middleware and data-access policy used by the route. Establish where workspace membership is enforced and whether that enforcement covers both export creation and retrieval.
2. If the boundary is missing, enforce the intended workspace permission before returning the export. Check related export paths for the same assumption.
3. Agree a test environment with two synthetic workspaces and permitted test accounts. Do not use real customer records or infer runtime authorisation from repository access.
4. Assign the repair and verification owner. Estimate work after the missing controls and affected paths are understood. No repair duration is asserted here.

## Proposed verification

All checks below are **not run**. Expected results describe the fictional application's intended requirements.

| Check | Setup | Expected result |
| --- | --- | --- |
| Permitted export | A test member requests an export for their own synthetic workspace. | Only that workspace's permitted export is returned. |
| Other workspace | The same test member requests the other synthetic workspace's export. | Access is denied and no export content or download location is returned. |
| Signed-out request | No signed-in session requests the synthetic export. | The request is denied without export content. |
| Removed membership | A synthetic member loses workspace access before requesting an existing export. | The retrieval checks current permission and denies access. |
| Related retrieval path | An authorised test checks any separate export-download route within the agreed scope. | The same workspace boundary holds, including for existing export records. |

A real verification record would include the reviewed and fixed revisions, environment, test time, redacted evidence and observed results. It would also explain any path that could not be checked.

## Closure

This fictional finding remains **investigating**. It cannot be called verified fixed. If a real investigation confirmed exposure, assessing affected data and the appropriate response would need its own scope; changing the route alone would not establish what happened before the change.
