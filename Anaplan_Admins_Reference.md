# Anaplan Admins Reference Guide

Version: 1.0 | Prepared: 2026-10-19

Scope: General Anaplan reference, not an organization-specific runbook. Available features and permissions depend on your tenant, subscription, model, and configuration. Recommended operating practices below are templates, not assertions about your environment.

## Audience and purpose
For tenant administrators, workspace administrators, access owners, and operational support teams. Administration is a set of distinct responsibilities, not one interchangeable permission level.

## Administration boundaries
| Layer | Reference responsibility | Control consideration |
|---|---|---|
| Tenant | Tenant administration and assignment of administration roles | Document which delegated role performs each task. |
| Workspace/model | Workspace administration and model access configuration | Separate privileged administration from normal planning activity. |
| Model roles | Permissions to model features and data areas | Use approved roles rather than broad access by default. |
| Selective access | User-specific access to list items | Verify expected read/write scope after changes. |
| Dynamic cell access | Boolean-driven cell visibility and editability | Test access-driver behavior with representative users. |

Tenant administrators assign administration roles through Administration. Workspace administrators configure model access through model roles, selective access, and model contents. [S1]

## Access provisioning checklist
1. Obtain a request identifying user, business sponsor, model/process, requested scope, and duration.
2. Confirm approval under the organization’s access policy.
3. Verify identity and the intended tenant/workspace/model.
4. Assign the approved model role and applicable selective access.
5. Validate access with a representative non-administrator account or approved test procedure.
6. Record approver, implementer, timestamp, access granted, and verification evidence.
7. Set a review or expiration date where required by policy.

For transfers and departures, reconcile access across all relevant workspaces, models, and associated identity-management processes. Treat the steps above as a governance template, not a complete identity-provider integration procedure.

## Important security distinctions
- Selective access restricts lists and list items. Enabling it leaves ordinary users without access until access is assigned. Workspace administrators retain the ability to open and amend the list. [S2]
- Dynamic cell access uses Boolean access drivers to make cells editable, read-only, or hidden. [S3]
- A workspace administrator can import from a file into cells without dynamic cell write access. Do not rely on an administrator test to demonstrate ordinary-user restrictions. [S3]
- Hiding a page element is not a substitute for verifying underlying model access.

## Recommended operational checks
### Before a planning cycle
- Confirm business owners and escalation contacts.
- Review privileged access and temporary access exceptions.
- Confirm source-data availability and integration ownership.
- Validate critical user journeys and a representative restricted role.
- Agree support coverage and change restrictions for the cycle.

### During operations
- Reconcile integration outcomes with source totals and business expectations.
- Track failed loads, unresolved exceptions, and user impact.
- Record changes to access, configuration, and integration mappings.
- Escalate failures with timestamps, affected scope, and evidence.

### Periodic review
Choose a cadence based on risk and business cycle: access recertification, privileged-role review, service/integration identity review, operational documentation review, and recovery rehearsal.

## Production change control
Anaplan recommends Deployed mode for production and test synchronization targets. Structural changes should originate in a compatible development model and move through Compare and Synchronize. Do not disable Deployed mode to make an expedient production structural edit: this can break synchronization compatibility. [S4]

Release checklist:
- Approved request and deployment window.
- Compatible source/target models and identified revision tag.
- Test evidence, business acceptance, and access validation.
- Reviewed synchronization comparison and data impact.
- Documented recovery procedure and responsible owner.
- Post-release smoke tests and business reconciliation.

Revision tags support structural lifecycle management; do not treat them as a complete recovery strategy for production data. Define and test data recovery separately.

## Incident record
```text
Incident ID / severity:
Start time / time zone:
Affected tenant, workspace, model, app:
Affected users and business deadlines:
Exact error and reproduction steps:
Recent changes:
Integration run details, if applicable:
Mitigation and owner:
Recovery validation:
Root cause and prevention actions:
```

## Sources
- [S1] Control user access within models: https://help.anaplan.com/control-user-access-within-models-8c495688-216e-49c4-aa56-a4b70487e5d7
- [S2] Selective access: https://help.anaplan.com/selective-access-f0dd364d-cd04-429e-b788-15c79d8cf698
- [S3] Dynamic cell access: https://help.anaplan.com/dynamic-cell-access-55ae93e6-5139-4bbf-93f9-c8cb06f68f75
- [S4] Considerations when you enable Deployed mode: https://help.anaplan.com/considerations-when-you-enable-deployed-mode-5dea12f4-57c4-4b57-a2cb-97bdfe5d007e
