# IU Anaplan Budgeting — Implementation Backlog and Deferral Register

Version: 1.0 | Prepared: 2026-10-19
Document status: Proposed governance template; not yet approved by IU or Deloitte.
Register owner: [IU owner] | Vendor counterpart: [Deloitte lead]
Authoritative location: [Teams/SharePoint link] | Review cadence: [weekly proposed]

## Purpose
Preserve requirements, defects, unanswered decisions, and proposed deferrals throughout the IU budgeting implementation. Reconstruct items scattered across user stories, shared files, emails, and meetings without treating an undocumented discussion as an approved scope change.

This template contains no verified project items. Bracketed values are placeholders. Nothing here determines contractual scope, liability, payment obligations, or acceptance rights; those require the governing project agreements and authorized decisions.

## Core governance rule — proposed for IU approval
An item originally required for the agreed implementation remains traceable to that baseline until an authorized IU decision changes its disposition. A vendor recommendation to defer is recorded as a recommendation, not as IU approval. Silence, meeting attendance, or a label such as “future feature” is not treated by this register as evidence of approval.

PMI guidance emphasizes documenting, evaluating, approving, and communicating changes, and tracing requirements to business needs and delivery evidence. [S1][S2]

## Relationship to the future-feature document
This register owns every item's canonical record and permanent ID, including future candidates. The companion future-feature document is an index and planning view; it references these IDs rather than maintaining a second independent status record.

Use IDs IU-ANAPLAN-0001, IU-ANAPLAN-0002, and so on. Never change an ID when an item is deferred, promoted, split, or closed. Record parent/child or duplicate relationships explicitly.

## Keep these fields separate
| Dimension | Allowed values / guidance |
|---|---|
| Item type | Requirement gap; defect; clarification/decision; enhancement; dependency |
| Baseline scope | Confirmed baseline; confirmed new request; disputed; not yet verified |
| Decision state | Pending review; delivery confirmed; deferral proposed; deferral approved; scope dispute; rejected; withdrawn |
| Delivery state | Not scheduled; planned; in progress; blocked; ready for IU validation; closed |
| Release treatment | Go-live required; later implementation release; post-go-live candidate; undecided |
| Business priority | Critical; high; medium; low — record rationale and IU owner |
| Closure outcome | Delivered and IU accepted; duplicate; rejected; withdrawn — include evidence |

A deferral is not delivery completion. A future candidate is not a delivery commitment. Unknown scope must remain unknown or disputed until evidence and an authorized decision resolve it.

## Master index
No populated items yet. Add one row per canonical item.

| ID | Title | Type | Baseline scope | Decision state | Delivery state | Release treatment | IU owner | Deloitte owner | Next action / owner | Review due |
|---|---|---|---|---|---|---|---|---|---|---|

For a large register, use the same schema in a shared list or workbook and preserve these rules. Do not operate two competing authoritative registers.

## Canonical item template
Copy this section for each item. Link the master-index row to its heading.

### IU-ANAPLAN-[NNNN] — [Concise title]

#### Identification and ownership
- Date captured: [date]
- Captured by: [name]
- Item type: [value]
- Business process / affected unit: [value]
- IU business owner: [name]
- Deloitte delivery owner: [name]
- Related user-story / requirement IDs: [IDs and links]
- Related defect, risk, decision, change-request IDs: [IDs and links]
- Parent / child / duplicate relationships: [IDs or none]

#### Requirement and baseline evidence
- Business need: [what the user must accomplish and why]
- Required behavior / original acceptance criteria: [specific, testable description]
- Current implemented behavior: [observed behavior; distinguish evidence from assumption]
- Gap: [difference]
- Baseline scope classification: [confirmed baseline / new request / disputed / unverified]
- Scope evidence: [approved story, design, scope document, change approval, version/date/section]
- Original planned release or milestone: [value or unknown]
- Evidence confidence: [verified / partially verified / unverified]

#### Source trail
| Evidence ID | Source type | Date/time | Author / participants | Durable link / exact locator | Relevant statement or summary | Verification note |
|---|---|---|---|---|---|---|
| E-01 | [story/email/meeting/file] | [date] | [names] | [link, subject, page, timestamp] | [quote or clearly marked paraphrase] | [note] |

