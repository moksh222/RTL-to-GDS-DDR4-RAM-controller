# DDR4 RAM Controller: Physical Design Implementation

This repository contains the physical design documentation and project artifacts for a DDR4 RAM Controller. The project demonstrates the translation of a functional RTL design into a physical GDSII implementation using Cadence EDA tools.

## 1. Project Overview
The goal of this project was to implement a robust DDR4 RAM Controller. The design was synthesized, floorplanned, and routed to meet timing and area constraints. This repository provides a comprehensive look at the implementation through CAD-captured snapshots of the design and verification stages.


## 2. Design Specifications
Based on the implementation data:
*   **Design Module:** `ddr4_ram_controller`
*   **Total Leaf Cells:** 9,735
*   **Total Nets:** 9,787
*   **I/O Terminals:** 68
*   **Technology Target:** High-density standard cell library


## 3. Design Flow
The physical design followed a standard industry workflow:
*   **Synthesis & Netlist Generation:** The RTL was synthesized to a gate-level netlist (`ddr4_ram_controller.v`).
*   **Floorplanning:** Defining the core area and placement of standard cells to optimize for routing and power distribution.
*   **Place & Route:** Automating the physical connection of components, managing routing congestion, and ensuring signal integrity across multiple metal layers.
*   **Physical Verification:** Layout-versus-schematic (LVS) checks and density analysis to ensure readiness for fabrication.


## 4. Verification
Functional verification was performed to ensure the controller adheres to DDR4 protocols:
*   **Waveform Analysis:** Validated read/write transactions, address decoding (`addr[31:0]`), and reset/enable signal behavior.
*   **Logical Consistency:** Ensured that the gate-level schematic matches the intended functionality of the RTL code.
