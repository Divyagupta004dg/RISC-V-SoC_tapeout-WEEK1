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


🟢 Procedural Assignments in Verilog

Verilog supports two styles of procedural assignments inside always blocks. These define how values are updated and whether execution is sequential or concurrent.

🟢 Type 1: Blocking Assignment

● Symbol: =
● Execution style: Runs one statement at a time, in strict order.
● Best suited for: Modeling combinational logic (always @(*)).
● Example:

``always @(*)  
  y = a & b; `` 

🟢 Type 2: Non-Blocking Assignment

● Symbol: <=
● Execution style: Updates are scheduled and applied at the end of the current time step.
● Best suited for: Sequential circuits triggered by a clock (always @(posedge clk)).
● Example:

``always @(posedge clk)  
  q <= d;  ``

#  Lab 1: Ternary Operator MUX

<img width="1337" height="956" alt="image" src="https://github.com/user-attachments/assets/0ac7f251-9176-4534-8e85-030a4ec18b86" />

# Lab 2: Synthesis Using Yosys

<img width="1998" height="806" alt="image" src="https://github.com/user-attachments/assets/23abe6de-b572-458b-9d00-e5c2732b044b" />

# Lab 3: Gate-Level Simulation of( MUX)

<img width="1383" height="970" alt="image" src="https://github.com/user-attachments/assets/4afd07c1-7c4f-406d-9ab2-705dc7cb0d1f" />

# Lab 4: GLS of Bad MUX

<img width="1295" height="979" alt="image" src="https://github.com/user-attachments/assets/eb58172a-f669-40d9-a4fb-e941066d857a" />

# Lab 5: Blocking Assignment Caveat

<img width="1185" height="974" alt="image" src="https://github.com/user-attachments/assets/b320abf2-cddf-400c-84c5-6a580406961e" />

# Lab 6: Synthesis of the Blocking Caveat

<img width="1974" height="825" alt="image" src="https://github.com/user-attachments/assets/64b1ae31-f060-4c91-a16a-6fa9d249082e" />
