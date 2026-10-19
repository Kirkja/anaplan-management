# Anaplan Modelers Reference Guide

Version: 1.0 | Prepared: 2026-10-19

Scope: General Anaplan reference, not an organization-specific runbook. Available features and permissions depend on your tenant, subscription, model, and configuration. Recommended operating practices below are templates, not assertions about your environment.

## Audience and purpose
For model builders, solution architects, and technical reviewers. Use this as a design, testing, and release checklist rather than a substitute for model-specific specifications.

## Design before building
Document:
- Business decision, process owner, users, and acceptance criteria.
- Required outputs and their grain: for example, product × region × month.
- Inputs, source systems, identifiers, refresh cadence, and reconciliation rules.
- Lists, hierarchies, time requirements, versions/scenarios, and expected growth.
- Access requirements, approval rules, and exception handling.
- Model boundaries, dependencies, integration responsibilities, and lifecycle approach.

Define the required outputs first, then work backward through calculations, inputs, and source data.

## DISCO module organization
DISCO separates modules by responsibility. The acronym means Data, Input, System, Calculation, and Output. [S1]

| Category | Intended responsibility | Review question |
|---|---|---|
| Data | Staged or imported source data | Can it be reconciled to its source? |
| Input | User-maintained assumptions and planning inputs | Are inputs validated and appropriately restricted? |
| System | Shared mappings, attributes, and reusable supporting logic | Is common logic defined in one clear place? |
| Calculation | Business transformations and calculations | Is each result understandable and testable? |
| Output | Reporting, UX, and integration-facing results | Does the output match the business-required grain? |

Adopt your CoE’s naming convention; DISCO does not require a particular prefix scheme.

## Module and line-item review
For each module, document its purpose and applicable dimensions. For each material line item, review:
- Business definition, data type/format, formula or source.
- Required dimensions, time scope, and scenario/version treatment.
- Aggregation behavior and expected totals.
- Missing-data, zero, sign, rounding, and exception behavior.
- Access drivers and read/write expectations.
- Downstream consumers and reconciliation requirements.

Recommended design practices: avoid unnecessary dimensionality; reuse shared mappings; isolate complex transformations; explain non-obvious formulas; measure performance using representative data rather than assuming a change is faster.

## Access design
Model roles, selective access, and dynamic cell access solve different problems. Selective access controls list-item scope; dynamic cell access controls cells using Boolean drivers configured in Blueprint. [S2][S3]

Test at least:
- Allowed and prohibited entities.
- Read-only versus editable periods or scenarios.
- Hidden versus visible data.
- Ordinary-user actions and imports.
- Intended administrator behavior separately.

Workspace administrators can import files into cells without dynamic cell write access. Include non-administrator testing for restricted workflows. [S3]

## Integration contract template
```text
Integration name and owner:
Source / destination:
Business purpose and cadence:
Record grain and stable identifiers:
Required columns and data types:
Time, currency, and unit conventions:
Mapping and rejection rules:
Reconciliation totals and tolerances:
Rerun / duplicate-handling procedure:
Failure notification and escalation:
```

## Test matrix
| Test class | Example evidence |
|---|---|
| Calculation | Known inputs, expected outputs, actual outputs |
| Aggregation | Detail-to-total reconciliation |
| Boundary | Zero, missing values, new members, period boundaries |
| Security | Representative ordinary-user allow/deny tests |
| Integration | Accepted/rejected records and control totals |
| Regression | Previously accepted business cases still pass |
| Performance | Representative workload and measured timing |
| UAT | Business owner acceptance against stated criteria |

## ALM release workflow
1. Develop structural changes in the compatible source model in Standard mode.
2. Test calculations, integrations, access, and critical user journeys.
3. Add a revision tag identifying the intended structural state.
4. Review and synchronize changes into a compatible test target.
5. Obtain business acceptance and production approval.
6. Compare and synchronize into the compatible production target.
7. Reconcile data, run smoke tests, and record deployment evidence.

Revision tags capture structural development states for comparison and synchronization. Anaplan recommends keeping test and production targets in Deployed mode. Do not disable that mode to edit production structure. [S4][S5]

Production data and structural changes need separate impact and recovery analysis. A revision tag is not a substitute for a complete data-recovery plan.

## Definition of done
- Requirements and acceptance criteria satisfied.
- Model and integration design documented.
- Tests and reconciliation evidence recorded.
- Security tested using appropriate non-admin roles.
- Peer review complete and exceptions approved.
- Release/recovery procedure documented.
- User guidance and operational ownership updated.

## Sources
- [S1] DISCO methodology: https://community.anaplan.com/discussion/44188/time-to-tidy-no-more-mess-in-your-models
- [S2] Selective access: https://help.anaplan.com/selective-access-f0dd364d-cd04-429e-b788-15c79d8cf698
- [S3] Dynamic cell access: https://help.anaplan.com/dynamic-cell-access-55ae93e6-5139-4bbf-93f9-c8cb06f68f75
- [S4] ALM development lifecycle: https://help.anaplan.com/how-application-lifecycle-management-supports-the-development-lifecycle-aa369576-4135-4a3e-8636-1a942c28feaa
- [S5] Deployed mode considerations: https://help.anaplan.com/considerations-when-you-enable-deployed-mode-5dea12f4-57c4-4b57-a2cb-97bdfe5d007e
