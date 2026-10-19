# Anaplan Users Reference Guide

Version: 1.0 | Prepared: 2026-10-19

Scope: General Anaplan reference, not an organization-specific runbook. Available features and permissions depend on your tenant, subscription, model, and configuration. Recommended operating practices below are templates, not assertions about your environment.

## Audience and purpose
For planners, contributors, reviewers, and report consumers. Use this guide to navigate planning work, enter data carefully, and report problems with enough context to resolve them.

## Quick reference
| Need | What to check or do |
|---|---|
| Find your work | Open the assigned app and page; confirm the intended planning process. |
| Understand the view | Check entity, period, scenario/version, currency, units, and filters before interpreting values. |
| Enter values | Work only in cells made editable for your role and process. |
| Review detail | Use a worksheet when the process requires detailed grid work. |
| Run an action | Confirm its purpose, input scope, and expected result before running it. |
| Export | Use an available export action and follow your organization’s data-handling policy. |
| Report an issue | Capture page, context selections, timestamp, expected result, and actual result. |

## Core concepts
- App: the organized user experience for a business process.
- Board: a page used to present information through cards and visualizations.
- Worksheet: an interactive grid with an Insights panel for additional context.
- Context: selections such as time, entity, or scenario that determine the data you see.
- Action/process: configured operations that may import, export, or update model data. Your organization should document their effects.

Anaplan documents boards and worksheets as ways to view and edit model data. Worksheets can expose import, export, and process actions. [S1][S2]

## Standard planning workflow
1. Confirm the planning cycle, deadline, and assigned business scope.
2. Open the designated page and verify context, filters, units, and currency.
3. Review actuals, baseline assumptions, and the latest available source-data date.
4. Enter or update permitted inputs.
5. Review totals, variances, and configured validation messages.
6. Follow the organization’s approval or submission procedure, if one exists.
7. Record material assumptions and unresolved exceptions in the designated location.

Do not assume a Submit button, approval workflow, or universal save procedure exists. These depend on the implementation.

## Read-only or missing data
Possible areas for the support team to investigate include model roles, selective access, dynamic cell access, page context, and workflow-specific locks. Selective access controls list items; dynamic cell access can make cells editable, read-only, or hidden. [S3][S4]

Before requesting a change:
- Confirm you are in the correct app, page, planning cycle, and entity.
- Record which cells or records are affected.
- Explain the business access you need; do not request administrator access as a shortcut.
- Avoid including confidential values in screenshots unless the support channel permits them.

## Imports, processes, and exports
- Use only approved files and templates; verify identifiers, periods, units, and headers.
- Review action results and exceptions before treating a load as complete.
- If an action appears interrupted, check its outcome before repeating it.
- Export layouts may be predefined in the source model. Do not assume every visible grid has the same export options. [S5]

## Support request template
```text
Business process:
App and page:
Model, if known:
Date/time and time zone:
Context selections and filters:
Action taken:
Expected result:
Actual result / exact error:
Scope: one user / multiple users / unknown
Business impact and deadline:
Screenshot or approved example:
```

## Sources
- [S1] Anapedia: https://help.anaplan.com/
- [S2] Worksheet pages: https://help.anaplan.com/worksheet-pages-1cc11f1c-1447-4510-833d-cc393e8d9846
- [S3] Selective access: https://help.anaplan.com/selective-access-f0dd364d-cd04-429e-b788-15c79d8cf698
- [S4] Dynamic cell access: https://help.anaplan.com/dynamic-cell-access-55ae93e6-5139-4bbf-93f9-c8cb06f68f75
- [S5] Add export actions to a page: https://help.anaplan.com/add-export-actions-to-a-page-d5b55014-1eaf-42ed-92a1-88218225b11c
