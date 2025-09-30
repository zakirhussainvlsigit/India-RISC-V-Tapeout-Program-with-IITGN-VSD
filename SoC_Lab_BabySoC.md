# VSDBabySoC Lab Deliverables

The **VSDBabySoC** is a simple System-on-Chip (SoC) design that integrates the following IP cores:

- **RISC-V processor** (`rvmyth`)
- **PLL (Phase-Locked Loop) module** (`pll`)
- **DAC (Digital-to-Analog Converter) module** (`dac`)

This project demonstrates the integration of these IP cores and aims to **simulate and verify the design behavior** using both **pre-synthesis** and **post-synthesis** simulations.

---

## EDA Tool Requirements

- **Compiler**: [Icarus Verilog](http://iverilog.icarus.com/) (for compilation)
- **Waveform Viewer**: [GTKWave](http://gtkwave.sourceforge.net/) (for viewing waveform files)

---

## Clone the VSDBabySoC Repository

```bash
git clone https://github.com/manili/VSDBabySoC.git
