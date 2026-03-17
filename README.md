# Computer Organization and CPU Design
This repository contains a comprehensive collection of hardware design source code and laboratory reports for the Computer Organization course. The project follows a modular, bottom-up design philosophy, starting from basic logic components and culminating in a functional MIPS-architecture CPU that supports both R-type and I-type instructions. All modules are implemented using Verilog HDL.

# Experiment 2: Lookahead Carry Adder (LCA)
This project implements a 4-bit Lookahead Carry Adder by utilizing four 1-bit full adders in conjunction with a parallel carry-lookahead unit. This design effectively reduces the propagation delay associated with traditional ripple-carry adders by calculating carry signals simultaneously, resulting in higher computational efficiency for arithmetic addition.

# Experiment 3: Multi-function Arithmetic Logic Unit (ALU)
This project features the design of a 32-bit multi-function ALU. The module can perform various operations including bitwise AND, OR, XOR, addition, subtraction, magnitude comparison, and shifting based on specific control signals. It also outputs real-time status flags, such as the Zero Flag (ZF) and Overflow Flag (OF), which are essential for supporting conditional branch instructions in the CPU.

# Experiment 4: Register File Design
This project involves the implementation of a register file containing thirty-two 32-bit registers. The module supports dual-port asynchronous read operations and single-port synchronous write operations. While data can be read in real-time without waiting for a clock edge, write operations are strictly managed by a write-enable signal and the rising edge of the system clock to ensure data stability.

# Experiment 5: Memory Unit Design
This project establishes a main memory module by instantiating a RAM IP Core. The design encapsulates the read and write logic of the underlying storage units. Through the use of write-enable signals and the address bus, it provides stable 32-bit data access, which serves as the foundational data storage support for the CPU's data path.

# Experiment 6: MIPS Assembler and Simulator
This project focuses on assembly language programming practices for the MIPS architecture. By writing and executing specific .asm files within a simulator, the execution processes of various logical and arithmetic instructions were verified alongside register state transitions. This phase provided a rigorous theoretical foundation for the subsequent hardware design of instruction decoding and data path logic.

# Experiment 7: Instruction Fetch and Decode
This project implements the instruction fetch module, the first critical step in processor operation. It consists primarily of a Program Counter (PC) and an instruction memory. The PC increments automatically with each external clock cycle to drive the memory to output 32-bit instruction codes. The module was physically verified on an FPGA board using an LED array through specific pin constraints.

# Experiment 8: R-Type CPU Design
This project integrates the previously designed ALU, register file, and instruction fetch modules into a top-level architecture. By constructing a complete data path, this CPU prototype successfully parses and executes pure R-type MIPS instructions. The system can correctly read instruction register addresses, perform arithmetic or logical operations, and accurately write the results back to the target register.

# Experiment 9: R-I Type CPU Design
This project represents a major upgrade to the previous CPU by incorporating a data memory module and more complex controller logic. By adding multiplexers and various control signals such as select_ALU_F and select_M_R_Data, the data path was expanded to support a mixed instruction set of R-type and I-type commands. This design is fully prepared for synthesis and hardware-level verification on a standard FPGA platform.
