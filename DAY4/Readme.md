🟢 Gate-Level Simulation (GLS) – An Overview

● Definition
Gate-Level Simulation (GLS) is a verification stage in the VLSI design process where the synthesized gate-level netlist is simulated. It ensures the design behaves correctly after RTL is transformed into logic gates.

🟢 Why GLS is Important

● Checks synthesis correctness – Confirms that the RTL is translated into gates without altering functionality.
● Verifies timing behavior – By using SDF (Standard Delay Format) files, real delays are introduced to detect setup/hold violations.
● Assesses power behavior – Provides realistic switching activity for power estimation.
● Validates test features – Ensures scan chains and DFT (Design for Testability) structures work as expected.

🟢 When Do We Run GLS?

● Post-Synthesis – Right after converting RTL to a gate-level netlist.
● Pre-Physical Design – Before floorplanning and placement, so bugs can be fixed early.

🟢 Different Modes of GLS

● Functional Gate Simulation – Focuses on logical correctness with zero or unit delays.
● Timing-Aware Gate Simulation – Uses back-annotated delays (from SDF) to reflect real hardware timing behavior.
