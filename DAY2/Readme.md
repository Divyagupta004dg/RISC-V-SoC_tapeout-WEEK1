# 1 Introduction to timing.libs

**.lib file contents**

run ``gvim ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib``

<img width="1008" height="683" alt="image" src="https://github.com/user-attachments/assets/095d2265-bee7-4703-86dc-b8bbbedce863" />


run ``gvim multiple_modules.v``

<img width="1008" height="598" alt="image" src="https://github.com/user-attachments/assets/d92cf154-83bc-4623-ae46-a07ae43f6a09" />

``yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib``

1. Executing Liberty frontend: ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
   
Imported 418 cell types from liberty file.

``yosys> read_verilog multiple_modules.v``

2. Executing Verilog-2005 frontend: multiple_modules.v

Parsing Verilog input from `multiple_modules.v' to AST representation.

Generating RTLIL representation for module `\sub_module2'.

Generating RTLIL representation for module `\sub_module1'.

Generating RTLIL representation for module `\multiple_modules'.
Successfully finished Verilog frontend.

run ``synth -top multiple_modules``

# 2 Hiercharcy vs flat design

**hierchary design **

yosys> ``show multiple_modules``

<img width="638" height="676" alt="image" src="https://github.com/user-attachments/assets/d0a986c7-66c1-491b-8aee-08ad6134ad9e" />

yosys> ``write_verilog -noattr multiple_modules_hier.v``

yosys> ``!gvim multiple_modules_hier.v``

<img width="1222" height="768" alt="image" src="https://github.com/user-attachments/assets/b1be65d2-91f1-4698-b1c8-020f7cc4ff57" />

we will be using stacked NMOS 

**flatten view**

<img width="1222" height="768" alt="image" src="https://github.com/user-attachments/assets/799111d6-940d-4685-b95d-59e7c78a218c" />

# Various flop coding styles and optimizarion

<img width="1222" height="768" alt="image" src="https://github.com/user-attachments/assets/f6625c98-bfd5-4edb-bb88-e9ab8f387123" />

<img width="1052" height="699" alt="image" src="https://github.com/user-attachments/assets/967ff3ee-c4f3-47b9-af46-8dac7f683854" />
