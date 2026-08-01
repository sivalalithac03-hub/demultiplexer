# 1-to-4 Demultiplexer using Verilog HDL

## Overview

A **1-to-4 Demultiplexer (DEMUX)** routes one input signal to one of four outputs based on two select lines.

Only one output receives the input value, while the remaining outputs remain LOW.

---

## Truth Table

| S1 | S0 | Input (D) | Y3 | Y2 | Y1 | Y0 |
|----|----|-----------|----|----|----|----|
| 0  | 0  | D | 0 | 0 | 0 | D |
| 0  | 1  | D | 0 | 0 | D | 0 |
| 1  | 0  | D | 0 | D | 0 | 0 |
| 1  | 1  | D | D | 0 | 0 | 0 |

---

## Project Structure

```
Demultiplexer-1to4-Verilog/
│── README.md
│── LICENSE
│── src/
│   └── demux1to4.v
│── testbench/
│   └── demux1to4_tb.v
│── simulation/
│   ├── demux.vcd
│   ├── simulation_output.txt
│   └── waveform.png
```

---

## Software Requirements

- Icarus Verilog
- GTKWave
- ModelSim (Optional)
- Xilinx Vivado (Optional)

---

## Compile

```bash
iverilog -o demux src/demux1to4.v testbench/demux1to4_tb.v
```

## Run

```bash
vvp demux
```

## View Waveform

```bash
gtkwave demux.vcd
```

---

## Expected Results

| Select Lines | Active Output |
|--------------|---------------|
| 00 | Y0 = D |
| 01 | Y1 = D |
| 10 | Y2 = D |
| 11 | Y3 = D |

---

## Applications

- Data Routing
- Communication Systems
- Memory Address Decoding
- Digital Signal Processing

---

## Author

Your Name