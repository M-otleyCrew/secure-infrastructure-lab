# Firewall Policy Matrix
Working design intent only; not vendor-specific commands.

| ID | Source | Destination | Service | Action | Rationale |
|---|---|---|---|---|---|
| P01 | WAN | DMZ reverse proxy | HTTPS only, if required | Allow | Minimal public exposure |
| P02 | WAN | Internal zones | Any | Deny | No direct inbound access |
| P03 | Users | Servers | Approved application ports | Allow | Required business workflow only |
| P04 | Users | Management | Any | Deny | Protect privileged interfaces |
| P05 | Management | Named server management IPs | Required admin protocols | Allow + log | Admin access from approved source |
| P06 | DMZ | Servers | Required backend port(s) only | Allow + log | Narrow application path |
| P07 | DMZ | Users / Management / Backup | Any | Deny | Prevent unnecessary lateral movement |
| P08 | Backup server | Protected servers | Vendor-documented backup ports | Allow + log | Scheduled backup jobs |
| P09 | Users / DMZ | Backup repository | Any | Deny | Reduce direct access to backup storage |
| P10 | Backup zone | WAN | Any | Deny by default | Add only approved update destinations |
| P99 | Any unlisted inter-zone flow | Any | Any | Deny | Default-deny baseline |

## Before implementation
- Confirm application and backup products.
- Verify exact ports and traffic direction in official product documentation.
- Restrict rules to explicit hosts/address groups where practical.
- Document owner, review date and expiry for temporary exceptions.
- Test allowed and denied paths.
