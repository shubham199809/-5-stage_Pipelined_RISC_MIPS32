# -5-stage_Pipelined_RISC_MIPS32
5-Stage Pipelined RISC MIPS32
This repository contains the implementation of a 5-stage pipelined RISC (Reduced Instruction Set Computer) processor based on the MIPS32 architecture. The design is capable of executing a set of instructions in a pipelined manner, significantly improving the overall throughput compared to a single-cycle implementation.

Table of Contents
Introduction
Features
Architecture
Pipeline Stages
Instruction Set
Installation
Usage
Testing
Contributing
License
Introduction
MIPS32 is a RISC architecture that is widely studied in computer architecture courses. This project implements a 5-stage pipelined processor that follows the MIPS32 instruction set. Pipelining increases the CPU instruction throughput, allowing multiple instructions to be processed simultaneously by different stages of the processor.

Features
5-Stage Pipeline: The processor is divided into five stages: Fetch, Decode, Execute, Memory, and Write-back.
Hazard Detection: Implements techniques for handling data hazards, control hazards, and structural hazards.
Forwarding: Data forwarding is used to resolve data hazards when possible.
Branch Prediction: Basic branch prediction mechanism to reduce the penalty of control hazards.
Support for MIPS32 Instructions: Implements a subset of the MIPS32 instruction set.
Architecture
The architecture of the processor follows a 5-stage pipeline, with each stage responsible for a specific part of the instruction processing:

Instruction Fetch (IF): Fetches the instruction from memory.
Instruction Decode (ID): Decodes the fetched instruction and reads the necessary registers.
Execute (EX): Executes the instruction using the ALU.
Memory Access (MEM): Accesses memory for load/store instructions.
Write-back (WB): Writes the result back to the register file.
Pipeline Stages
1. Instruction Fetch (IF)
Fetches the instruction from instruction memory based on the Program Counter (PC).
The PC is updated to point to the next instruction.
2. Instruction Decode (ID)
Decodes the fetched instruction.
Reads operands from the register file.
Performs sign extension if necessary.
3. Execute (EX)
Performs arithmetic or logical operations using the ALU.
Computes the effective address for memory access instructions.
4. Memory Access (MEM)
Accesses data memory for load and store instructions.
Performs the actual memory read or write operations.
5. Write-back (WB)
Writes the result back to the destination register in the register file.
