---

# Week 3 Task - Post-Synthesis GLS & STA Fundamentals

## 🎯 Objective

To understand and perform **Gate-Level Simulation (GLS)** after synthesis, validate functionality, and get introduced to **Static Timing Analysis (STA)** concepts with practical experiments using **OpenSTA**.

---

## 🧩 Part 1 – Post-Synthesis GLS

### Reference

* **GLS Flow and Methodology:** [VSD_HDP – Day 6 Example](https://github.com/Ananya-KM/VSD_HDP/blob/main/Day%206.md)

### 🔧 Steps

1. Perform **synthesis** of the **BabySoC** design.
2. Run **Gate-Level Simulation (GLS)** using the synthesized **netlist**.
3. Compare **GLS output** with **functional simulation output** (from *Week 2* task).

   * The results **should match**.

### 📦 Deliverables

* Synthesis logs
* GLS waveform screenshots
* Short note confirming:

  > ✅ *GLS output = Functional output*

---

## 📘 Part 2 – Fundamentals of STA (Static Timing Analysis)

### 📚 Learning Resource

If STA is new to you, start with this **free foundational course (free for 4 days)**:
👉 [STA Fundamentals – Udemy](https://www.udemy.com/course/vlsi-academy-stachecks/?couponCode=F960AEDD365E0CD12546)

### 🧠 Focus Topics

* Setup and Hold checks
* Slack
* Clock definitions
* Path-based analysis

### 📄 Deliverable

* A **one-page summary** or **key notes** from the STA course (*bullet points are fine*).

---

## ⚙️ Part 3 – Generate Timing Graphs with OpenSTA

### 🔗 Resources

* **OpenSTA GitHub:** [The-OpenROAD-Project/OpenSTA](https://github.com/The-OpenROAD-Project/OpenSTA)
* **Example Script:** [Day 19 – VSD_HDP](https://github.com/arunkpv/vsd-hdp/blob/main/docs/Day_19.md)
* **Documentation (PDF):** [OpenSTA User Guide](https://github.com/The-OpenROAD-Project/OpenSTA/blob/master/doc/OpenSTA.pdf)

### 🧾 Steps

1. Load your **synthesized netlist** and **constraints** into OpenSTA.
2. Generate **timing graphs** (setup/hold paths, slack, etc.).
3. Capture at least **one timing report** and its corresponding **graph**.

### 📦 Deliverables

* OpenSTA input scripts
* Timing reports and graphs (screenshots with **your userid and timestamp** clearly visible)
* **Observations**, such as:

  * What is the **critical path**?
  * What does the **slack** indicate?

---

## ✅ By the End of Week 3, You Will:

1. Perform **GLS** and validate **functional correctness post-synthesis**.
2. Gain **basic STA knowledge**.
3. Generate **timing graphs** using **OpenSTA** and interpret **timing paths**.

---
