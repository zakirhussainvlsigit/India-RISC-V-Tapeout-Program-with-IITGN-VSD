## Part 1 – Post-Synthesis GLS  

## Step 1: read the verilog modules and other required files
```
yosys
read_verilog /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/module/vsdbabysoc.v
read_verilog -I /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/include /home/zakir/Desktop/week2Labs/VSDBabySoC/output/compiled_tlv/rvmyth.v
read_verilog -I /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/include /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/module/clk_gate.v
```

<img width="810" height="497" alt="image" src="https://github.com/user-attachments/assets/6c6832e7-d7bd-47d8-b61b-09d9545f99f0" />

<img width="806" height="502" alt="image" src="https://github.com/user-attachments/assets/2319f9d2-30b1-4dbf-aa4f-a589240f5512" />

<img width="891" height="505" alt="image" src="https://github.com/user-attachments/assets/caee1952-51c4-41e2-89d8-ab1938e0e78d" />  

---

## Step 2: read the standard cell library, liberty file
```
read_liberty -lib /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/lib/avsdpll.lib
read_liberty -lib /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/lib/avsddac.lib
read_liberty -lib /home/zakir/Desktop/week3Labs/p1/VSDBabySoC/src/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

<img width="1127" height="573" alt="image" src="https://github.com/user-attachments/assets/f29ad963-02e6-4f30-9f21-dfc7f59bb9a6" />

<img width="1143" height="578" alt="image" src="https://github.com/user-attachments/assets/33f8a9d8-bb24-47c3-b14b-49ad1b68cd38" />

<img width="1127" height="572" alt="image" src="https://github.com/user-attachments/assets/e986bdeb-82b9-4550-817f-1c2281afdb48" />  

---

## Step 3: Run Synthesis use top module name, which is vsdbabysoc

- synth -top vsdbabysoc
  
  <img width="1151" height="751" alt="image" src="https://github.com/user-attachments/assets/373ea46a-0cc5-4c0a-81c2-b7a43f0f9b37" />

  <img width="880" height="632" alt="image" src="https://github.com/user-attachments/assets/ffab06b8-5171-4a89-b6ed-c8d9dc3cdf33" />

  <img width="770" height="767" alt="image" src="https://github.com/user-attachments/assets/b5e9f472-61f0-499a-84a1-7b87c02f4c64" />

  <img width="721" height="587" alt="image" src="https://github.com/user-attachments/assets/6c4cc6aa-07a2-4652-924c-cba28334783e" />

  <img width="710" height="856" alt="image" src="https://github.com/user-attachments/assets/0023e38f-9dd5-4216-ade5-291a299c7377" />

  ## Step 4: Sequential logic map it to D Flip-Flops from Standard Cells

  - dfflibmap -liberty /home/zakir/Desktop/week3Labs/part1/VSDBabySoC/src/lib/sky130_fd_sc_hd__tt_025C_1v80.lib

    <img width="1188" height="55" alt="image" src="https://github.com/user-attachments/assets/6ea0247a-8975-40da-8414-a7321b97c891" />

    <img width="927" height="158" alt="image" src="https://github.com/user-attachments/assets/e1304fe6-8e06-4e72-811a-91031f61154d" />

 ## Step 5: Perform Optimization and Technology Mapping

 - opt
 - abc -liberty /home/zakir/Desktop/week3Labs/part1/VSDBabySoC/src/lib/sky130_fd_sc_hd__tt_025C_1v80.lib -script +strash;scorr;ifraig;retime;{D};strash;dch,-f;map,-M,1,{D}

   <img width="1165" height="717" alt="image" src="https://github.com/user-attachments/assets/15e0606a-e826-4e7d-98fc-f3bbdc9216d6" />

   <img width="1802" height="217" alt="image" src="https://github.com/user-attachments/assets/2029dfe1-f126-4875-8778-88aa82ec98a6" />

   <img width="1140" height="232" alt="image" src="https://github.com/user-attachments/assets/e142a932-0dfa-4322-bada-35adbd5f2621" />

## Step 6: Perform Final Clean-Up and Renaming
- flatten
- setundef -zero
- clean -purge
- rename -enumerate

<img width="886" height="502" alt="image" src="https://github.com/user-attachments/assets/30b3c987-3ecb-42d0-8191-d69671cbdf7d" />

## Step 7: Check Statistics
- stat

<img width="921" height="847" alt="image" src="https://github.com/user-attachments/assets/c44007df-5a0e-42b7-9b07-70577c0dc2b8" />

<img width="762" height="807" alt="image" src="https://github.com/user-attachments/assets/57591ffd-cec7-4378-b795-de5ad35ff0d0" />

## Step 8: Write the Synthesized Netlist
- write_verilog -noattr /home/zakir/Desktop/week3Labs/part1/post_synth_sim/vsdbabysoc.synth.v

<img width="1186" height="343" alt="image" src="https://github.com/user-attachments/assets/5fd7c6e4-574b-4438-bd10-7dbfa9d0a821" />

---
POST_SYNTHESIS SIMULATION AND WAVEFORMS
---
## Step 1: Compile the Testbench
Run the following iverilog command to compile the testbench:

iverilog -o /home/zakir/Desktop/week3Labs/part1/post_synth_sim/post_synth_sim.out -DPOST_SYNTH_SIM -DFUNCTIONAL -DUNIT_DELAY=#1 -I /home/zakir/Desktop/week3Labs/part1/VSDBabySoC/src/include -I /home/zakir/Desktop/week3Labs/part1/VSDBabySoC/src/module /home/zakir/Desktop/week3Labs/part1/VSDBabySoC/src/module/testbench.v

<img width="1487" height="437" alt="image" src="https://github.com/user-attachments/assets/677a6dd4-9bf7-44cf-87d6-4e45bc7ce3f0" />

<img width="1330" height="158" alt="image" src="https://github.com/user-attachments/assets/ccb2c0eb-d1fc-477e-87e6-ae377d94809c" />

<img width="1242" height="327" alt="image" src="https://github.com/user-attachments/assets/b50d5519-040f-4daa-9b56-cf44eda74491" />

<img width="1147" height="272" alt="image" src="https://github.com/user-attachments/assets/37c43703-3b5d-4825-b4a0-35704de37ba4" />

<img width="1858" height="893" alt="image" src="https://github.com/user-attachments/assets/181241a7-f687-4f8a-8f30-f7d2ec96662a" />

























