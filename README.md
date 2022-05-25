![image](https://user-images.githubusercontent.com/77483516/167080105-2a7f5195-23eb-4444-a444-74f917136e4e.png)
# sky130RTLDesignAndSynthesisWorkshop
## Index
* [DAY 1 - Introduction to Verilog RTL design and Synthesis](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#day-1---introduction-to-verilog-rtl-design-and-synthesis)
   * [SKY130RTL D1SK1 L1 Introduction to iverilog design test bench](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#sky130rtl-d1sk1-l1-introduction-to-iverilog-design-test-bench)
   * [SKY130RTL D1SK2 L1 Lab1 introduction to lab:](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#sky130rtl-d1sk2-l1-lab1-introduction-to-lab)
   * [SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1:](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#sky130rtl-d1sk2-l2-lab2-introduction-iverilog-gtkwave-part1)
   * [SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2:](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#sky130rtl-d1sk2-l3-lab2-introduction-iverilog-gtkwave-part2)
   * [SKY130RTL D1SK3 L1 Introduction to yosys:](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#sky130rtl-d1sk3-l1-introduction-to-yosys)
   * [SKY130RTL D1SK3 L2 introduction to logic synthesis part1 :](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#sky130rtl-d1sk3-l2-introduction-to-logic-synthesis-part1-)
   * []()
* [DAY 2: - Timing libs, hierarchial vs flat coding styles and effictive flop coding styles](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#day-2---timing-libs-hierarchial-vs-flat-coding-styles-and-effictive-flop-coding-styles)
* [DAY 3: Combinational and Seqeuntial optimizations](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#day-3-combinational-and-seqeuntial-optimizations)
* [DAY 4: GLS, blocking vs non-blocking and Synhtesis and Simulation mismatch](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#day-4-gls-blocking-vs-non-blocking-and-synhtesis-and-simulation-mismatch)
* [DAY 5: If, case, for and for generate](https://github.com/MohanThota/sky130RTLDesignAndSynthesisWorkshop/blob/main/README.md#day-5-if-case-for-and-for-generate)



## DAY 1 - Introduction to Verilog RTL design and Synthesis

### SKY130RTL D1SK1 L1 Introduction to iverilog design test bench

In the first lecture of the course, we learnt about the definitions of the RTL Design, Simulator and Test Bench. The simulator we are going to use in this workshop is iverilog. After the definitions of the terms mentioned above, we learnt the workings of Simulator and Test Bench. 

**Simulator Working:** 

Simulator looks for the changes in the input and for every change in the input, we observe changes in the output.  

**Test Bench:** 

Test Bench generates the stimulus for the design and observes the output. 
![TESTBENCH](https://user-images.githubusercontent.com/77483516/167550635-d5befd27-03e4-4af8-9bad-02c12f0ba7bb.PNG)
Iverilog based simulator flow: 

iverilog simulator takes the design and corresponding test bench of the design and generates the vcd( Value Change Dump format) file. The vcd file can be viewed using gtkwave waveform viewer. 
 ![iverilog simulation flow](https://user-images.githubusercontent.com/77483516/167551131-933b6e74-853b-4ee7-bc6f-bbfbad235220.PNG)
 
### SKY130RTL D1SK2 - Labs using iverilog and gtkwave
### SKY130RTL D1SK2 L1 Lab1 introduction to lab: 

In this session we git cloned the required modules from GitHub to VLSI folder
![gitclone lab](https://user-images.githubusercontent.com/77483516/167553727-3170eb1c-e844-4257-8573-2e39643ab9c2.PNG)

Inside the sky130 folder we have my lib which contains the standard cell library sky130_fd_sc_hd__tt_025C_1v80.lib 
![sky130lib](https://user-images.githubusercontent.com/77483516/167554418-06ff5742-a670-4027-9c7f-5af3a957f98b.PNG)

 
All the required Verilog files and Test benches are present in Verilog files folder. 
 ![verilog files folder](https://user-images.githubusercontent.com/77483516/167554592-3855aa1c-c4a1-4f9f-abc8-f740c611cf41.PNG)
 
 
### SKY130RTL D1SK2 L2 Lab2 Introduction iverilog gtkwave part1:
 
In this lab, we learnt how to simulate Verilog files using iverilog. After executing the a.out file we get the dumpfile, which can be used using GTKWAVE waveform user. 
     ![iverilog simulation](https://user-images.githubusercontent.com/77483516/167556666-6d62bae8-e3fe-4f5b-bd7a-f4a5a9d8e8a8.PNG)
     ![gtkwave1](https://user-images.githubusercontent.com/77483516/167556716-918a5a36-b2ab-4a3c-b01b-30c5fc88cb2e.PNG)
### SKY130RTL D1SK2 L3 Lab2 Introduction iverilog gtkwave part2: 

In this module, we have seen how to open verilog file using gvim command. 
![verilog files gvim](https://user-images.githubusercontent.com/77483516/167556833-11ab899a-ef68-4bd5-87a5-f8e57928584c.PNG)

         
 

### SKY130RTL D1SK3 - Introduction to Yosys and Logic synthesis

### SKY130RTL D1SK3 L1 Introduction to yosys: 

 **Synthesizer:** 

It is a tool used for converting the RTL into netlist. In this workshop we are going to use yosys synthesizer. 

![synthesizer flow](https://user-images.githubusercontent.com/77483516/167556923-dfb821b9-891e-4635-a943-f84bb1dfffd8.PNG)
Yosys setup: 
![yosys setup](https://user-images.githubusercontent.com/77483516/167556991-4c4fbdb0-22bf-48ab-abfe-71c8d3817cbc.PNG)

**Verification of the synthesis:** 

To verify the generated netlist, we are going to use the same test bench and iverilog simulator. 
 ![verify synthesis](https://user-images.githubusercontent.com/77483516/167557047-969b689f-9fbd-4a22-90e6-f5c8732af634.PNG)
 
### SKY130RTL D1SK3 L2 introduction to logic synthesis part1 :

**RTL Design:**

**SYNTHESIS:**
 ![image](https://user-images.githubusercontent.com/77483516/167559189-67017034-2ea8-4fb8-8acf-d6e77b68d2e7.png)

**LIBRARY:**

.lib is a collection of logic modules, which include basic logic gates and different flavours of same gates. 
 ![image](https://user-images.githubusercontent.com/77483516/167559302-3838c8ea-1984-4e2d-bf87-cc8b27e54c9f.png)
 

Why do we have different flavours of gates? 
 In order to have time for the logic to be executed properly and for setting up and holding of the current and previous inputs and outputs, we need different flavours of gates. 

For example, consider this situation: 
![image](https://user-images.githubusercontent.com/77483516/167560040-346e4276-03e0-4d45-a38f-30459d99d1f0.png)
In this situation the clock should accommodate the propagation delay, combinational logic delay and setup time of the B D flipflop. As the time is inversely proportional to frequency the smaller the time the faster the frequency. If we have faster cells, the time taken for the operation will be less. Less time implies maximum frequency. 


### SKY130RTL D1SK3 L3 introduction to logic synthesis part2:

 Why do we need slower cells? 

   In order to have proper hold time for the newly generated values in the design. If we go too fast, the logic may miss few values and we won’t get the intended results. 

**FASTER CELLS VS SLOWER CELLS:**
![image](https://user-images.githubusercontent.com/77483516/167560168-2198d9bb-0678-4768-9698-b54487368001.png)


**SYNTHESIS( ILLUSTRATION ):**
After syntactical check, the synthesizer will map different types of statements in the code to standard cells as shown below. 
![image](https://user-images.githubusercontent.com/77483516/167560303-733bb692-a01c-4a61-8207-092e616e666c.png)

### SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux Part1: 
**yosys:** 
yosys can be invoked by using the command yosys in the Verilog files module. 
![image](https://user-images.githubusercontent.com/77483516/167560618-9bb740c6-ddbe-4a74-8dcb-82f2cf68409c.png)

**Reading the liberty:** 

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


### SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux Part2:

  In older version of yosys the above synthesis will generate two inverse gates and Nand for the function of and. But in the latest version directly a mux is used as standard cell. 
  ![image](https://user-images.githubusercontent.com/77483516/167561946-6bc578b2-b876-48b9-a452-b60fb75190d6.png)


### SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux Part3:
Command: write_verilog good_mux_netlist.v 
![image](https://user-images.githubusercontent.com/77483516/167562080-7ac91934-8caf-4c7d-aea4-7fd6733f1e98.png)

Command: !gvim good_mux_netlsit.v 
Reads the netlist. 
![image](https://user-images.githubusercontent.com/77483516/167562184-5afdf4e9-70a9-4ae8-88cd-34ec5dcc1de7.png)

Command: 1)write_verilog –noattr good_mux_netlist.v 

   2)!gvim goof_mux_netlsit.v 

To make and display the netlsit readable. 

 ![image](https://user-images.githubusercontent.com/77483516/167562555-fd8a94a4-2ca9-4ea7-8dee-81c75a84bcea.png)



## DAY 2: - Timing libs, hierarchial vs flat coding styles and effictive flop coding styles  

### SKY130RTL D2SK1 L1 Lab4 Introduction to dot :
 
 Command: gvim ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 
 ![image](https://user-images.githubusercontent.com/77483516/167562894-a1c07667-a12d-43a3-b33c-45be5171c994.png)
The various terms of the opened library’s name are tt-> typical process ,025C-> Temperature, 1v80->voltage. 

### SKY130RTL D2SK2 L1 Lab05 Hier synthesis flat synthesis part1: 

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

**HEIRARICHAL SYNTHESIS**
![image](https://user-images.githubusercontent.com/77483516/167563549-1a387c85-90b4-48c4-a9c6-eb693ec50f84.png)

Command: write_verilog –noattr multiple_modules_netlsit.v 

Command: !gvim multiple_modules_netlist.v 

![image](https://user-images.githubusercontent.com/77483516/167563660-7ba8d31f-c8a7-4db6-bf81-f349b238ce7c.png)

![image](https://user-images.githubusercontent.com/77483516/167563698-8e59e5b3-3f38-4149-befa-b2f83dd6a8d5.png)

![image](https://user-images.githubusercontent.com/77483516/167563745-8db0f7bc-e3cf-4c20-8a7d-ceac6b6d5798.png)

![image](https://user-images.githubusercontent.com/77483516/167563830-682cf134-0d81-4be5-89d2-966f71201084.png)

**FLAT SYNTHESIS OF MULTIPLE_MOUDLES:**

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


### SKY130RTL D2SK3 L3 Lab flop synthesis simulations part1: 

**DFF_ASYNCRES  IVERILOG SIMULATION**

Command: iverilog dff_asyncres.v tb_dff_asyncres.v 

Command: ./a.out 

Command: gtkwave tb_dff_asyncres.vcd 

![image](https://user-images.githubusercontent.com/77483516/167565321-5e63a5b2-9547-4a39-b04e-2323ff43de36.png)

![image](https://user-images.githubusercontent.com/77483516/167565156-d2038dbe-900a-4d1d-bed2-6f68f43bebdf.png)

OBSERVATIONS: If there is no reset, the state changes only with posedge of clock. 

Else, the output changes with reset. 

**DFF_ASYNC_SET IVERILOG SIMULATION:**

Command: iverilog dff_async_set.v tb_dff_async_set.v 

Command: ./a.out 

Command: gtkwave tb_dff_async_set.vcd 

![image](https://user-images.githubusercontent.com/77483516/167565477-d5a518a9-3782-427b-b8ef-30ab92461cdc.png)

![image](https://user-images.githubusercontent.com/77483516/167565550-cd1bfe8a-976a-4649-a3e1-572c9f2e7791.png)

OBSERVATIONS: The q will be set without waiting for the clock. The q value will wait till the posedge of clock. 

**DFF_SYNCRES IVERILOG SIMULATION:**

Command: iverilog dff_syncres.v tb_dff_syncres.v 

Command: ./a.out 

Command: gtkwave tb_dff_syncres.vcd 

OBSERVATIONS: The q will change only with the posedge of the clock even when the sync_reset is on. 

![image](https://user-images.githubusercontent.com/77483516/167565701-22875f3a-a76a-45d3-98bc-c9a6f72a84ca.png)

![image](https://user-images.githubusercontent.com/77483516/167565748-ea202f9b-65a7-4313-8460-d4669e9cce55.png)



### SKY130RTL D2SK3 L4 Lab flop synthesis simulations part2:

**DFF_ASYNCRES SYNTHESIS:**

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

**DFF_ASYNC_SET SYNTHESIS:**

Command: read_verilog dff_async_set.v 

Command: synth –top dff_async_set 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167566687-b3156a84-4d57-405c-96e5-24b71fce33eb.png)

![image](https://user-images.githubusercontent.com/77483516/167566745-674b7b1b-0297-4d38-8793-962db3f81aa0.png)

![image](https://user-images.githubusercontent.com/77483516/167566865-e862becc-fae4-4b43-ac9b-63ec3410f80f.png)

![image](https://user-images.githubusercontent.com/77483516/167566829-f0d0fdee-22ab-462e-9a5a-dfea5370a80a.png)


**DFF_SYNCRES SYNTHESIS:**

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_syncres.v 

Command: synth –top dff_syncres 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167567006-1dcc1f1b-3192-4776-9375-b3b108b64143.png)

![image](https://user-images.githubusercontent.com/77483516/167567122-cec58b6d-2adf-45ab-9b5e-4246cafce555.png)

![image](https://user-images.githubusercontent.com/77483516/167567170-695825f7-3e30-4eb0-b46c-e980ec26b715.png)



### SKY130RTL D2SK3 L5 Interesting optimisations part1:

Command: gvim mult_*.v  -o 

This command helps in opening multiple files, with  mult as starting four letters. 

![image](https://user-images.githubusercontent.com/77483516/167567461-9b266cb7-d99d-4170-9568-257b97a48169.png)

![image](https://user-images.githubusercontent.com/77483516/167567514-ed0457aa-3761-4cfe-86bd-99ef266fb25d.png)

OBSERVATIONS: 

1) The first file mult_2.v gives 4-bit output after multiplication of 2 and 3-bit input. 

    The output is nothing but appending a ‘0’ at the right side of the input. 

2) The second file mult_8.v gives 6-bit output after multiplication of 9 and 3-bit input. 

     The output can be generated by appending the input with itself. 
     
 
**MULT_2 SYNTHESIS:**

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



**MULT_8 SYNTHESIS:**

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



## DAY 3: Combinational and Seqeuntial optimizations

### SKY130RTL D3SK2 L1 Lab06 Combinational Logic Optimisations part1:

**OPT_CHECK OPTIMISZATION AND SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog opt_check.v 

Command: synth –top opt_check 

![image](https://user-images.githubusercontent.com/77483516/167589189-4909e682-71db-445a-b62d-93f34788f22e.png)

![image](https://user-images.githubusercontent.com/77483516/167589257-53f56b65-6659-43ca-b31b-800063099d40.png)

Command: opt_clean –purge 

This command helps in identifying and removing the unused cells in the design. 

![image](https://user-images.githubusercontent.com/77483516/167589367-aff984f3-c966-48dc-b9b0-87ce22295243.png)

Command: abc –liberty  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167589474-db49c812-8584-487a-88c4-74249dd3d1a3.png)

![image](https://user-images.githubusercontent.com/77483516/167589565-f87318a2-fcb4-42b4-ba8b-883bf06c6fcf.png)

OBSERVATIONS:  

1) When one of the inputs of a multiplexer is zero, the design can be optimised as an AND gate. 



**OPT_CHECK2 OPTIMISZATION AND SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog opt_check2.v 

Command: synth –top opt_check2

![image](https://user-images.githubusercontent.com/77483516/167589723-b0c11be0-fa99-40c3-ad83-5b632d9083ac.png)

![image](https://user-images.githubusercontent.com/77483516/167589811-bded376a-174e-45eb-8428-119ff3f43774.png)

Command: opt_clean –purge 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167589916-966c2b14-46e2-4726-bb39-3905ec4750ca.png)

![image](https://user-images.githubusercontent.com/77483516/167589971-82cd28d7-14f7-4ae5-9ef1-7dc04b184e40.png)

OBSERVATIONS: 

1) When one of the inputs of multiplexer is one, the design can be optimised as a OR gate. 

2) Instead of generating OR gate from Nand gates, the updated standard cell library had an OR gate.  


### SKY130RTL D3SK2 L2 Lab06 Combinational Logic Optimisations part2: 

**OPT_CHECK3 OPTIMIZATION AND  SYNTHESIS :**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog opt_check3.v 

Command: synth –top opt_check3 

![image](https://user-images.githubusercontent.com/77483516/167590243-3e5ab140-74ca-4184-bc1f-091c64a0db77.png)

Command: opt_clean –purge 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show

![image](https://user-images.githubusercontent.com/77483516/167590378-d54c69ae-bba1-4e65-b1b0-9527128f8b33.png)

![image](https://user-images.githubusercontent.com/77483516/167590432-ee5a88dd-2c51-4bc7-8d1b-3c561baaeb9f.png)

![image](https://user-images.githubusercontent.com/77483516/167590488-1e2bf99b-2937-401b-8f61-6d3cc620a468.png)

![image](https://user-images.githubusercontent.com/77483516/167590557-c8d513c9-f1c3-43bf-938c-a1d0cbe3b813.png)
 
OBSERVATIONS: The two multiplexers in the opt_check3.v are optimised as single 3 input AND gate. Because, one the inputs of the two multiplexers are zero they are optimised to AND gates as in opt_check.v. 

![image](https://user-images.githubusercontent.com/77483516/167590677-a41cd65c-14b1-4f11-8619-0270b9ddb470.png)

**OPT_CHECK4.V OPTIMISATION AND SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog opt_check4.v 

Command: synth –top opt_check4 

Command: opt_clean –purge 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167590819-34d0fffb-7062-47c2-87f4-cd89a5e43e9b.png)

![image](https://user-images.githubusercontent.com/77483516/167590905-37fe099c-6656-4624-9d29-572b6c0de2ba.png)

![image](https://user-images.githubusercontent.com/77483516/167590984-c263c857-0684-4104-8364-b25e3abc714e.png)

![image](https://user-images.githubusercontent.com/77483516/167591026-0bcb9704-50a2-4318-9ee7-52f2e1052c81.png)

OBSERVATIONS: The opt_check4.v design is simplified as an XNOR gate.

**MULTIPLE_MODULE_OPT.V OPTIMIZATION AND SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog multiple_module_opt.v 

Command: synth –top multiple_module_opt 

Command: flatten 

Command: opt_clean –purge 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167591179-ec56f934-4f99-48a9-aefd-67dba85038d3.png)

![image](https://user-images.githubusercontent.com/77483516/167591232-ad6c186b-cdb1-4ec7-8de7-7090b91644c2.png)

![image](https://user-images.githubusercontent.com/77483516/167591277-34f103d5-557f-4959-aa3f-0c6aafc1d5b7.png)

![image](https://user-images.githubusercontent.com/77483516/167591378-df6c65a8-f00a-4de3-a916-0578f21f27b6.png)

![image](https://user-images.githubusercontent.com/77483516/167591488-09cd35ff-2727-432f-aa24-052259e62195.png)

![image](https://user-images.githubusercontent.com/77483516/167591733-50a72397-f803-425c-9e12-838e9cb6ea69.png)

Command: write_verilog –noattr multiple_module_opt_netlist.v 

Command: !gvim multiple_module_opt_netlist.v 

![image](https://user-images.githubusercontent.com/77483516/167591836-8b684741-e844-4440-b6a2-4fd2d539069a.png)

![image](https://user-images.githubusercontent.com/77483516/167591880-aae6e9d1-3132-437d-85ab-cfa9edb2b147.png)

![image](https://user-images.githubusercontent.com/77483516/167591935-77cca596-9ea5-4cf9-b2b3-0d6bea7d85f9.png)

OBSERVATIONS:  

1)The multiple_module_opt.v  is optimised to a two input AND gate and two input OR gate using boolean logic optimization. 

2)The U1 module is simplified to a. 

**MULTIPLE_MODULE_OPT2.V OPTIMIZATION AND SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog multiple_module_opt.v 

Command: synth –top multiple_module_opt2 

Command: flatten 

Command: opt_clean –purge 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

Command: write_verilog –noattr multiple_module_opt2_netlist.v 

Command: !gvim multiple_module_module_opt2_netlist.v 

![image](https://user-images.githubusercontent.com/77483516/167592133-630740f1-92dc-4dac-ae7c-27f13b2e20f6.png)

![image](https://user-images.githubusercontent.com/77483516/167592200-3c8e5f99-8e1c-4d39-beab-d77590cdea1a.png)

![image](https://user-images.githubusercontent.com/77483516/167592241-61a2fab3-a7b3-488a-b31b-1409c27c13d3.png)

![image](https://user-images.githubusercontent.com/77483516/167592355-ecd7524b-365f-4394-a83a-a91f849ccc41.png)

![image](https://user-images.githubusercontent.com/77483516/167592502-54b84763-2fb0-4862-b554-25beaf53553f.png)

![image](https://user-images.githubusercontent.com/77483516/167592545-c5f42dce-3828-4464-82a3-4a61146a1d56.png)

![image](https://user-images.githubusercontent.com/77483516/167592602-4c1098cd-3653-4c78-8358-2fa2ea9e0045.png)

![image](https://user-images.githubusercontent.com/77483516/167592643-fe32c9b9-0597-49da-8224-162dde6662bc.png)

![image](https://user-images.githubusercontent.com/77483516/167592749-3102cda7-c367-49d8-b355-1d543a1b3eb8.png)

OBSERVATIONS: 

1) The synthesizer optimised the multiple_module_opt2.v using constant propagation optimization. 

2) The synthesizer optimized the output to zero. 

 

### SKY130RTL D3SK3 L1 Lab07 Sequential Logic Optimisations part1:

**DFF_CONST1 SIMULATION:**

Command: iverilog dff_const1.v tb_dff_const1.v 

Command: ./a.out 

Command: gtkwave tb_dff_const1.vcd 

![image](https://user-images.githubusercontent.com/77483516/167592937-73e58ab0-2bf8-45ea-a6b9-9d7edf7881bf.png)

![image](https://user-images.githubusercontent.com/77483516/167593002-93b79d1e-9760-46ad-9ece-0a83958a3200.png)

OBSERVATIONS: The q doesn’t change value when reset is low. Q will change value only with the posedge of the clock. 

** DFF_CONST2 SIMULATION: **

Command: iverilog dff_const1.v tb_dff_const2.v 

Command: ./a.out 

Command: gtkwave tb_dff_const2.vcd 

![image](https://user-images.githubusercontent.com/77483516/167593336-a8a477d5-48ad-4d19-972e-77e84389a5cd.png)

![image](https://user-images.githubusercontent.com/77483516/167593386-0208179d-1bb3-4f21-ab76-8a8a6e40b507.png)

OBSERVATIONS: The q value is always one.

 

**DFF_CONST1.V SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_const1.v 

Command: synth –top dff_const1 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167593538-e48482fa-da40-4a89-b2bd-7e8eb51561fc.png)

![image](https://user-images.githubusercontent.com/77483516/167593599-d573fabf-0f78-4a11-895d-bb9816d9d3f7.png)

![image](https://user-images.githubusercontent.com/77483516/167593696-4f408020-bf6e-41a8-bd66-3a790bd773c4.png)

![image](https://user-images.githubusercontent.com/77483516/167593750-3338c722-7e80-4814-a2af-b62a410156e9.png)

![image](https://user-images.githubusercontent.com/77483516/167593790-efe8de04-5d2c-4c2a-b322-88a65c1e0872.png)

OBSERVATIONS: As stated before, the D_flip_flop in the netlist is active_low. So, the synthesizer used an inverter to change rest from active_high to active_low. 



### SKY130RTL D3SK3 L2 Lab07 Sequential Logic Optimisations part2:

**DFF_CONST2.V SYNTHESIS**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_const2.v 

Command: synth –top dff_const2 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167594642-0f7f96b8-fa4b-41d2-b167-b72ef973b304.png)

![image](https://user-images.githubusercontent.com/77483516/167594704-9cb2656d-aaf7-41f0-b140-f8a5a2108bb7.png)

![image](https://user-images.githubusercontent.com/77483516/167594762-ae5ae139-bc1a-4464-b7ae-c089c2db7d9a.png)

OBSERVATION: ABC command ‘s result is indicating that there is no standard cell. 

![image](https://user-images.githubusercontent.com/77483516/167594888-dabed410-df63-4fe3-9d00-2a7188797f91.png)



### SKY130RTL D3SK3 L2 Lab07 Sequential Logic Optimisations part3:

**DFF_CONST3.V SIMULATION, OPTIMIZATION AND SYNTHESIS:**

Command: iverilog dff_const3.v tb_dff_const3.v 

Command: ./.aout 

Command:  gtkwave tb_dff_const3.vcd 

![image](https://user-images.githubusercontent.com/77483516/167595066-71ee201e-ff1b-49bb-b870-1f37956f4305.png)

![image](https://user-images.githubusercontent.com/77483516/167595156-fa5eb570-d1bb-4d8f-895f-1ffde366b140.png)

OBSERVATIONS: 
q=1 at every instant except at the moment in the above figure. So, the flipflop can’t be optimised. 

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_const3.v 

Command: synth –top dff_const3 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167595347-294de5d1-9ab9-4e13-a353-bad57a2a16bf.png)

![image](https://user-images.githubusercontent.com/77483516/167595412-0c10d7d7-7e28-4073-8a1c-20a09d7c7106.png)

![image](https://user-images.githubusercontent.com/77483516/167595510-a97134d5-1804-412b-b396-1a915c55c12e.png)

![image](https://user-images.githubusercontent.com/77483516/167595572-f843411b-181c-435a-8c56-9a6f60bef99e.png)

OBSERVATIONS: 
Because q cannot be optimised, the circuit remains unoptimized. 


**DFF_CONST4.V SIMULATION, OPTIMIZATION AND SYNTHESIS:**

Command: iverilog dff_const4.v tb_dff_const4.v 

Command: ./.aout 

Command:  gtkwave tb_dff_const4.vcd 

![image](https://user-images.githubusercontent.com/77483516/167595766-298a6e80-8efa-4412-98ad-b3d19bf24c6c.png)

![image](https://user-images.githubusercontent.com/77483516/167595814-cefdf1c2-1c64-4611-bd2a-934f29d6baf1.png)

OBSERVATIONS: The q is always one. 

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_const4.v 

Command: synth –top dff_const4 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167595946-3e3a3a30-fa1a-4307-887f-15d7b41cf396.png)

![image](https://user-images.githubusercontent.com/77483516/167596003-d549be2b-1d56-4865-af44-d91f41cd8857.png)

![image](https://user-images.githubusercontent.com/77483516/167596051-1e775eca-fbd4-4468-b12e-c0f49c8b2e58.png)

![image](https://user-images.githubusercontent.com/77483516/167596096-c7a30537-8074-4ade-be53-a4efdc7f3ba0.png)

OBSERVATIONS: As the q is always one in this synthesis, there is no standard cell in the netlist. 


**DFF_CONST5.V SIMULATION, OPTIMIZATION AND SYNTHESIS:**

Command: iverilog dff_const5.v tb_dff_const5.v 

Command: ./.aout 

Command:  gtkwave tb_dff_const5.vcd 

![image](https://user-images.githubusercontent.com/77483516/167596352-22a48a45-bfea-44be-95d2-9f5063ae98dc.png)

![image](https://user-images.githubusercontent.com/77483516/167596396-d76a0c73-08ac-4a93-98b6-13e03e171030.png)

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog dff_const5.v 

Command: synth –top dff_const5 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167596600-25176b1c-2fd6-44fb-bb05-c6497fc730cc.png)

![image](https://user-images.githubusercontent.com/77483516/167596647-84cec405-0267-47d5-93ab-b50075a5cd5f.png)

![image](https://user-images.githubusercontent.com/77483516/167596700-eb7a3c98-5bf1-4fc8-8cbd-87aad8ba9b0f.png)

![image](https://user-images.githubusercontent.com/77483516/167596737-6389d7ba-a998-4c25-850f-a55f221939f3.png)

OBSERVATIONS: There is no optimization in this file synthesis. 


### SKY130RTL D3SK4 L1 Seq optimisation unused outputs part1:*

**COUNTER_OPT.V SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog counter_opt.v 

Command: synth –top counter_opt 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167596924-34a52c7b-e69a-4a7b-9e90-e1d08953191a.png)

![image](https://user-images.githubusercontent.com/77483516/167596980-f82ba880-b378-4da1-8bd2-73b7ae957696.png)

![image](https://user-images.githubusercontent.com/77483516/167597108-28b83f0c-581b-4ef5-b465-a3fb54135985.png)

![image](https://user-images.githubusercontent.com/77483516/167597147-8b654298-0708-4b23-8c69-ec377fd55651.png)


OBSERVATIONS: 
The synthesis shows that q is connected to D through an inverter. So, for every posedge, they q will change. The synthesizer will ignore the counting of the remaining two bits.


### SKY130RTL D3SK4 L2 Seq optimisation unused outputs part2:

**COUNTER_OPT2.V SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog counter_opt2.v 

Command: synth –top counter_opt2

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167597397-fcf50cee-40b3-46bc-910a-9c4c05f456d1.png)

![image](https://user-images.githubusercontent.com/77483516/167597438-2287dbb0-8c85-4e6d-9744-fb3b33d20660.png)

![image](https://user-images.githubusercontent.com/77483516/167597474-0e210968-16ad-43a3-8953-49be37ec9967.png)

![image](https://user-images.githubusercontent.com/77483516/167597528-f598a59b-0c64-4297-bcff-859a8f5bcbaf.png)

OBSERVATIONS: There is no optimization in this synthesis. 


**COUNTER_OPT3.V SYNTHESIS FOR ASSESMENT:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog counter_opt3.v 

Command: synth –top counter_opt 

Command: dfflibmap –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167597745-4c2a1a67-08e1-4d20-ac9d-97d1289a4045.png)

![image](https://user-images.githubusercontent.com/77483516/167597826-b489bb67-4adf-421f-88a3-719117aa4667.png)

![image](https://user-images.githubusercontent.com/77483516/167597897-ca091420-c08a-4fe6-abc6-18bf8dcfb4f0.png)

![image](https://user-images.githubusercontent.com/77483516/167597953-3279ea05-25f4-4511-896d-8133e5d593e2.png)





## DAY 4: GLS, blocking vs non-blocking and Synhtesis and Simulation mismatch

### SKY130RTL D4SK2 L1 Lab GLS Synth Sim Mismatch part1:

**TERENARY_OPERATOR GLS :**

Command: iverilog ternary_operator_mux.v tb_ternary_operator_mux.v 

Command: ./a.out 

Command: gtkwave tb_ternary_operator_mux.vcd 

![image](https://user-images.githubusercontent.com/77483516/167598517-1256ef57-379c-47da-b71a-cdfcd5f40eb4.png)

![image](https://user-images.githubusercontent.com/77483516/167598604-a1f5a630-f35f-42f0-9aec-beccf25a8daa.png)

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog ternary_operator_mux.v 

Command: synth –top ternary_operator_mux 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

Command: write_verilog –noattr ternary_operator_mux_net.v 

![image](https://user-images.githubusercontent.com/77483516/167598744-ae87940a-2c21-4816-8e72-4f9e9095f4a6.png)

![image](https://user-images.githubusercontent.com/77483516/167598782-f6984d48-caca-4a7d-b9fc-c6de85ff2f2c.png)

![image](https://user-images.githubusercontent.com/77483516/167598833-02b390d0-639d-4ece-9fa5-f78850bbb2ce.png)

![image](https://user-images.githubusercontent.com/77483516/167598875-f3d9d056-27a7-4a8f-8753-700a65c5e89e.png)

Command: iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v ternary_operator_mux_net.v tb_ternary_operator_mux.v 

Command: ./a.out 

Command: gtkwave tb_ternary_operator_mux.v 

![image](https://user-images.githubusercontent.com/77483516/167598998-38909cec-ba89-4749-9f28-f7132c28b6c2.png)

![image](https://user-images.githubusercontent.com/77483516/167599041-bf20a9a6-a6be-4d29-a2d7-78460267f5b0.png)


### SKY130RTL D4SK2 L2 Lab GLS Synth Sim Mismatch part2:

**BAD_MUX.V SIMULATION:**

Command: iverilog bad_mux.v tb_bad_mux.v 

Command: ./a.out 

Command: gtkwave tb_bad_mux.vcd

![image](https://user-images.githubusercontent.com/77483516/167599359-40482076-a2b4-427f-b0a2-da48108fac02.png)

![image](https://user-images.githubusercontent.com/77483516/167599425-2106ff93-133e-49e7-a3ec-9dde04f1957c.png)

OBSERVATIONS: Clearly, the waveform shows that the verilog file is not working as a multiplexer. 

**BAD_MUX.V Synthesis:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog bad_mux.v 

Command: synth –top bad_mux 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: write_verilog –noattr bad_mux_net.v

![image](https://user-images.githubusercontent.com/77483516/167599643-44ea4bee-f2fb-4380-8226-7e5aae7f322a.png)

![image](https://user-images.githubusercontent.com/77483516/167599737-e33f73c1-4ea2-4852-b877-4df6fb14dbd5.png)

Command: iverilog ../my_lib/verilog_module/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v bad_mux.net.v tb_bad_mux.v 

Command: ./a.out 

Command: gtkwave tb_bad_mux.vcd

![image](https://user-images.githubusercontent.com/77483516/167599861-3d0dfacb-7d6c-4b0a-8981-5be21604be54.png)

![image](https://user-images.githubusercontent.com/77483516/167599913-26148b6b-b1f7-4eae-97a5-9ff435b80819.png)

OBSERVATION: THE ABOVE WAVEFORM CLEARLY INDICATES SIMULATION – SYNTHESIS MISMATCH CAUSED BY MISSING SENSITIVITY LIST. 



### SKY130RTL D4SK3 L1 Lab Synth sim mismatch blocking statement part1:

**BLOCKING CAVEAT.V SIMULATIOn** 

Command: iverilog blocking_caveat.v tb_blocking_caveat.v 

Command: ./a.out 

Command: gtkwave tb_blocking_caveat.vcd 

![image](https://user-images.githubusercontent.com/77483516/167600093-71e1242f-d385-4dfe-889f-cbfacefb0454.png)

![image](https://user-images.githubusercontent.com/77483516/167600133-1db419f6-88df-401d-8c59-9e77922118a1.png)

OBSERVATIONS: Clearly, the output of the aORb is taking previous values to generate d.  




### SKY130RTL D4SK3 L1 Lab Synth sim mismatch blocking statement part2: 

**BLOCKING CAVEAT.V SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog blocking_caveat.v 

Command: synth –top blocking_caveat 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: write_verilog –noattr bad_mux_net.v 

![image](https://user-images.githubusercontent.com/77483516/167600289-7e33abcb-826d-40d5-912c-bc69add5f832.png)

![image](https://user-images.githubusercontent.com/77483516/167600357-16f69b43-f378-4078-8125-c7beb9e14c66.png)

![image](https://user-images.githubusercontent.com/77483516/167602549-eeff4cda-9bab-4099-bd4e-f19bb83219fb.png)

Command: iverilog ../my_lib/verilog_module/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v blocking_caveat_net.v tb_blocking_caveat.v 

Command: ./a.out 

Command: gtkwave tb_blocking_caveat.vcd 

![image](https://user-images.githubusercontent.com/77483516/167602687-bc7c78c9-eb4c-472d-b7fb-f1cb9cd18b95.png)

![image](https://user-images.githubusercontent.com/77483516/167602734-bc9b74eb-c5e9-4f6a-9f55-41fa2e939adc.png)

OBSERVATION: Clearly, the waveform after synthesis indicates the simulation-synthesis mismatch caused by blocking-caveat. 



## DAY 5: If, case, for and for generate

### SKY130RTL D5SK2 L1 Lab Incomplete IF part1:

**INCOMPLETE_IF SIMULATION:** 

Command: iverilog incomp_if.v tb_incomp_if.v 

Command: ./a.out 

Command: gtkwave tb_incomp_if.vcd 

![image](https://user-images.githubusercontent.com/77483516/167603006-6ec4b420-7f9e-429a-963b-f740215425be.png)

![image](https://user-images.githubusercontent.com/77483516/167603084-d4d1f67c-e61d-41b3-a8b9-d00354e337b4.png)

![image](https://user-images.githubusercontent.com/77483516/167603128-a3b17bd3-cc6e-40d3-bb6a-d303bf365409.png)

OBSERVATIONS:  

1)Whenever i0 is high, the y is following i1. 

2)Whenever i0 is low, the output y is latching to its previous value as shown in above two images. 

3)This behaviour is due to inferred latch.   

 
**INCOMP_IF SYNTHESIS**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog incomp_if.v 

Command: synth –top incomp_if 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167603294-87caa2f6-717c-4fcf-962c-1a84005d0a9b.png)

![image](https://user-images.githubusercontent.com/77483516/167603349-440bd917-b7bb-4bdc-8c2a-6be85757be81.png)

![image](https://user-images.githubusercontent.com/77483516/167603429-912724bb-150b-4c1f-9c55-53c49d431a34.png)

![image](https://user-images.githubusercontent.com/77483516/167603488-442facbf-36ae-44d0-87b8-deb0b603fa37.png)

OBSERVATIONS: Both the simulation and synthesis are inferring a latch, when we designed a multiplexer.


 

### SKY130RTL D5SK2 L2 Lab Incomplete IF part2: 

**INCOMPLETE_IF SIMULATION2:**

Command: iverilog incomp_if2.v tb_incomp_if2.v 

Command: ./a.out 

Command: gtkwave tb_incomp_if2.vcd 

![image](https://user-images.githubusercontent.com/77483516/167603669-409786c1-9e5c-4800-9182-50340e81e3c5.png)

![image](https://user-images.githubusercontent.com/77483516/167603735-cf2a5506-aba4-4c45-82e2-4bc2854cb61e.png)

![image](https://user-images.githubusercontent.com/77483516/167603900-427bafff-486d-4c01-a06a-545a145b1071.png)

OBSERVATIONS:  

1) When i0 is high, the output y is following i1. 

2)When i2 is high and i1 is low, the output is following i2. 

3)When both i2 and i0 are low, the output is latching to y. 



**INCOMP_IF2 SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog incomp_if2.v 

Command: synth –top incomp_if2 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167604243-67e1958f-57ff-43aa-8e58-b672abec2ecd.png)

![image](https://user-images.githubusercontent.com/77483516/167604294-8ead8738-23af-476c-a760-d24082d5693f.png)

![image](https://user-images.githubusercontent.com/77483516/167604370-2993b630-9c57-4928-8883-1a2f3daf7d7d.png)

![image](https://user-images.githubusercontent.com/77483516/167604410-0d0828a9-879e-4078-bcc6-7770deee8d28.png)

OBSERVATIONS:  

1)Clearly, we can see the inferred latch on dot viewer. 

2) The D_latch has active high enable. So, when i0 and i1 are low, the output of the nor gate becomes high. Then the latch becomes active.  


### SKY130RTL D5SK3 L1 Lab incomplete overlapping Case part1:

**INCOMP_CASE SIMUALTION:**

Command: iverilog incomp_case.v tb_incomp_case.v 

Command: ./a.out 

Command: gtkwave tb_incomp_case.vcd 

![image](https://user-images.githubusercontent.com/77483516/167604608-bac9bb9c-a731-451f-994d-eb09bf8bdb0c.png)

![image](https://user-images.githubusercontent.com/77483516/167604688-4818512b-eadb-41db-8021-148eee2c31c3.png)

 

OBSERVATIONS:  

The output y is i0 when select is 00. When the select is 01, the output y is i1. 

When the select bit [1] is high, the circuit latches to y value. In this y is zero. 


**INCOMP_CASE SYNTHESIS:** 

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog incomp_case.v 

Command: synth –top incomp_case 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167604870-9e705cdf-1898-456b-ae87-edd5f252392c.png)

![image](https://user-images.githubusercontent.com/77483516/167604919-338b933d-3585-4e25-ba89-e76e8ec1c5aa.png)

![image](https://user-images.githubusercontent.com/77483516/167605056-013bf2e1-45fe-439e-888a-d350e6612e06.png)

![image](https://user-images.githubusercontent.com/77483516/167605110-5a8b3906-f11d-4a54-ac1d-b4ca97d1ba07.png)

OBSERVATIONS:  

1)The dot viewer is showing the latch with enable tied to select [1]. 

2)The remaining part is the mux logic. 



### SKY130RTL D5SK3 L2 Lab incomplete overlapping Case part2:

**COMP_CASE SIMUALTION:**

Command: iverilog comp_case.v tb_comp_case.v 

Command: ./a.out 

Command: gtkwave tb_comp_case.vcd 

![image](https://user-images.githubusercontent.com/77483516/167605340-f40c8738-8eb5-44e6-b1ba-370e19c7aa98.png)

![image](https://user-images.githubusercontent.com/77483516/167605442-9a9bab0e-6a37-49ca-b5a8-b97861f16a98.png)

OBSERVATIONS: The output y is following y when select is 10 or 11.



**COMP_CASE SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog comp_case.v 

Command: synth –top comp_case 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167605593-ab04d743-35ec-44cf-8264-44a43b9f1098.png)

![image](https://user-images.githubusercontent.com/77483516/167605638-7fc6b3a6-ba41-4d27-b30a-8bc4aa709ff8.png)

![image](https://user-images.githubusercontent.com/77483516/167605685-da0bf595-ed61-4160-b494-e77a51ca51fd.png)

![image](https://user-images.githubusercontent.com/77483516/167605753-c77d1618-8544-4188-a1eb-9f37942002c5.png)

OBSERVATIONS: Clearly, there is no latch and circuit is working fine in both simulation and synthesis. 


### SKY130RTL D5SK3 L3 Lab incomplete overlapping Case part3:

**PARTIAL_CASE_ASSIGN SIMULATION:**

Command: iverilog partial_case_assign.v tb_partial_case_assign.v 

Command: ./a.out 

Command: gtkwave tb_partial_case_assign.vcd 

![image](https://user-images.githubusercontent.com/77483516/167605947-6ca65c3b-4c7d-4ed7-acca-fb7c2f7f7f7b.png)

![image](https://user-images.githubusercontent.com/77483516/167605993-aa34153c-96f9-4089-abc4-eb6fc4736f9e.png)

OBSERVATION: Clearly, when select is 01, the x is latching to its value. 


**PARTIAL_CASE_ASSIGN SYNHTESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog partial_case_assign.v 

Command: synth –top partial_case_assign 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167606161-fb457991-d661-46fe-bd20-529de92ca200.png)

![image](https://user-images.githubusercontent.com/77483516/167606235-92fca118-27f6-438a-91df-41d40c673aca.png)

![image](https://user-images.githubusercontent.com/77483516/167606274-d2d74ff2-507c-49fa-8956-8b046247b7f5.png)

![image](https://user-images.githubusercontent.com/77483516/167606325-1393e2fd-efe4-4ca6-8766-9d6b556c3c6e.png)

OBSERVATIONS: 

1) The dot viewer clearly shows the latch for x and there is no latch for y. 


**BAD_CASE SIMULATION:**

Command: iverilog bad_case.v tb_bad_case.v 

Command: ./a.out 

Command: gtkwave tb_bad_case.vcd 

![image](https://user-images.githubusercontent.com/77483516/167606462-8d7ad363-46cb-40d7-9c39-9289eb397b9a.png)

![image](https://user-images.githubusercontent.com/77483516/167606504-3b637bcf-9023-4a0b-a617-9ec55ed4362a.png)

OBSERVATION: Clearly, when the select is 11, the output y is becoming 1. 


### SKY130RTL D5SK3 L4 Lab incomplete overlapping Case part4:

**BAD_CASE SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog bad_case.v 

Command: synth –top bad_case 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167606694-2ac12166-1478-42a2-9fc7-4987e4abf07e.png)

![image](https://user-images.githubusercontent.com/77483516/167606836-ef78491b-dde6-4919-aa2e-0a090e54b675.png)

Observation: There are no latches in bad_case. 

![image](https://user-images.githubusercontent.com/77483516/167606961-1487c35b-e058-4a38-ad50-9dab3a6fc206.png)



**BAD_MUX NETLSIT SIMULATION:**

Command: write_verilog –noattr tb_bad_case_net.v 

Command: iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v bad_case_net.v tb_bad_case.v 

Command: ./a.out 

Command: gtkwave tb_bad_case.vcd 

![image](https://user-images.githubusercontent.com/77483516/167607074-7ef70eab-8b02-4c10-93b1-f7922bc69a0e.png)

![image](https://user-images.githubusercontent.com/77483516/167607128-d47c53a6-3d6c-4dda-ac13-30cde11b36f3.png)

OBSERVATION:  

1)The netlist simulations shows that the output y is taking i3, when the select is 11. 

2) This is a simulation-synthesis mismatch. So, we need to avoid overlapping case while VERILOG coding. 



### SKY130RTL D5SK5 L1 Lab For and For Generate part1:

**MUX_GENERATE.V SIMULATION:**

Command: iverilog mux_generate.v tb_mux_generate.v 

Command: ./a.out 

Command: gtkwave tb_mux_generate.vcd 

![image](https://user-images.githubusercontent.com/77483516/167607306-950b8411-4a72-4a81-a333-fa8d76b2c15e.png)

![image](https://user-images.githubusercontent.com/77483516/167607337-7e9633f8-7e76-4ec3-a25a-f58bd1654d9a.png)

OBSERVATION: We can see the waveforms of a 4:1 mulitplexer designed using for loop. 



**MUX_GENERATE.V SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog mux_generate.v 

Command: synth –top mux_generate 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167607460-2af659a0-3d9b-479e-a84d-1a700b4cb250.png)

![image](https://user-images.githubusercontent.com/77483516/167607501-d9bc5f4a-c5e6-4394-bd7a-449ebb3e8e29.png)

![image](https://user-images.githubusercontent.com/77483516/167607556-451f2376-a0d9-4731-b160-e8679353fcb5.png)

![image](https://user-images.githubusercontent.com/77483516/167607603-2fdf6e53-87e5-4efe-9c4d-7a6a06c99fa7.png)

OBSERVATION: We can see that the synthesis has a latch. The latch just acts as a buffer. 



### SKY130RTL D5SK5 L2 Lab For and For Generate part2: 

**DEMUX_CASE SIMULATION:** 

Command: iverilog demux_case.v tb_demux_case.v 

Command: ./a.out 

Command: gtkwave tb_demux_case.vcd 

![image](https://user-images.githubusercontent.com/77483516/167607775-61fb4a08-f064-40c3-b480-b3f04d2adb7c.png)

![image](https://user-images.githubusercontent.com/77483516/167607823-7c41189c-bb4c-46e1-88da-8f40cf9ba647.png)

OBSERVATION: We can see that output is being selected based on the select line. 


**DEMUX_CASE SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog demux_case.v 

Command: synth –top demux_case 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167607949-ced7f616-dad4-4223-a3af-fc4fc2ba9420.png)

![image](https://user-images.githubusercontent.com/77483516/167608026-e85af2f0-0eb8-4eef-99ac-e3161fe81194.png)

![image](https://user-images.githubusercontent.com/77483516/167608095-3623002f-286e-4eca-945e-8e3c727d4c22.png)

![image](https://user-images.githubusercontent.com/77483516/167608182-b860f09a-a23d-4fea-ac2b-b202367710a8.png)



**DEMUX_GENERATE.V SIMULATION:** 

Command: iverilog demux_generate.v tb_demux_generate.v 

Command: ./a.out 

Command: gtkwave tb_demux_generate.vcd

![image](https://user-images.githubusercontent.com/77483516/167608298-9bc7ed7a-8697-438d-b960-06bd157a20d3.png)

![image](https://user-images.githubusercontent.com/77483516/167608377-c686d1a9-b5d9-48dd-9ed1-c6725c47139e.png)



**DEMUX_GENERATE SYNTHESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog demux_generate.v 

Command: synth –top demux_generate 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show 

![image](https://user-images.githubusercontent.com/77483516/167608450-118fbe43-4a10-4266-a5f0-5a0583e5b184.png)

![image](https://user-images.githubusercontent.com/77483516/167608500-31a0e9f2-c40f-418b-a6ec-dc5e207639df.png)

![image](https://user-images.githubusercontent.com/77483516/167608647-da59f7ea-38c3-4d85-a1c5-63a854444e34.png)

![image](https://user-images.githubusercontent.com/77483516/167608724-b00b785f-6846-41a6-a678-1664f02b916d.png)

OBSERVATION: In this lab, both demux_case.v and demux_generate.v has similar synthesis. However, the demux_generate.v can be scalable. 


### SKY130RTL D5SK5 L3 Lab For and For Generate part3: 

Command: gvim rca.v -o fa.v 

![image](https://user-images.githubusercontent.com/77483516/167608890-06e33bf9-4f50-489d-85ae-821ae7602be4.png)


### SKY130RTL D5SK5 L4 Lab For and For Generate part4: 

**RCA SIMULATION:**

Command: iverilog fa.v rca.v tb_rca.v 

This command tells the simulator that fa.v is separate module but is called in rca.v. 

Command: ./a.out 

Command: gtkwave tb_rca.vcd

![image](https://user-images.githubusercontent.com/77483516/167609183-7bae0b9d-d130-44d7-843d-1143b9875df8.png)

![image](https://user-images.githubusercontent.com/77483516/167609235-2c92e831-e0e1-4cd1-b740-99fc3b5db493.png)


**RCS SYNHTESIS:**

Command: yosys 

Command: read_liberty –lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: read_verilog fa.v 

Command: read_verilog rca.v 

Command: synth –top rca 

Command: abc –liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 

Command: show rca 
 
![image](https://user-images.githubusercontent.com/77483516/167609518-5f12f071-52b5-4708-9655-143680f5e9f2.png)

![image](https://user-images.githubusercontent.com/77483516/167609718-4df9265a-fb49-4736-ac68-fb0284c12356.png)

![image](https://user-images.githubusercontent.com/77483516/167609786-a9fe8018-fc92-414a-a07c-51a819ab8422.png)

![image](https://user-images.githubusercontent.com/77483516/167609916-5fcd524c-4a40-4ac9-af84-ed065f9ca7f3.png)

OBSERVATION: 8 FA MODULES ARE INSTANTIATED. 


**RCA GLS SYNHTESIS:**

Command: write_verilog –noattr tb_rca_net.v 

![image](https://user-images.githubusercontent.com/77483516/167610025-8db4401a-034b-4304-b706-1c527920693a.png)

Command: iverilog ../my_lib/verilog_module/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v tb_rca_net.v tb_rca.v 

Command: ./a.out 

Command: gtkwave tb_rca.vcd 

![image](https://user-images.githubusercontent.com/77483516/167610143-0f882c0e-6c3b-43fb-9fa8-7de6bd470a9b.png)

![image](https://user-images.githubusercontent.com/77483516/167610258-917c312b-e1fc-42aa-8027-a7f4d88154d5.png)

OBSERVATIONS: There is no mismatch between simulation and synthesis. 


