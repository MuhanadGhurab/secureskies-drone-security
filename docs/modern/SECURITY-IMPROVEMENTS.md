# Security Improvements (Modern Proposal)

> **Modern proposal — not part of the original implementation.**

| Control area | Proposal theme |
|--------------|----------------|
| Device identity | Unique device identities for companion computer and ground station roles |
| Mutual authentication | Authenticate endpoints before accepting commands or telemetry |
| Message integrity | Integrity protection for telemetry and control messages |
| Replay detection | Detect and reject replayed command/telemetry frames |
| Role-based access | Operator roles with least privilege |
| Signed configuration | Sign mission/config packages before acceptance |
| Audit trails | Immutable or append-only operator action logs |
| Key-management model | Rotation, storage, and separation of duties |
| Secure updates | Signed update packages for companion software |
| Monitoring | Defensive monitoring of twin/simulation events |
| Incident-response controls | Playbooks for suspected compromise in simulated environments |

These controls are design targets for future simulation and documentation — not claims about 2024.
