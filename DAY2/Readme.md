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


