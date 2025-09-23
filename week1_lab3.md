### Lab3: Labs using Yosys and Sky130 PDKs

- Lab3 Yosys 1 good mux Part1
    - invoke yosys synthesizer by typing the command 'yosys' then you will see the below image wherein the marked 2 is yosys tool's command prompt
      <img width="1581" height="362" alt="image" src="https://github.com/user-attachments/assets/07de4f87-f78a-4d65-9e75-bd7a289695e8" />
    - To come out of the tool's command prompt type 'exit' as shown below
      <img width="1177" height="248" alt="image" src="https://github.com/user-attachments/assets/ed9e434e-ab1a-47fe-abe0-eff899a94892" />
    - In the cloned GitHub repository you will find two sub-directories 1. lib 2. my_lib. marked 1 is the lib directory which contains the standard cells library and the marked 2 is the my_lib directory which contains the verilog models marked as 4 of that corresponding standard cell library marked as 3. which are shown as in the below image.
      <img width="1421" height="472" alt="image" src="https://github.com/user-attachments/assets/a5023468-96cf-4fa3-9760-1c81423f26d8" />
    - To do the syntheis first invoke the yosys tool by typing the command 'yosys' and then read the liberty or standard cell library file using the command
      'read_liberty -lib standard_cell_library_name' as shown below
      <img width="1312" height="367" alt="image" src="https://github.com/user-attachments/assets/ebb65546-86e2-4672-8323-98bc8f143861" />
    - Once liberty file is read the next step is to read the verilog file using the command 'read_verilog verilogFile.v' as shown below. If more than one file then read the all the verilog files.
      <img width="1167" height="321" alt="image" src="https://github.com/user-attachments/assets/c330648b-15e2-486c-b57f-4bda76c53936" />
    - After reading you must see the below image
      <img width="967" height="245" alt="image" src="https://github.com/user-attachments/assets/c5b4937d-35a6-408a-830c-f196ba612c8f" />
    - Once read, then type the command 'synth -top verilogModuleName' as shown below
      <img width="1239" height="303" alt="image" src="https://github.com/user-attachments/assets/4f973b7f-0a81-40ff-9a10-ac62c325aae8" />
    - Once generic synthesis is done, now do the mapping to standard cells using the command\
      'abc -liberty standardCellsLibraryName' as shown below
      <img width="831" height="490" alt="image" src="https://github.com/user-attachments/assets/e29bbd7a-803c-4ce7-a993-bd2a02e619b2" />