For meetings, identify the meeting and minutes or recording timestamp where available. For emails, preserve date, sender, subject, and an approved shared copy/reference. Do not overwrite earlier evidence when a later discussion contradicts it. Follow IU retention and data-handling policies.

#### Impact and proposed disposition
- Business priority and rationale: [value]
- Go-live criticality and rationale: [value]
- Affected users / process / budget cycle: [description]
- Data, integration, reporting, accessibility, security, or approval dependency: [description or none]
- Deloitte recommendation: [deliver / defer / reject / clarify]
- Recommendation author/date and stated rationale: [details]
- Proposed workaround: [steps or none]
- Workaround owner, feasibility, effort, risks, and duration: [details]
- Impact if deferred: [business consequence]
- Estimate and cost treatment: [provided by whom/date; unestimated if unknown]
- Proposed target release: [value or uncommitted]

#### IU decision and delivery tracking
- Decision state: [value]
- Authorized IU decision-maker: [name/role; authority to be confirmed]
- Decision, date, and approval evidence: [details or pending]
- Change-request / governance decision link: [link or not yet issued]
- Accepted residual risk and accountable owner: [details or not accepted]
- Delivery state: [value]
- Release treatment: [value]
- Delivery commitment: [committed / proposed / uncommitted]
- Commitment evidence and delivery owner: [details]
- Next action, owner, and due date: [details]
- Next review date: [date]
- Escalation trigger and recipient: [details]

#### Validation and closure
- Acceptance criteria: [numbered, testable criteria]
- Test/UAT evidence: [links]
- IU validator and validation date: [details]
- Closure outcome, approval, and date: [details or open]
- Remaining limitations and linked follow-up items: [details]

#### Append-only decision history
| Date | Actor | Previous state | New state / recommendation | Rationale | Evidence / approval | Next action |
|---|---|---|---|---|---|---|

## Initial reconstruction procedure
1. Agree who maintains the register and who can approve scope/release changes for IU.
2. Request Deloitte's current backlog, deferred-item list, release plan, decision log, and change requests. Request the status history where available, not just current labels.
3. Inventory relevant user stories, shared Teams files, meeting notes, and emails. Start with agreed requirements, go-live needs, and explicitly deferred items.
4. Capture candidate items before resolving them. Mark uncertainty rather than inventing approvals, dates, or commitments.
5. Deduplicate against story IDs and the actual business requirement; retain all supporting sources.
6. For each item, compare original requirement, implemented behavior, proposed disposition, and evidence of IU approval.
7. Hold an IU–Deloitte reconciliation session. Record agreements and unresolved scope disputes separately.
8. Have IU review proposed deferrals and business impacts. Publish a dated baseline snapshot and unresolved decisions.
9. Repeat reconciliation as new communications arrive; do not let meeting notes become the only record.

Suggested search terms for the historical sweep: backlog, phase 2, future, enhancement, out of scope, post-go-live, later release, workaround, deferred, not supported, parking lot, and change request. A keyword match is a candidate, not proof of agreement.

## Proposed weekly review agenda
- New items and missing baseline evidence.
- Proposed deferrals and unresolved IU decisions.
- High-impact gaps, go-live dependencies, and unapproved workarounds.
- Overdue next actions and items with no owner or release commitment.
- Items ready for IU acceptance; validate evidence before closure.
- Updated future-feature index and release implications.

Record decisions and distribute the updated register after each review. Agree escalation timeframes locally; do not imply a contractual service level.

## Readiness summary template
Report counts as of a stated date, distinguishing:
- Open confirmed-baseline items.
- Proposed deferrals awaiting IU decision.
- Approved deferrals with documented risk/workaround acceptance.
- Disputed or unverified scope items.
- Items without an owner, next action, or review date.
- Items marked delivered but awaiting IU validation.

Surface critical individual items as well as counts. This summary supports go-live decisions; it does not replace the project's formal acceptance authority.

## Sources
- [S1] PMI, Scope change control: https://www.pmi.org/learning/library/scope-control-projects-you-6972
- [S2] PMI, Top five causes of scope creep (requirements traceability and authorized change): https://www.pmi.org/learning/library/top-five-causes-scope-creep-6675
