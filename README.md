![image](https://user-images.githubusercontent.com/77483516/167080105-2a7f5195-23eb-4444-a444-74f917136e4e.png)
**# sky130RTLDesignAndSynthesisWorkshop**
Day 1 - Introduction to Verilog RTL design and Synthesis 

**SKY130RTL D1SK1 L1 Introduction to iverilog design test bench** 

In the first lecture of the course, we learnt about the definitions of the RTL Design, Simulator and Test Bench. The simulator we are going to use in this workshop is iverilog. After the definitions of the terms mentioned above, we learnt the workings of Simulator and Test Bench. 

Simulator Working: 

Simulator looks for the changes in the input and for every change in the input, we observe changes in the output.  

Test Bench: 

Test Bench generates the stimulus for the design and observes the output. 
![TESTBENCH](https://user-images.githubusercontent.com/77483516/167550635-d5befd27-03e4-4af8-9bad-02c12f0ba7bb.PNG)
Iverilog based simulator flow: 

iverilog simulator takes the design and corresponding test bench of the design and generates the vcd( Value Change Dump format) file. The vcd file can be viewed using gtkwave waveform viewer. 
 ![iverilog simulation flow](https://user-images.githubusercontent.com/77483516/167551131-933b6e74-853b-4ee7-bc6f-bbfbad235220.PNG)
**SKY130RTL D1SK2 - Labs using iverilog and gtkwave**
SKY130RTL D1SK2 L1 Lab1 introduction to lab: 

In this session we git cloned the required modules from GitHub to VLSI folder
![gitclone lab](https://user-images.githubusercontent.com/77483516/167553727-3170eb1c-e844-4257-8573-2e39643ab9c2.PNG)

Inside the sky130 folder we have my lib which contains the standard cell library sky130_fd_sc_hd__tt_025C_1v80.lib 
![sky130lib](https://user-images.githubusercontent.com/77483516/167554418-06ff5742-a670-4027-9c7f-5af3a957f98b.PNG)

 
All the required Verilog files and Test benches are present in Verilog files folder. 
 ![verilog files folder](https://user-images.githubusercontent.com/77483516/167554592-3855aa1c-c4a1-4f9f-abc8-f740c611cf41.PNG)
**SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1:** 
 
In this lab, we learnt how to simulate Verilog files using iverilog. After executing the a.out file we get the dumpfile, which can be used using GTKWAVE waveform user. 
     ![iverilog simulation](https://user-images.githubusercontent.com/77483516/167556666-6d62bae8-e3fe-4f5b-bd7a-f4a5a9d8e8a8.PNG)
     ![gtkwave1](https://user-images.githubusercontent.com/77483516/167556716-918a5a36-b2ab-4a3c-b01b-30c5fc88cb2e.PNG)
**SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2: **

In this module, we have seen how to open verilog file using gvim command. 
![verilog files gvim](https://user-images.githubusercontent.com/77483516/167556833-11ab899a-ef68-4bd5-87a5-f8e57928584c.PNG)

         
 

**SKY130RTL D1SK3 - Introduction to Yosys and Logic synthesis** 

SKY130RTL D1SK3 L1 Introduction to yosys: 

 Synthesizer: 

It is a tool used for converting the RTL into netlist. In this workshop we are going to use yosys synthesizer. 

![synthesizer flow](https://user-images.githubusercontent.com/77483516/167556923-dfb821b9-891e-4635-a943-f84bb1dfffd8.PNG)
Yosys setup: 
![yosys setup](https://user-images.githubusercontent.com/77483516/167556991-4c4fbdb0-22bf-48ab-abfe-71c8d3817cbc.PNG)

Verification of the synthesis: 

To verify the generated netlist, we are going to use the same test bench and iverilog simulator. 
 ![verify synthesis](https://user-images.githubusercontent.com/77483516/167557047-969b689f-9fbd-4a22-90e6-f5c8732af634.PNG)
SKY130RTL D1SK3 L2 introduction to logic synthesis part1 

RTL Design: 
SYNTHESIS: 
 ![image](https://user-images.githubusercontent.com/77483516/167559189-67017034-2ea8-4fb8-8acf-d6e77b68d2e7.png)

LIBRARY:  

.lib is a collection of logic modules, which include basic logic gates and different flavours of same gates. 
 ![image](https://user-images.githubusercontent.com/77483516/167559302-3838c8ea-1984-4e2d-bf87-cc8b27e54c9f.png)
 

Why do we have different flavours of gates? 
 In order to have time for the logic to be executed properly and for setting up and holding of the current and previous inputs and outputs, we need different flavours of gates. 

For example, consider this situation: 
![image](https://user-images.githubusercontent.com/77483516/167560040-346e4276-03e0-4d45-a38f-30459d99d1f0.png)
In this situation the clock should accommodate the propagation delay, combinational logic delay and setup time of the B D flipflop. As the time is inversely proportional to frequency the smaller the time the faster the frequency. If we have faster cells, the time taken for the operation will be less. Less time implies maximum frequency. 


SKY130RTL D1SK3 L3 introduction to logic synthesis part2: 

 Why do we need slower cells? 

   In order to have proper hold time for the newly generated values in the design. If we go too fast, the logic may miss few values and we won’t get the intended results. 

FASTER CELLS VS SLOWER CELLS: 
![image](https://user-images.githubusercontent.com/77483516/167560168-2198d9bb-0678-4768-9698-b54487368001.png)


SYNTHESIS( ILLUSTRATION ): 
After syntactical check, the synthesizer will map different types of statements in the code to standard cells as shown below. 
![image](https://user-images.githubusercontent.com/77483516/167560303-733bb692-a01c-4a61-8207-092e616e666c.png)

**SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux Part1: **
yosys: 
yosys can be invoked by using the command yosys in the Verilog files module. 
![image](https://user-images.githubusercontent.com/77483516/167560618-9bb740c6-ddbe-4a74-8dcb-82f2cf68409c.png)

Reading the liberty: 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
![image](https://user-images.githubusercontent.com/77483516/167561081-282b3423-65b1-4813-8770-2cbc304a8b4c.png)

Command: read_verilog good_mux.v 
Reads the good_mux verilog file. 
![image](https://user-images.githubusercontent.com/77483516/167560893-7c032b32-32f1-498c-92b9-35bbd633a7eb.png)

Command: synth –top good_mux 
Specifies the modules to be synthesized and synthesizes the module. 
![image](https://user-images.githubusercontent.com/77483516/167561240-685808d9-6c97-447d-940d-60d2d53634b7.png)

Commnad: abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
This command generates netlist based on the standard cells available in the library.
![image](https://user-images.githubusercontent.com/77483516/167561344-48c533d7-8fc8-488f-8c01-438895c7e62e.png)

Command: show 
Displays the graphical version of the netlist in dot viewer. 
![image](https://user-images.githubusercontent.com/77483516/167561763-a0e2086b-d868-4ba7-bed7-cf346cb25d18.png)

**SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux Part2:** 

  In older version of yosys the above synthesis will generate two inverse gates and Nand for the function of and. But in the latest version directly a mux is used as standard cell. 
  ![image](https://user-images.githubusercontent.com/77483516/167561946-6bc578b2-b876-48b9-a452-b60fb75190d6.png)
  
**SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux Part3:** 
Command: write_verilog good_mux_netlist.v 
![image](https://user-images.githubusercontent.com/77483516/167562080-7ac91934-8caf-4c7d-aea4-7fd6733f1e98.png)

Command: !gvim good_mux_netlsit.v 
Reads the netlist. 
![image](https://user-images.githubusercontent.com/77483516/167562184-5afdf4e9-70a9-4ae8-88cd-34ec5dcc1de7.png)

Command: 1)write_verilog –noattr good_mux_netlist.v 

   2)!gvim goof_mux_netlsit.v 

To make and display the netlsit readable. 

 ![image](https://user-images.githubusercontent.com/77483516/167562555-fd8a94a4-2ca9-4ea7-8dee-81c75a84bcea.png)



 **DAY 2:**     

 **SKY130RTL D2SK1 L1 Lab4 Introduction to dot :**
 
 Command: gvim ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 
 ![image](https://user-images.githubusercontent.com/77483516/167562894-a1c07667-a12d-43a3-b33c-45be5171c994.png)
The various terms of the opened library’s name are tt-> typical process ,025C-> Temperature, 1v80->voltage. 


**SKY130RTL D2SK2 L1 Lab05 Hier synthesis flat synthesis part1:** 

**HEIRARCHIAL SYNTHESIS OF MULTIPLE_MODULES** 

Command: gvim multiple_modules.v 
![image](https://user-images.githubusercontent.com/77483516/167563088-e3c8dbd9-cfcf-4d13-920d-40fa44d1ec21.png)

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog multiple_modules.v 

![image](https://user-images.githubusercontent.com/77483516/167563223-dc04116a-447c-4f74-813c-a02b9370b9cf.png)

Command: synth –top multiple_modules 

![image](https://user-images.githubusercontent.com/77483516/167563301-b0e1db20-0732-46b0-b587-0d17a800d76a.png)

Commnad: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

![image](https://user-images.githubusercontent.com/77483516/167563363-8ee3686b-d117-40a6-87ba-f7f5d1b2a413.png)

Command: show multiple_modules 

HEIRARICHAL SYNTHESIS 
![image](https://user-images.githubusercontent.com/77483516/167563549-1a387c85-90b4-48c4-a9c6-eb693ec50f84.png)

Command: write_verilog –noattr multiple_modules_netlsit.v 

Command: !gvim multiple_modules_netlist.v 

![image](https://user-images.githubusercontent.com/77483516/167563660-7ba8d31f-c8a7-4db6-bf81-f349b238ce7c.png)

![image](https://user-images.githubusercontent.com/77483516/167563698-8e59e5b3-3f38-4149-befa-b2f83dd6a8d5.png)

![image](https://user-images.githubusercontent.com/77483516/167563745-8db0f7bc-e3cf-4c20-8a7d-ceac6b6d5798.png)

![image](https://user-images.githubusercontent.com/77483516/167563830-682cf134-0d81-4be5-89d2-966f71201084.png)

FLAT SYNTHESIS OF MULTIPLE_MOUDLES: 

Command: flatten 

Command: write_verilog –noattr multiple_modules_flat.v 

Command: !gvim multiple modules_flat.v 

![image](https://user-images.githubusercontent.com/77483516/167563981-86d2d2a8-7747-4139-aa96-1e059ab6963c.png)

![image](https://user-images.githubusercontent.com/77483516/167564247-6bdb866a-827c-4ab7-a35e-c32b5ccf0b59.png)

![image](https://user-images.githubusercontent.com/77483516/167564297-70926f60-0919-4324-93e4-e65455646aac.png)

![image](https://user-images.githubusercontent.com/77483516/167564409-83f5e979-5cd8-416f-9e51-941cf7c5ad7b.png)

Command: show multiple_modules

![image](https://user-images.githubusercontent.com/77483516/167564507-aa55b9e1-13af-43d5-93a2-4b022808b125.png)

**SYNTHESIS OF INDIVIDUAL MODULES:** 

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog multiple_modules.v 

![image](https://user-images.githubusercontent.com/77483516/167564754-1a28fc49-fc25-458e-b0d3-c10f4bf498da.png)


![image](https://user-images.githubusercontent.com/77483516/167564699-41a9bb4c-f408-499b-9b48-b951b383810f.png)


Command: synth –top sub_module1 

![image](https://user-images.githubusercontent.com/77483516/167564843-06186403-d9a5-4d57-a70f-ae0212f02bf9.png)

Command: abc –liberty ../my-lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show sub_module1 

Command: write –noattr sub_moudle_netlist.v 

Command: !gvim sub_module_netlist.v 

![image](https://user-images.githubusercontent.com/77483516/167564959-0b893189-e9e8-44e4-82a4-4efad345230d.png)

![image](https://user-images.githubusercontent.com/77483516/167564997-2dcaaf31-9922-4b0c-8ef9-3474009a8318.png)

![image](https://user-images.githubusercontent.com/77483516/167565033-7df79c64-0381-408e-bdfd-a357906a84aa.png)


**SKY130RTL D2SK3 L3 Lab flop synthesis simulations part1: **

DFF_ASYNCRES  IVERILOG SIMULATION 

Command: iverilog dff_asyncres.v tb_dff_asyncres.v 

Command: ./a.out 

Command: gtkwave tb_dff_asyncres.vcd 

![image](https://user-images.githubusercontent.com/77483516/167565321-5e63a5b2-9547-4a39-b04e-2323ff43de36.png)

![image](https://user-images.githubusercontent.com/77483516/167565156-d2038dbe-900a-4d1d-bed2-6f68f43bebdf.png)

OBSERVATIONS: If there is no reset, the state changes only with posedge of clock. 

Else, the output changes with reset. 

DFF_ASYNC_SET IVERILOG SIMULATION: 

Command: iverilog dff_async_set.v tb_dff_async_set.v 

Command: ./a.out 

Command: gtkwave tb_dff_async_set.vcd 

![image](https://user-images.githubusercontent.com/77483516/167565477-d5a518a9-3782-427b-b8ef-30ab92461cdc.png)

![image](https://user-images.githubusercontent.com/77483516/167565550-cd1bfe8a-976a-4649-a3e1-572c9f2e7791.png)

OBSERVATIONS: The q will be set without waiting for the clock. The q value will wait till the posedge of clock. 

DFF_SYNCRES IVERILOG SIMULATION: 

Command: iverilog dff_syncres.v tb_dff_syncres.v 

Command: ./a.out 

Command: gtkwave tb_dff_syncres.vcd 

OBSERVATIONS: The q will change only with the posedge of the clock even when the sync_reset is on. 

![image](https://user-images.githubusercontent.com/77483516/167565701-22875f3a-a76a-45d3-98bc-c9a6f72a84ca.png)

![image](https://user-images.githubusercontent.com/77483516/167565748-ea202f9b-65a7-4313-8460-d4669e9cce55.png)

**SKY130RTL D2SK3 L4 Lab flop synthesis simulations part2:**

DFF_ASYNCRES SYNTHESIS:

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib

Command: read_verilog dff_ayncres.v

Command: synth –top dff_asyncres

![image](https://user-images.githubusercontent.com/77483516/167565913-5d3d590a-ed3f-4f48-8c54-c6e20802d52c.png)

![image](https://user-images.githubusercontent.com/77483516/167565979-3f79892b-17e0-42f5-a051-14abe56d794d.png)

![image](https://user-images.githubusercontent.com/77483516/167566016-1ab40387-0948-4e1b-a6fc-1c52ddef3d93.png)

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
This command helps if the flop library and standard cell library are different. 

![image](https://user-images.githubusercontent.com/77483516/167566175-4cefe4dd-bf20-40a1-a2b9-846982b211a5.png)

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

![image](https://user-images.githubusercontent.com/77483516/167566306-fb8d3756-0f44-436b-8c75-7c176782f390.png)

Command: show

![image](https://user-images.githubusercontent.com/77483516/167566377-b1019374-b02e-4eb1-9611-a7de8d63f932.png)

OBSERVATIONS: The use of inverse gate in the synthesis indicates that the flop, in the library, has active low reset as input. 

DFF_ASYNC_SET SYNTHESIS: 

Command: read_verilog dff_async_set.v 

Command: synth –top dff_async_set 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167566687-b3156a84-4d57-405c-96e5-24b71fce33eb.png)

![image](https://user-images.githubusercontent.com/77483516/167566745-674b7b1b-0297-4d38-8793-962db3f81aa0.png)

![image](https://user-images.githubusercontent.com/77483516/167566865-e862becc-fae4-4b43-ac9b-63ec3410f80f.png)

![image](https://user-images.githubusercontent.com/77483516/167566829-f0d0fdee-22ab-462e-9a5a-dfea5370a80a.png)


DFF_SYNCRES SYNTHESIS: 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_syncres.v 

Command: synth –top dff_syncres 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167567006-1dcc1f1b-3192-4776-9375-b3b108b64143.png)

![image](https://user-images.githubusercontent.com/77483516/167567122-cec58b6d-2adf-45ab-9b5e-4246cafce555.png)

![image](https://user-images.githubusercontent.com/77483516/167567170-695825f7-3e30-4eb0-b46c-e980ec26b715.png)



**SKY130RTL D2SK3 L5 Interesting optimisations part1:** 

Command: gvim mult_*.v  -o 

This command helps in opening multiple files, with  mult as starting four letters. 

![image](https://user-images.githubusercontent.com/77483516/167567461-9b266cb7-d99d-4170-9568-257b97a48169.png)

![image](https://user-images.githubusercontent.com/77483516/167567514-ed0457aa-3761-4cfe-86bd-99ef266fb25d.png)

OBSERVATIONS: 

1) The first file mult_2.v gives 4-bit output after multiplication of 2 and 3-bit input. 

    The output is nothing but appending a ‘0’ at the right side of the input. 

2) The second file mult_8.v gives 6-bit output after multiplication of 9 and 3-bit input. 

     The output can be generated by appending the input with itself. 
     
 
 
 MULT_2 SYNTHESIS: 

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog mult_2.v 

Command: synth –top mul2 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167567634-97a43f27-5f0c-48d7-9314-5a99a4a1e2ec.png)

![image](https://user-images.githubusercontent.com/77483516/167567687-f1d017bd-8190-4b2c-bc25-abfdd502c99b.png)

OBSERVATIONS: 

1) The print statistics indicates that no cells are required. 

2) The netlist generation command shows “there is nothing to map”. 

![image](https://user-images.githubusercontent.com/77483516/167567804-6ae11546-8636-4bbf-b0bf-f3ff918e9a2b.png)

Command: show

![image](https://user-images.githubusercontent.com/77483516/167567869-2636d1e6-00f5-4f43-9ebf-ceef6a767c82.png)

OBSERVATION:  As  discussed before, the result is generated by appending the zero at right side. 

Command: write_verilog –noattr mult_2_netlist.v 

Command: !gvim mult_2_netlist.v 

![image](https://user-images.githubusercontent.com/77483516/167568035-22b4ab47-aaa6-4f03-9d04-0f98a07996f3.png)

![image](https://user-images.githubusercontent.com/77483516/167568080-f801eab7-ac2e-4541-b905-2c5a91198768.png)



MULT_8 SYNTHESIS: 

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog mult_8.v 

Command: synth –top mult8 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167568245-da2d2678-3a47-4c5b-94fb-82fb6ee3ef5f.png)

![image](https://user-images.githubusercontent.com/77483516/167568274-df4265c7-7bd0-471f-b5fe-c7c4fbce40d9.png)

OBSERVATIONS: There are no standard cells used in this synthesis. 

![image](https://user-images.githubusercontent.com/77483516/167568435-cfa7fe89-675b-43c6-b3a1-40e5406c90b0.png)
OBSERVATIONS: The abc command doesn’t want to be called without standard cells.

![image](https://user-images.githubusercontent.com/77483516/167568558-226430eb-726b-4557-b2c5-2c88fec5695f.png)

OBSERVATIONS: The show command indicates that the input is appended to itself and given as output. 

Command : write_verilog mult_8_netlsit.v 

Command: !gvim mult_8_netlsit.v 

![image](https://user-images.githubusercontent.com/77483516/167568645-124cfb7c-2e84-418c-bfd3-2d0244eaf990.png)

![image](https://user-images.githubusercontent.com/77483516/167568699-ba81dc9e-e0a7-4d60-9bfc-9aae96f3137c.png)

