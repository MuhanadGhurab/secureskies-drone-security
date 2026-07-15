# Requirements Traceability (Public)

Requirements are **historical targets**. Do not read “requirement listed” as “feature completed.”

## Functional

| Requirement | Original intent | Historical evidence | Final status |
|-------------|-----------------|---------------------|--------------|
| Autonomous flight / navigation | Patrol / navigate autonomously | Partial FC/RPi tooling | Partially complete |
| Remote control | Operator control path | Mission Planner / GUI concepts | Partially complete |
| Real-time video streaming | Live surveillance feed | FPV/Pixhawk path claims | Partially complete |
| Media capture | Record / capture media | UI mockups | Designed only |
| Waypoints | Mission waypoints | Mission Planner tooling tests | Partially complete |
| Obstacle avoidance | Sense-and-avoid | Not evidenced as delivered | Not implemented |
| Battery monitoring | Operator battery awareness | UI concept | Designed only |
| Flight logs / telemetry | Logs and telemetry | Mission Planner monitoring claims | Partially complete |
| Network monitoring | Observe network traffic | Wireshark/tcpdump install/pass | Partially complete |
| Intrusion detection / IDPS | Detect/prevent intrusion | Unnamed IDPS integrate claim | Partially complete |
| Alert generation | Operator alerts | Conceptual flows | Designed / partial |
| Cloud storage | Store media/data | AWS Console integration claim | Partially complete |
| Manual intervention | Human override | GUI concept | Designed only |
| Fail-safe operation | Failsafe / RTH | Validation attempted | **Tested — fail** |

## Non-functional

| Requirement | Final status | Notes |
|-------------|--------------|-------|
| Communication reliability | Tested — fail (gateways) / partial elsewhere | Secure low-latency gateway fail |
| Video quality | Unclear | “4K” historically claimed — unverified |
| Security & privacy (encryption/auth) | Not tested as pass | Compliance check failed |
| Environmental resilience | Not tested | — |
| Flight endurance / range | Not tested | — |
| Regulatory compliance / geofencing | Tested — fail | — |
