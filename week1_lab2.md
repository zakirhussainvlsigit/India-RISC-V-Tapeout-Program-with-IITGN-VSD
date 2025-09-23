### Week-1 Lab2 : Lab2 Introduction iverilog and gtkwave

* Lab2 Introduction iverilog gtkwave part1

   * Goto the directory called verilog_files, you will see the following. In this you will find several verilog designs with their corresponding Testbenches.

  <img width="1841" height="562" alt="image" src="https://github.com/user-attachments/assets/2c284865-3329-4e4b-8716-8273a298080a" />


   * Test the Multiplexor example: To compile type the command 'iverilog' along with design file and its associated testbench file as shown below
 
     <img width="1311" height="117" alt="image" src="https://github.com/user-attachments/assets/23ab9094-9550-4dbc-8b99-9c99ac99f7aa" />
  
   * Once successfully compiled you will see a.out file created as shown below
     
     <img width="1726" height="355" alt="image" src="https://github.com/user-attachments/assets/29ede5dd-85b6-48c5-8433-e645f420dd09" />

   * Execute the a.out as shown below, which will dump the .vcd file. vcd= value change dump which is a file that contains the simulation result to view it in the waveform viewer tool such as GTKWave
     
     <img width="1052" height="248" alt="image" src="https://github.com/user-attachments/assets/4ea7ef41-8492-4cee-8ca2-c27738c1d019" />

   * To launch the waveform viewer you need use that vcd file, type the command 'gtkwave file.vcd' as shown below
 
     <img width="1315" height="135" alt="image" src="https://github.com/user-attachments/assets/64c2877f-07ef-4709-b7bd-55adf03df125" />




