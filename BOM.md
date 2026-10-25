# Bill of Materials — Initial Version

This is the beginning of the project BOM. Prices are approximate planning estimates in USD and may change by supplier and location.

**Reference conversion used:** 1 USD ≈ ₹94.76 (25 October 2026). citeturn0search14

| Component | Qty | Est. Unit Price (USD) | Est. Total (USD) | Project Cost | Purpose |
|---|---:|---:|---:|---:|---|
| Nordic nRF54LM20 DK | 1 | $45.38 | $45.38 | **$0 — Challenge hardware** | Central Bluetooth LE + Edge AI platform |
| Current / energy sensing module | 1 | $3.17 | $3.17 | Self-sourced | Load monitoring |
| Voltage sensing circuit/module | 1 | $1.05 | $1.05 | Self-sourced | Voltage measurement |
| Temperature sensor | 1 | $1.05 | $1.05 | Self-sourced | Comfort/environment monitoring |
| Humidity sensor | 1 | $1.05 | $1.05 | Self-sourced | Environmental context |
| Occupancy/presence sensor | 1 | $1.58 | $1.58 | Self-sourced | Occupancy/context information |
| Isolated switching module | 1 | $1.58 | $1.58 | Self-sourced | Safe load control |
| Low-voltage demonstration load | 1 | $2.11 | $2.11 | Self-sourced | Controlled-load demonstration |
| Jumper wires/connectors | 1 set | $1.58 | $1.58 | Self-sourced | Prototyping |
| Breadboard/prototyping hardware | 1 | $1.58 | $1.58 | Self-sourced | Initial prototype |

## Estimated budget

| Category | Estimated Cost |
|---|---:|
| nRF54LM20 DK reference value | **$45.38** |
| nRF54LM20 DK actual project cost | **$0.00** |
| Other prototype hardware | **$14.77** |
| Total reference hardware value | **$60.15** |
| Estimated out-of-pocket prototype cost | **$14.77** |

## nRF54LM20 DK role

The nRF54LM20 DK is the core processing and wireless platform.

Planned responsibilities:

- Bluetooth LE communication
- Sensor-data reception
- Feature extraction
- Operating-state tracking
- Edge-AI inference
- Anomaly/event generation
- Recommendation inputs
- Communication with the visualization layer

## Pricing notes

- The nRF54LM20 DK is shown with an estimated reference value but **$0 project cost** because it is being requested through the Nordic challenge.
- Other component prices are planning estimates, not supplier quotations.
- Exact sensor part numbers will be finalized after the sensing architecture is selected.
- The BOM will be updated with exact part numbers, suppliers and actual purchase prices as the prototype develops.

## Safety

The initial prototype should avoid unsafe direct mains experimentation.

Any mains measurement/control must use appropriate isolation, protection, enclosure and supervision. A safe low-voltage demonstration load is preferred for the first prototype.
