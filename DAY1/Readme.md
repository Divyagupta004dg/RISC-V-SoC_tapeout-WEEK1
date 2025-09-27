**start commands**

sudo -i

cd /home

cd divya

cd VLSI

cd sky130RTLDesignAndSynthesisWorkshop

cd verlog_files

<img width="1222" height="768" alt="image" src="https://github.com/user-attachments/assets/254f38c5-f5b0-4a81-80eb-f04d6e114f4a" />

# Lab using i verilog and gtkwave 


<img width="1280" height="800" alt="Image" src="https://github.com/user-attachments/assets/e939f182-7bd1-4b3b-b51e-8850e240e3e6" />

<img width="1280" height="800" alt="Image" src="https://github.com/user-attachments/assets/bf934d49-e59c-4daa-94ce-217255e3ce8c" />

# Lab using Yosys and sky pdk 130

yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
1. Executing Liberty frontend: ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
Imported 418 cell types from liberty file.

yosys> read_verilog good_mux.v

2. Executing Verilog-2005 frontend: good_mux.v
Parsing Verilog input from `good_mux.v' to AST representation.
Generating RTLIL representation for module `\good_mux'.
**Successfully finished Verilog frontend.**

RUN
yosys > synth -top good_mux

yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib

yosys> show
 
<img width="638" height="676" alt="image" src="https://github.com/user-attachments/assets/f7f83af0-e8f3-4fbe-8b43-59f48338ddf6" />


**netlist**

yosys> write_verilog -noattr good_mux_netlist.v

yosys> !gvim good_mux_netlist.v

<img width="1008" height="683" alt="image" src="https://github.com/user-attachments/assets/d65d0548-037e-4a8b-aff0-6ff00f349c2e" />
