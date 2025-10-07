# VSDBabySoC Lab Deliverables

The **VSDBabySoC** is a simple SoC (System-on-Chip) design that comprises the following:

- RISC-V processor (`rvmyth`)
- PLL (Phase-Locked Loop) module (`pll`)
- DAC (Digital-to-Analog Converter) module (`dac`)

This project demonstrates integration of these IP cores and aims to simulate and verify the design behavior using **pre-synthesis** and **post-synthesis simulations**.

---

## EDA Tools Requirements
- **Compiler:** Icarus Verilog (for compilation)  
- **Waveform Viewer:** GTKWave (for viewing waveform files)

---

## Clone VSDBabySoC
Clone the repository from the following link:  
[VSDBabySoC](https://github.com/manili/VSDBabySoC.git)  

```
git clone https://github.com/kunalg123/rvmyth.git

```

---

## Modules

### `vsdbabysoc.v` (Top-Level SoC Module)
This module integrates the following submodules:
- `rvmyth`
- `pll`
- `dac`

---

### `rvmyth.v` (RISC-V Core)
The **rvmyth** module is a simple RISC-V based processor.  
It outputs a **10-bit digital signal (`OUT`)** to be converted by the DAC.  

Clone it from the following link:  
[rvmyth](https://github.com/kunalg123/rvmyth/)

---

### `avsdpll.v` (PLL Module)
The **pll** module is a Phase-Locked Loop that generates a stable clock (`CLK`) for the RISC-V core.  

- [Introduction](https://github.com/ireneann713/PLL.git)  
- Clone it from the following link: [avsdpll](https://github.com/lakshmi-sathi/avsdpll_1v8.git)

---

### `avsddac.v` (DAC Module)
The **dac** module converts the **10-bit digital signal** from the `rvmyth` core to an analog output.  

Clone it from the following link:  
[avsddac](https://github.com/vsdip/rvmyth_avsddac_interface.git)
