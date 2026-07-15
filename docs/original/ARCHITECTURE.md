# Original Architecture

> Label for all diagrams: **Modern public reconstruction based on the original academic report.**

## Actors and components

- Operator / security personnel
- Mission Planner (ground tooling)
- Raspberry Pi companion computer
- Pixhawk flight controller
- GPS, motors/ESCs, FPV camera, telemetry radio
- Network monitoring tools and unnamed IDPS concept
- AWS Console / cloud concepts (services unspecified)
- Alert management concepts / operator interface mockups

## Trust boundaries (historical concept)

1. Operator device ↔ ground tools
2. Ground ↔ drone (telemetry / video)
3. Companion computer ↔ flight controller
4. Companion computer ↔ cloud
5. Companion computer ↔ monitored network concept

## Use case

```mermaid
flowchart LR
  OP[Operator] -->|configure / monitor| MP[Mission Planner]
  OP -->|alerts UI concept| AL[Alert management]
  MP --> RPI[Raspberry Pi]
  RPI --> PX[Pixhawk]
  RPI --> NET[Network monitor / IDPS]
  RPI --> AWS[AWS Console / cloud]
  PX --> GPS[GPS]
  PX --> MOT[Motors]
  PX --> CAM[FPV camera]
  NET --> AL
  CAM --> RPI
```

## Data / control flow

```mermaid
sequenceDiagram
  participant Op as Operator
  participant MP as Mission Planner
  participant Pi as Raspberry Pi
  participant PX as Pixhawk
  participant Cloud as AWS Console
  Op->>MP: mission / constraints
  MP->>Pi: configuration
  Pi->>PX: flight directives
  PX-->>Pi: telemetry / video path
  Pi->>Cloud: media / data upload concept
  Pi-->>Op: alerts monitoring concept
```

## Component flow

```mermaid
flowchart TB
  subgraph Ground
    OP[Operator]
    MP[Mission Planner]
    AL[Alert concepts]
  end
  subgraph Air
    RPI[Raspberry Pi]
    PX[Pixhawk]
    SENS[GPS / FPV / Motors]
  end
  subgraph CloudConcept
    AWS[AWS Console]
  end
  OP --> MP
  OP --> AL
  MP --> RPI
  RPI --> PX
  PX --> SENS
  RPI --> AWS
  RPI --> AL
```

## Operator interaction flow

```mermaid
flowchart TD
  A[Open management device] --> B[Authenticate - designed mockup]
  B --> C[Configure Mission Planner]
  C --> D[Monitor telemetry / video]
  D --> E{Alert?}
  E -->|yes| F[Review alert management]
  E -->|no| D
  F --> G[Manual intervention concept]
```

## Alert-management flow

```mermaid
flowchart LR
  MON[Network monitoring / IDPS] --> DET[Suspicious activity]
  DET --> AL[Alert / report]
  AL --> CC[Control center / operator]
  CC --> RES[Response / further action]
```

## Power-flow summary

```mermaid
flowchart TD
  BAT[Battery / power path] --> PM[Power module]
  PM --> PX[Pixhawk / telem]
  PM --> CAM[FPV / video path]
  PB[USB power bank] --> RPI[Raspberry Pi]
```

## Known historical inconsistencies (not guess-resolved)

| Topic | Tension |
|-------|---------|
| Abstract vs conclusion | Abstract language vs incomplete deployment |
| Sensor design mentions | Some design text vs camera/GPS-centric hardware list |
| “Raspberry Pi API” | Named API but described as terminal CLI |
| AWS | Console named; services unnamed |
| Testing narrative | Passes coexist with explicit fails and inconclusive results |
