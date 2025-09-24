### Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles : Labs


## Lab4 Introduction to timing .libs

- Lab4 Introduction to dot Lib part1: Discussed Brierly about PVT, P-process V-voltage T-temerature
  <img width="1197" height="614" alt="image" src="https://github.com/user-attachments/assets/d0a73c01-2caa-40cf-a806-2b1c8b69bf0d" />

- Lab4 Introduction to dot Lib part2: In this lab, .lib equivalent verilog models been discussed briefly.  
     - The following is the .lib model file  
    <img width="972" height="666" alt="image" src="https://github.com/user-attachments/assets/ba674393-62fe-40cc-8097-ec1751bcb8fd" />   
     - The following is the verilog model    
  <img width="757" height="535" alt="image" src="https://github.com/user-attachments/assets/3486ecfb-98f2-4d35-8a42-36ad86cc1cb3" />

- Lab4 Introduction to dot Lib part3: In this lab, various gates with various area, delay been discussed.
     - The following is the same gates with different area in .lib file
       <img width="794" height="615" alt="image" src="https://github.com/user-attachments/assets/5da2e935-4450-4fc3-aaca-aa3fe1c0f516" />
          - Another AND gate but with different area
       <img width="800" height="616" alt="image" src="https://github.com/user-attachments/assets/24b2412b-b705-4098-881e-8b38258f0e11" />
### Lab5 Hierarchical vs Flat Synthesis
- Lab05 Hierarchical synthesis vs flat synthesis part1 [Example is multiple modules\]
  <img width="882" height="362" alt="image" src="https://github.com/user-attachments/assets/b4fbf4db-5e52-4d1c-a7df-04e09013a5e6" />
  <img width="821" height="591" alt="image" src="https://github.com/user-attachments/assets/4eb6f216-a281-4382-a574-eef96e5d030d" />
     - Hierarchy is maintained in the following
       <img width="1757" height="426" alt="image" src="https://github.com/user-attachments/assets/10605c4f-b6db-4dd1-9321-201163b2aefd" />
     - Writing hierarchical netlist file
       <img width="781" height="316" alt="image" src="https://github.com/user-attachments/assets/34a53332-d93c-4923-9097-de23efb60d36" />
     - Hierarchical netlist shown below
       <img width="1389" height="913" alt="image" src="https://github.com/user-attachments/assets/333d6436-c163-4e5d-b84b-9262d93623b1" />
### Now lets see what is Flat synthesis
- Lab05 Hierarchical synthesis vs flat synthesis part2 [Example is multiple modules\]
     - Flat synthesis shown below with command 'flatten'
       <img width="857" height="627" alt="image" src="https://github.com/user-attachments/assets/f61066c8-389a-4947-acd5-86c9d64d0ca6" />
     - The corresponding flattned image is shown below
       <img width="1673" height="401" alt="image" src="https://github.com/user-attachments/assets/4e142bcf-644a-419b-af52-b7aab0282a28" />
     - The following is the netlist file
       <img width="1513" height="749" alt="image" src="https://github.com/user-attachments/assets/4c608b12-3832-4aa0-9c2c-83a914326396" />
### Various Flop Coding Styles and optimization












