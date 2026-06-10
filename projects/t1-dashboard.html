# ESP32 Smart Display Shield

A custom, dual-layer printed circuit board (PCB) designed to interface an ESP32 DevKit V1 microcontroller with an external 7-segment display module and status indicator LEDs. This project involved full-cycle hardware development, moving from initial schematic capture and circuit design to physical footprint modification, board routing, and design rule optimization within KiCad.

---

## Technical Specifications & Features

- **Microcontroller Core:** Driven by an ESP32 DevKit V1 (30-pin, 25.4mm wide variant).
- **Display System:** Interfaced with a multi-digit 7-segment display for real-time data streaming.
- **Visual Telemetry:** Triple LED status indicator subsystem configured for reliable current sourcing (High GPIO output triggers active state).
- **Form Factor & Layer Stack:** Dual-layer copper layout optimized for tight-clearance desktop enclosures, incorporating corner mechanical mounting holes for stable deployment.

---

## Engineering Challenges & Design Solutions

### 1. Component Tolerance & Footprint Modification
A primary challenge during the layout phase was adapting to variant discrepancies common among development boards. Initial footprints utilized standard $22.86\text{mm}$ ($0.9\text{ inch}$) row spacing. After physical evaluation of the target hardware, a $25.4\text{mm}$ ($1.0\text{ inch}$) row-to-row spacing discrepancy was identified. 
Instead of introducing untested library dependencies, the footprint was directly modified in the Footprint Editor by geometrically shifting the 15-pin rows by exactly $\pm1.27\text{mm}$ using precise delta-move transformations.

### 2. Signal Routing & Clearance Optimization
Widening the core microcontroller footprint compressed the routing channels running beneath the central display module and nearby passive components. This required a full optimization pass to prevent manufacturing defects:
- Track paths were re-routed around the outer boundaries of resistor pads (such as `R10`) to eliminate copper overlaps.
- Resistor spacing was dynamically adjusted to maintain clearance around adjacent ESP32 header rows (`J3`), ensuring a zero-error feedback loop from the Design Rule Checker (DRC).

### 3. Diode Polarity & Netlist Synchronization
To keep firmware execution intuitive (driving GPIO lines high to illuminate status indicators), the schematic and board netlist were completely synchronized to orient the LED anodes (`Pin 2`) directly downstream from the current-limiting resistors. Footprints were physically rotated $180^\circ$ on the canvas, aligning the internal flat edges of the silkscreen markings with the physical cathodes (`Pin 1`) sinking straight into the solid Ground copper pour.

---

## Core Tools Used

- **EDA Software:** KiCad 8.0 (Schematic Editor, PCB Layout Canvas, Footprint Editor, 3D Viewer)
- **Validation:** KiCad Design Rule Checker (DRC) for track clearance, net compliance, and manufacturing constraint verification.
- **Hardware Tools:** Digital calipers for physical prototype dimension auditing.

---

## Design Gallery

### Schematic Layout
*Clean netlist distribution showing the ESP32 GPIO channels, current-limiting resistors, properly oriented diode anodes, and integrated "No-Connection" safety flags to suppress floating pin noise.*

### 2D Copper Tracking & Silkscreen
*Top-down view of the finalized dual-layer layout showing clean horizontal routing, thermal-relief spokes on ground plane connections, and white F.Silkscreen reference text alignment.*
