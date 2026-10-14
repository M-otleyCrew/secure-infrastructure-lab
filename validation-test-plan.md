# Validation Test Plan
Run only in a lab you own or are explicitly authorized to assess.

| ID | Test | Expected result | Result | Evidence / notes |
|---|---|---|---|---|
| T01 | User endpoint → approved business application | Required service succeeds | Not tested | |
| T02 | User endpoint → server management interface | Blocked | Not tested | |
| T03 | DMZ endpoint → backup repository | Blocked | Not tested | |
| T04 | Admin workstation → approved management endpoint | Allowed | Not tested | |
| T05 | External test host → lab public address | Only intended public service exposed | Not tested | |
| T06 | Backup server → protected server during job | Documented backup flow succeeds | Not tested | |
| T07 | Restore a harmless test file | Restore succeeds and integrity is checked | Not tested | |
| T08 | Review denied cross-zone logs | Useful source, destination, service and action are recorded | Not tested | |

For each test, record date/time, source and destination (private lab addresses only), command/GUI action, expected and actual result, Pass/Fail/Not tested, sanitized evidence, and follow-up action.

Do not mark a test Pass until it has actually been executed. Remove credentials, tokens, public IPs and personal information before publishing evidence.
