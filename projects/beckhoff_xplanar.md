---
layout: default
title: Beckhoff XPlanar 6DOF Position Measurement Tool
---

## Objective
The primary objective of this project is to measure the 6-Degrees-of-Freedom (6DOF) pose of a Beckhoff XPlanar mover using a custom stereovision tracking system.

<p align="center">
  <img src="xplanar-system.jpeg" width="220" alt="XPlanar System">
</p>

*Figure 1: LED Frame Mounted on the XPlanar Mover.*
---

## Imlementation
To preserve strict real-time compatibility and avoid external hardware bottlenecks, all computer vision and estimation algorithms are developed and executed directly within the **TwinCAT PLC** environment. 

This approach minimizes communication latency between the vision system and the motion controllers, allowing the 6DOF data to be utilized efficiently in deterministic control loops.

The physical and software architecture relies on tight integration between industrial hardware and native TwinCAT libraries:

* **Hardware Component:** A custom-built, rigid frame mounted with precise LED markers to facilitate high-contrast detection.
* **Vision Acquisition:** Stereovision algorithms executed via **TwinCAT Vision**, processing dual-camera inputs directly on the industrial PC (IPC).

<p align="center">
  <img src="camera-setup.jpeg" width="220" alt="Camera Setup">
</p>
*Figure 2: Full Stereovision Camera Setup.*

---

## Results
The embedded stereovision system achieves high-precision tracking metrics across all 6 degrees of freedom:

| Metric | Target Accuracy |
| :--- | :--- |
| **Translational Accuracy** | Micrometer ($\mu\text{m}$) level |
| **Rotational Accuracy** | Milliradian ($\text{mrad}$) level |

