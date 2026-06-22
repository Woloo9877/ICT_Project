Single-Cycle Processor with SIMD Support (Verilog HDL)
Project Overview
This project documents the design, implementation, and verification of a high-performance single-cycle processor based on a custom MIPS-like Instruction Set Architecture (ISA). The processor features a 64-bit internal datapath, Harvard architecture, and advanced SIMD (Single Instruction, Multiple Data) capabilities.

The design was fully implemented in Verilog HDL and validated using the Xilinx ISim environment.

Key Features
Architecture: Classic Harvard architecture with separate instruction and data memory spaces.

Datapath: 64-bit internal datapath designed for high-throughput arithmetic.

Instruction Set: Supports R-type, I-type, and J-type instructions with 95% instruction set coverage.

SIMD Support: Includes specialized instructions (e.g., VMUL, vlw) for parallel data processing.

Advanced Operations:

18-operation 64-bit ALU.

Dedicated Hi and Lo registers for multiplication results.

4-bit Status Register (SR) for flag management.

Lane-selective write logic for SIMD operations.

Architecture Highlights
ALU: A 64-bit combinational unit capable of performing arithmetic, logic, shift, and SIMD-specific operations.

Memory System: 16-bit wide memory interface with a sign-extension unit to handle I-Type immediate values efficiently.

Hazard Management: Data hazards (specifically between MUL and MFLO instructions) are managed via software-level NOP stalls to maintain pipeline integrity.

Simulation & Verification
The processor was verified using a comprehensive test program that executes a sequence of complex instructions:

Arithmetic: Validated MUL functionality and storage in Hi/Lo registers.

Data Movement: Confirmed MFLO operations through software stall management.

Control Flow: Verified J (unconditional jump) instruction execution.

SIMD: Validated parallel multiplication logic.
