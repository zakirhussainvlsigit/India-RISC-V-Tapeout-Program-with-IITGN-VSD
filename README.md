# India-RISC-V-Tapeout-Program-with-IITGN-VSD

## Week-0 Activities
All open-source EDA tools are required to be installed in Week-0.  

- [Tools Installation](week0.md)

---

## Week-1 Activities

- **Day 1**: Introduction to iverilog, gtkwave, VCD file, .lib file, simulation and synthesis  
- **Day 2**: Timing libs, hierarchical vs flat synthesis, and efficient flop coding styles  
- **Day 3**: Combinational and sequential optimizations  
- **Day 4**: GLS, blocking vs non-blocking, and synthesis-simulation mismatch  
- **Day 5**: Optimization in synthesis  

👉 [Click here for Week-1 Labs](week1.md)

---

## Week-2 Activities

**Research: BabySoC Fundamentals & Functional Modelling**

- **Part 1 – Theory (Conceptual Understanding)**  
  📄 [Theory Activities](week2-part1-theory.pdf)

- **Part 2 – Labs on Functional Modelling**  
  📄 [Lab Activities](week2-part2-lab.pdf)

👉 [Click here for Week-2 Activities](week2_BabySoC.md)

---

## Week-3 Activities

**The following link will provide the details of Week-3 Activities**

👉 [Click here for Week-3 Activities](week3)

- **Part 1 – Post-Synthesis GLS**  
  📄 [Part-1 Activities](week3/week3_p1_Post_Synthesis_GLS.md)

- **Part 2 – Fundamentals of STA (Static Timing Analysis)**  
  📄 [Part-2 Activities](week3/week3_p2_Fundamentals_of_STA.md)

- **Part 3 – Generate Timing Graphs with OpenSTA**  
  📄 [Part-3 Activities](week3/week3_p3_Generate_Timing_Graphs_with_OpenSTA.md)

---

### Week-4 Activities

**The following link will provide the details of Week-4 Activities**

👉 [Click here for Week-4 Activities](week4)

---

## Find the link below for the detailed activities document

📄 [Click me for details](Week-4-Tasks.pdf)

---

## 📝 Week 4 Deliverables — CMOS Circuit Design (sky130)

For quick reference, the **Week 4 deliverables** include the following sections:

---

### 📌 1. Introduction / Background
- Briefly describe the **purpose of each experiment**  
  *(e.g., why Id vs Vds, why VTC, etc.)*.

---

### 🧾 2. SPICE Netlists / Code
- Include the **full SPICE netlist(s)** used for each component:
  - Id vs Vds
  - VTC
  - Transient
  - Variation

---

### 📊 3. Plots & Figures
For each experiment, include:
- Graphs:
  - Id vs Vds
  - Id vs Vgs
  - VTC
  - Transient waveforms
  - VTC under variation
- Annotated:
  - Mark threshold point
  - Switching point
  - Points for noise margin, etc.

---

### 📋 4. Tabulated Results
Provide summary tables listing:
- Extracted **threshold voltage(s)**  
- **Rise / fall propagation delays**  
- **Noise margins** *(NM<sub>L</sub>, NM<sub>H</sub>)*  
- **Effect of variation**:
  - Switching point shift
  - Noise margin change
  - Delay impact

---

### 🧠 5. Observations / Analysis
For each experiment, include a short discussion:
- What you see *(e.g., saturation onset, threshold shift)*  
- Why it happens *(device physics)*  
- How this ties back to **STA concepts** *(e.g., delay models, variation, margin)*

---

### 🏁 6. Conclusions
Higher-level reflections:
- How **transistor-level behavior** constrains **timing** in real circuits  
- How **variation or supply changes** can affect **STA margins** and **critical paths**

---

### 📚 7. References / Citations
- If any literature or models were referenced *(e.g., sky130 models)*, list them here.

---

