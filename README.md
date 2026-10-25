# ComfortFlex Edge

**Intelligent Building Energy Monitoring & Optimization using Nordic nRF54LM20**

ComfortFlex Edge is a prototype building-energy intelligence system designed to move beyond simply displaying electricity consumption. It combines distributed sensing, Bluetooth LE communication, edge intelligence, anomaly detection, comfort context, actionable recommendations, and verification.

## Core concept

**SENSE → UNDERSTAND → DETECT → RECOMMEND → ACT → VERIFY**

The system will:

- Collect electrical measurements from selected loads.
- Collect environmental and occupancy/context information.
- Communicate meaningful measurements and events using Bluetooth LE.
- Use the **nRF54LM20 DK** as the central Bluetooth and edge-intelligence platform.
- Learn normal operating patterns for monitored loads.
- Detect abnormal consumption, prolonged operation, standby waste, and high-demand events.
- Combine energy information with comfort and occupancy constraints.
- Recommend practical energy-saving actions.
- Demonstrate a safe controlled load.
- Measure the result and compare predicted and actual behaviour.

## Why nRF54LM20?

The nRF54LM20 platform provides the Bluetooth LE and processing capabilities needed for a low-power distributed sensing system. The nRF54LM20B variant also provides the integrated **Axon NPU**, which will be investigated for accelerating a lightweight TensorFlow Lite edge-AI model.

The project will focus on using the development kit as a genuine part of the system architecture rather than simply replacing an existing microcontroller.

## Main prototype

The first prototype will target:

1. One nRF54LM20 DK.
2. One or more electrical sensing points.
3. Temperature/humidity sensing.
4. Occupancy/presence context.
5. Bluetooth LE telemetry.
6. Edge-based operating-pattern/anomaly classification.
7. A safe, isolated controllable demonstration load.
8. A simple dashboard or visualization layer.

## Example insights

The system may generate events such as:

- Normal appliance operation
- Abnormal energy behaviour
- High-demand event
- Possible standby waste
- Prolonged operating cycle
- Comfort-safe energy-saving opportunity
- Flexible load available

The system will report an anomaly as a condition requiring investigation rather than claiming a specific equipment failure without sufficient evidence.

## Example use case

If a refrigerator normally follows a stable daily energy pattern but its consumption progressively rises above its learned baseline, ComfortFlex Edge can flag the change for inspection.

Similarly, if a water-heater cycle is longer than its normal operating pattern, the system can recommend changing the next cycle timing where the user's constraints allow it.

## Bluetooth LE

Bluetooth LE will provide the low-power communication layer between distributed sensing nodes and the central intelligence node.

The system is intended to transmit useful measurements, states and events rather than relying on continuous raw-data streaming.

Bluetooth Channel Sounding may also be investigated as an optional advanced feature for obtaining spatial/context information such as relative distance or presence between compatible nodes.

## Edge AI

The first AI task is intentionally lightweight:

**Input:** power/current/voltage-derived features, operating duration, time/context and previous state.

**Output:** operating behaviour classification such as:

- Normal
- Abnormal
- Prolonged operation
- High-demand
- Standby/waste pattern

For the nRF54LM20B, the project will investigate deployment of a quantized TensorFlow Lite model using the integrated Axon NPU.

## Safety

Any mains-energy measurement or switching will use appropriate isolation, protection and supervision. The initial demonstration should prefer a safe low-voltage load or an appropriately isolated commercial measurement/control module.

This repository does not provide a design for directly switching mains electricity.

## Project status

This is the initial project structure and BOM for the Nordic nRF54LM20 challenge application. Hardware, firmware, datasets and model files will be added as the prototype develops.

## Repository structure

```text
ComfortFlex-Edge/
├── README.md
├── BOM.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── architecture.md
│   └── prototype-plan.md
├── hardware/
│   ├── nrf54lm20/
│   ├── energy-sensing/
│   └── control/
├── firmware/
│   └── nrf54lm20/
└── edge-ai/
    ├── dataset/
    ├── training/
    └── model/
```

## Planned development stages

### Stage 1 — Sense
Establish energy and environmental measurements.

### Stage 2 — Connect
Implement Bluetooth LE telemetry using the nRF54LM20 platform.

### Stage 3 — Understand
Create baselines and operating-state features.

### Stage 4 — Detect
Deploy lightweight anomaly/operating-pattern classification at the edge.

### Stage 5 — Recommend
Generate actionable recommendations using energy, comfort, occupancy and time context.

### Stage 6 — Act
Demonstrate a safe controllable load.

### Stage 7 — Verify
Measure the actual response and compare it with the predicted result.

## Project objective

ComfortFlex Edge aims to demonstrate that building energy monitoring can evolve from a passive dashboard into a low-power, distributed intelligence system that can understand physical behaviour and recommend what should happen next.
