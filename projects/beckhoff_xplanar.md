# Beckhoff XPlanar 6DOF Position Measurement

## Goal
The primary objective of this project is to measure the 6-Degrees-of-Freedom (6DOF) pose of a Beckhoff XPlanar mover using a custom stereovision tracking system.

![Beckhoff XPlanar Mover Setup](images/xplanar-system.jpg)
*Figure 1: The Beckhoff XPlanar system featuring floating magnetic movers.*
---

## Real-Time Compatibility
To preserve strict real-time compatibility and avoid external hardware bottlenecks, all computer vision and estimation algorithms are developed and executed directly within the **TwinCAT PLC** environment. 

This approach minimizes communication latency between the vision system and the motion controllers, allowing the 6DOF data to be utilized efficiently in deterministic control loops.

---

## Implementation
The physical and software architecture relies on tight integration between industrial hardware and native TwinCAT libraries:

* **Hardware Component:** A custom-built, rigid frame mounted with precise LED markers to facilitate high-contrast detection.
* **Vision Acquisition:** Stereovision algorithms executed via **TwinCAT Vision**, processing dual-camera inputs directly on the industrial PC (IPC).

![Stereovision Camera Tracking Setup](images/stereovision-calibration.jpg)
*Figure 2: Schematic configuration of the stereovision tracking system and spatial calibration setup.*

---

## Results
The embedded stereovision system achieves high-precision tracking metrics across all 6 degrees of freedom:

| Metric | Target Accuracy |
| :--- | :--- |
| **Translational Accuracy** | Micrometer ($\mu\text{m}$) level |
| **Rotational Accuracy** | Milliradian ($\text{mrad}$) level |

> [!NOTE]
> This level of accuracy proves that hard real-time vision tracking is highly viable when processed directly in the PLC layer, opening up advanced closed-loop options for floating planar systems.
