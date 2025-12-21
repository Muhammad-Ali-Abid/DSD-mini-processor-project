# DSD Mini Processor Project

## Group Members:
1. Ibtisam Shoaib  
2. Muhammad Zaryab  
3. Fatima Muzammil  
4. Fizza Faisal  
5. Muhammad Ali Abid

---

# Mini RISC-V Processor (RV32I) – Verilog Implementation

## 📌 Project Overview
This project implements a **mini RISC-V processor** based on the **RV32I base integer instruction set**, designed and written entirely in **Verilog HDL**.  
The processor follows a **Harvard architecture**, using **separate instruction and data memories**, and is controlled using a **multi-cycle finite state machine (FSM)**.

The goal of this project is to understand and implement the **core concepts of processor design**, including instruction decoding, datapath design, control logic, and memory interfacing.

---

## 🧠 Architecture Overview
- **Instruction Set**: RISC-V RV32I (subset)
- **Word Size**: 32-bit
- **Architecture Type**: Harvard
- **Control Strategy**: Multi-cycle FSM
- **Design Style**: Modular (Control Unit + Datapath)

### High-Level Components
- Program Counter (PC)
- Instruction Register (IR)
- Control Unit (FSM-based controller)
- Register File (32 × 32-bit registers)
- Arithmetic Logic Unit (ALU)
- Instruction Memory (ROM)
- Data Memory (RAM)
- Immediate Generator
- ALU Control Unit

---

## 📐 Supported Instruction Types
This processor supports the **six RISC-V instruction formats**:

| Type | Description |
|----|------------|
| R-type | Register-to-register ALU operations |
| I-type | Immediate arithmetic and load instructions |
| S-type | Store instructions |
| B-type | Conditional branch instructions |
| U-type | Upper immediate instructions |
| J-type | Jump instructions |

---

## ⚙️ Instruction Subset (Initial)
The initial implementation focuses on a minimal yet functional subset:

- **Arithmetic**: `add`, `sub`, `addi`, `and`, `or`
- **Memory**: `lw`, `sw`
- **Control Flow**: `beq`, `jal`

This subset is sufficient to run simple programs and demonstrate full processor functionality.

---

## 🔁 Multi-Cycle Execution Model
Each instruction is executed over multiple clock cycles:

1. **Instruction Fetch**
2. **Instruction Decode & Register Read**
3. **Execute / Address Calculation**
4. **Memory Access (if required)**
5. **Write Back (if required)**

This approach simplifies hardware complexity and makes the control logic easier to understand and extend.

---

## 🧪 Verification
- Simulated using standard Verilog simulators (ModelSim / Icarus Verilog)
- Instruction-level testing using hand-written RISC-V machine code
- Separate testbenches for major modules

---

## 🚀 Project Goals
- Understand RISC-V instruction formats and decoding
- Design a clean datapath and control unit
- Implement a working processor core from scratch
- Build a strong foundation for pipelined or FPGA-based designs

---

## 📈 Future Enhancements
- Add full RV32I instruction support
- Implement pipelining
- Add hazard detection and forwarding
- Integrate UART or GPIO peripherals
- FPGA synthesis and hardware testing

---

## 📜 License
This project is for educational purposes and is open for learning and experimentation.
