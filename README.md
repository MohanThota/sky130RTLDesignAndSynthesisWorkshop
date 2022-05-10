![image](https://user-images.githubusercontent.com/77483516/167080105-2a7f5195-23eb-4444-a444-74f917136e4e.png)
**# sky130RTLDesignAndSynthesisWorkshop**
Day 1 - Introduction to Verilog RTL design and Synthesis 

SKY130RTL D1SK1 L1 Introduction to iverilog design test bench 

In the first lecture of the course, we learnt about the definitions of the RTL Design, Simulator and Test Bench. The simulator we are going to use in this workshop is iverilog. After the definitions of the terms mentioned above, we learnt the workings of Simulator and Test Bench. 

Simulator Working: 

Simulator looks for the changes in the input and for every change in the input, we observe changes in the output.  

Test Bench: 

Test Bench generates the stimulus for the design and observes the output. 
![TESTBENCH](https://user-images.githubusercontent.com/77483516/167550635-d5befd27-03e4-4af8-9bad-02c12f0ba7bb.PNG)
Iverilog based simulator flow: 

iverilog simulator takes the design and corresponding test bench of the design and generates the vcd( Value Change Dump format) file. The vcd file can be viewed using gtkwave waveform viewer. 
 ![iverilog simulation flow](https://user-images.githubusercontent.com/77483516/167551131-933b6e74-853b-4ee7-bc6f-bbfbad235220.PNG)
**SKY130RTL D1SK2 - Labs using iverilog and gtkwave 
**
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

