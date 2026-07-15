# Testing Record (Public)

Methodology in the academic report: **integration testing only**. The team stated the
prototype was too early for performance and penetration testing.

## Summary

| Metric | Count |
|--------|------:|
| Total reported test items | 24 |
| Reported pass | 20 |
| Reported fail | 3 |
| Reported inconclusive | 1 |

## Failed areas

- Secure low-latency communication gateway
- Failsafe / return-to-home / emergency landing validation
- Industry standards / regulatory compliance check

## Inconclusive area

- Machine-learning real-time threat analysis integration

## Category view

| Suite | Pass | Fail | Inconclusive |
|-------|-----:|-----:|-------------:|
| Hardware integration | 5 | 1 | 0 |
| Raspberry Pi integration | 5 | 0 | 1 |
| Flight controller integration | 5 | 1 | 0 |
| General software integration | 5 | 1 | 0 |

## Itemized results (sanitized)

| ID | Category | Result |
|----|----------|--------|
| HW-1 | Hardware assembly | Pass |
| HW-2 | Raspberry Pi boot | Pass |
| HW-3 | Battery/Pixhawk power-data path | Pass |
| HW-4 | Secure low-latency gateways | **Fail** |
| HW-5 | Performance/resilience (as scored historically) | Pass |
| HW-6 | Frame accommodation | Pass |
| PI-1 | Wireshark/tcpdump installed | Pass |
| PI-2 | Mission Planner installed | Pass |
| PI-3 | CPU/memory capacity | Pass |
| PI-4 | ML real-time threat analysis | **Inconclusive** |
| PI-5 | Centralized data exchange | Pass |
| PI-6 | Expansion readiness | Pass |
| FC-1 | Power management | Pass |
| FC-2 | FPV streaming path | Pass |
| FC-3 | RPi integration for monitoring/nav tooling | Pass |
| FC-4 | Sensor calibration (GPS/IMU) | Pass |
| FC-5 | Motor outputs | Pass |
| FC-6 | Failsafe / RTH validation | **Fail** |
| SW-1 | AWS Console ↔ RPi | Pass |
| SW-2 | IDPS ↔ RPi OS (unnamed product) | Pass |
| SW-3 | RPi OS installed | Pass |
| SW-4 | Scale for expansions | Pass |
| SW-5 | Standards / regulatory compliance | **Fail** |
| SW-6 | Inter-subsystem data exchange | Pass |

## Reproducibility

The public portfolio does **not** include raw logs, packet captures, or original source
artifacts for independent retesting.
