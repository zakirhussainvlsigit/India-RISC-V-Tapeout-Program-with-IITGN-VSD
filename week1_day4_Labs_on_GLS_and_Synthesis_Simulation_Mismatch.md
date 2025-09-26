# Labs on GLS and Synthesis-Simulation Mismatch

- GLS stands for Gate Level Simulation  

- Todo the gate level simulation we need the following 3 files  
   1. verilog model files of the standard cell library
   2. netlist file  
   3. testbench file  


- Lab GLS Synth Sim Mismatch part1
   - The following are the files for this lab
     <img width="855" height="159" alt="image" src="https://github.com/user-attachments/assets/4abe3437-716b-42fb-8a1d-965e954b0fdb" />
   - Consider mux2x1 using ternary operator
      - iverilog for comiling : After compilation we will get a.out file
      - execute the a.out in the terminal ./a.out, this will generate the .vcd file
      - See that as shown in the below figure
       <img width="882" height="183" alt="image" src="https://github.com/user-attachments/assets/b9c876b6-58ce-47ad-9998-6b12394927a7" />
       
       - Use gtkwave with .vcd file, to view the waveform, as shown below
         
       <img width="919" height="168" alt="image" src="https://github.com/user-attachments/assets/8aa31145-51c1-46aa-9a4c-2680ebb23231" />

       - Simulation result of the mux2x1

         <img width="1352" height="641" alt="image" src="https://github.com/user-attachments/assets/15e6d5c4-8662-43bc-b4e3-b325db432bf6" />
 
       - Synthesize the design, as shown below
 
         <img width="913" height="582" alt="image" src="https://github.com/user-attachments/assets/a8b2ae66-0135-45c6-a1ae-c66acc3dde80" />
 
       - perofrm GLS: compile :- verilog models of the standard cells, netlist file, testbench file as shown below
         
         <img width="872" height="102" alt="image" src="https://github.com/user-attachments/assets/272ab7cd-69c4-4a9e-97a6-75a93d8cfe04" />
 
       - execute a.out, it will generate .vcd file, now open it using gtkwave as shown below

         <img width="1002" height="297" alt="image" src="https://github.com/user-attachments/assets/fb8e27c7-699f-4b88-acad-0685102aa55d" />
 
       - From the below GLS : We can see standard cell and the behavior of mux2x1
    
         <img width="1347" height="641" alt="image" src="https://github.com/user-attachments/assets/cf7470b8-d9fe-40e9-bb4e-4608f207743d" />


 
       - 




     - Lab GLS Synth Sim Mismatch part2



 

