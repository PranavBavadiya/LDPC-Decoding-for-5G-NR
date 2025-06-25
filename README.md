# 📡 LDPC Decoding for 5G-NR

This project implements **Low-Density Parity-Check (LDPC)** code decoding techniques—**Hard Decision** and **Soft Decision**—based on the 5G NR standard. It includes BER and BLER performance evaluation using MATLAB simulations across different code rates and base graphs.

Developed as an end-semester project for **CT216: Introduction to Communication Systems** under the guidance of **Prof. Yash Vasavda**, DAIICT.

---

## 📘 Overview

LDPC codes are modern error-correcting codes known for their performance near the Shannon limit. They are extensively used in **5G New Radio (NR)** systems to ensure efficient and reliable data transmission over noisy channels.

This project focuses on:
- Implementing **Hard Decision Decoding** (Bit-Flipping Algorithm)
- Implementing **Soft Decision Decoding** (Min-Sum Approximation)
- Comparing decoding performance across two base matrices:
  - `NR_2_6_52`
  - `NR_1_5_352`

---

## 🚀 Features

- **Two Base Graphs** (BG1 and BG2) with different lifting sizes (Z = 52, Z = 352)
- **Rate Matching** to simulate various code rates: `1/4`, `1/3`, `1/2`, `3/5`, `4/5`
- **Performance Graphs**:
  - Bit Error Rate (BER) vs. Eb/N0 (Linear & Log scale)
  - Block Error Rate (BLER)
  - Probability of Success vs. Iterations
  - Shannon Limit Approximation

---

## 🧠 Decoding Techniques

### 🔧 Hard Decision Decoding
- Bit-flipping based iterative decoding
- Majority logic voting and parity checks
- Implemented using binary messages (0/1)

### 🧪 Soft Decision Decoding
- Log-Likelihood Ratio (LLR) based message passing
- Uses Min-Sum approximation for Check Node updates
- Incorporates confidence levels from the channel

---

## 📊 Results & Insights

- **Soft decoding** consistently outperforms hard decoding.
- **Lower code rates** (e.g., 1/4) provide better error correction.
- **Higher Eb/N0** significantly improves decoding success.
- Graphs validate decoding performance through metrics like BER, BLER, and convergence rate.

Graphs and discussions can be found in the 📄 `LDPC_32_Report.pdf` and 📄 `LDPC_32_PPT.pdf`.

---

## 📁 Project Structure

```bash
LDPC-Decoding-for-5G-NR
├── 📁 Data/                    # Base matrix text files (NR_2_6_52.txt, NR_1_5_352.txt)
├── 📁 Results/                 # Simulation outputs and graph data
├── 📁 hard_decoding/          # MATLAB code for hard decision decoder
├── 📁 soft_decoding/          # MATLAB code for soft decision decoder
├── 📄 LDPC_32_Report.pdf       # Complete report (theory + results)
├── 📄 LDPC_32_PPT.pdf          # Project presentation slides
├── 📄 LICENSE                  # MIT License
└── 📄 README.md                # This file
```
---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

## 📌 References

- Lecture Slides on Channel Coding by Prof. Yash Vasavda (DAIICT)  
- NPTEL Lectures by Prof. Andrew Thangaraj (IIT Madras)  
- 3GPP 5G NR Specifications  
