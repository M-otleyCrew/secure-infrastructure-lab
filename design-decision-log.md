# Design Decision Log

| ID | Decision | Reason | Trade-off / follow-up |
|---|---|---|---|
| D01 | Separate user, server, management, DMZ and backup zones | Reduces unnecessary communication and lateral movement paths | Requires explicit routing and rules |
| D02 | Default deny between zones | New traffic is blocked without a documented requirement | Requires inventory of legitimate application flows |
| D03 | Restrict management access to a dedicated admin path | Reduces exposure of privileged interfaces | Admin path must be secured and monitored |
| D04 | Restrict access to the backup repository | Helps protect recovery copies from ordinary endpoints | Exact backup ports and recovery process must be documented |
| D05 | Write vendor-neutral intent before vendor-specific config | Makes policy easier to review | Convert only after confirming product requirements |

Add new entries with date, decision, context, alternatives, reason selected and validation evidence.
