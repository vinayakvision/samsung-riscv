
# **Samsung-riscv**
The program focuses on the RISC-V architecture and leverages open-source tools to educate participants about VLSI chip design and RISC-V. The internship is led by Kunal Ghosh Sir.

## *Basic Details*

**Name:** Vinayak Venkappa Pujeri

**College:** Vidyavardhaka College of Engineering

**Email ID:** vision.vinayak12@gmail.com / vinayakpujeri2047@gmail.com

**GitHub Profile:** vinayakvision

**LinkedIN Profile:** vinayakvision

---

<details>
<summary> <b>Task 1:</b> The task involves thoroughly reviewing the lab videos related to C programming and the RISC-V architecture to gain a comprehensive understanding of both topics. Afterward, you are required to compile C code using two different compilers: the GCC compiler and the RISC-V compiler. This exercise will showcase your grasp of the compilation process, where you will observe and compare how each compiler translates the C code into machine code, highlighting the differences and specificities of the compilation process for different architectures.</summary> 
<br>
Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler.

**C Language based LAB**

**C and RISC-V Based Labs**

This repository demonstrates the processes involved in compiling C programs and generating assembly code using both a standard GCC compiler and a RISC-V GCC compiler. It includes comprehensive steps and explanations to guide users through each stage of the compilation and debugging workflow.

**C Language-Based Lab**

Steps to Compile a .c File on Your Machine:

1. Open the bash terminal and navigate to the directory where you want to create your file.
2. Use the following command to create and edit a new .c file:
   ```sh
   leafpad sum1ton.c


**Steps to Compile a .c File on our Machine:**
 ```sh
 gcc sum1ton.c
 ./a.out
```

 
Compilation and execution complete.
 
![2](https://github.com/user-attachments/assets/5363e456-21a1-498f-b360-5f5d66a58029)
)
RISC-V Based Lab

**Steps to Compile Using RISC-V GCC Compiler:**
1. Ensure the RISC-V GCC compiler is installed and accessible on your system.
2. Verify the .c file contents using the cat command:
   ```sh
   cat sum1ton.c


3. Compile the C program for RISC-V architecture using 01 option:
 ```sh
riscv64-unknown-elf-gcc -o1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
4. Disassemble the object file to view its assembly code using:
 ```sh
riscv64-unknown-elf-objdump -d sum1ton.o
```
5.minimize the assembly by using following code:
```sh
riscv64-unknown-elf-objdump -d sum1ton.o | less
```
 a)we extract main function's assembly code by using:
   ```sh
/main
```
6. Use /main in the terminal to locate the main function in the assembly output.
![4](https://github.com/user-attachments/assets/1f0acd4c-5ffa-43a4-97b6-fe6d89757fdf)
)

7.Compile the C program for RISC-V architecture using ofast option:
```sh
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
8.Disassemble the object file to view its assembly code using:
```sh
riscv64-unknown-elf-objdump -d sum1ton.o
```
9.minimize the assembly by using following code:
```sh
riscv64-unknown-elf-objdump -d sum1ton.o | less
```
 a)we extract main function's assembly code by using:
 ```sh
  /main
```
10. Use /main in the terminal to locate the main function in the assembly output.
![4](https://github.com/user-attachments/assets/a8cf86d0-0954-4ad8-a923-ffe519db5115)
)

Explanation of Key Commands and Options: 
1. -mabi=lp64: Specifies the Application Binary Interface (ABI) for 64-bit integers, pointers, and long data types, suitable for 64-bit RISC-V architecture.

2. -march=rv64i: Indicates the 64-bit RISC-V base integer instruction set architecture.

3. -O1: Enables basic optimization for better performance without significantly increasing compilation time.

4. -Ofast: Optimize the code aggressively for the best possible speed.

5. riscv64-unknown-elf-objdump: A tool for disassembling RISC-V binaries to examine the code structure and debug it effectively.
 
   </details>

---

<details>
<summary> <b>Task 2:</b> The task involves reviewing both C-based and RISC-V-based lab videos to understand the nuances of compiling C code for different architectures. Afterward, you are required to execute the process of compiling the C code using two distinct tools: the GCC compiler and the RISC-V compiler simulator. This will allow you to demonstrate your ability to work with both compilers, providing insights into how the C code is processed and converted into machine-readable code for each specific architecture.</summary> 
<br>

Task is to analyze the SPIKE simulation performance using RISC-V GCC with -O1 and -Ofast optimization levels.  

*SPIKE Simulation and Compiler Optimization*

This repository demonstrates how to compile a C program using RISC-V GCC, simulate it using SPIKE, and compare the performance of different optimization levels (-O1 and -Ofast). It includes detailed steps and explanations to ensure clarity.  

**Steps to Complete the Task**  

1.Write a Simple C Program  

2.The following program calculates the swaping of two numbers:  

3.Compile Using RISC-V GCC

4.Compile with -O1 Optimization.

*Use the following command to compile the program with the -O1 optimization flag:*
```sh
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o swift.o swift.c
```
**Disassemble Object Files to View Assembly Code(in new terminal)**
*Generate Dump for -O1 Optimization*
```sh
riscv64-unknown-elf-objdump -d swift.o
```
*Minimize the assembly by using following code:*
```sh
riscv64-unknown-elf-objdump -d swift.o | less
```
![main program for O1 option](https://github.com/user-attachments/assets/63c34a23-919a-4741-91f9-ab9e48a13e4a)


**Run SPIKE Simulation**
*Run a compiled RISC-V program on the SPIKE simulator in non-debug mode.*
```sh
spike pk swift.o
```
*Invoke the debug mode of the SPIKE RISC-V simulator.*
```sh
spike -d pk swift.o
```
![compiling with O1 option](https://github.com/user-attachments/assets/257327e6-bb35-412f-92de-ce70c92736d0)


**Compile with -Ofast Optimization.**
*Use the following command to compile the program with the -Ofast optimization flag:*
```sh
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o swift.o swift.c
```
**Disassemble Object Files to View Assembly Code(in new terminal)**
*Generate Dump for -Ofast Optimization*
```sh
riscv64-unknown-elf-objdump -d swift.o
```
*Minimize the assembly by using following code:*
```sh
riscv64-unknown-elf-objdump -d swift.o | less
```
![main program for ofast option](https://github.com/user-attachments/assets/f5df539d-7170-4158-bf1b-b19240672da2)


**Run SPIKE Simulation**
*Run -O1 Binary in SPIKE*
```sh
spike pk swift.o
```
*Invoke the debug mode of the SPIKE RISC-V simulator*
```sh
spike -d pk swift.o
```
![compiling with Ofast option](https://github.com/user-attachments/assets/c67c0820-11ea-4aae-aa01-1edaae5b8e71)


**After(spike -d pk swift.o) Observe the Instructions:**

1)After loading, SPIKE initializes and displays the Program Counter (PC) and Stack Pointer (SP).

2)Press Enter repeatedly to step through the execution.

3)Each press displays the next instruction executed by the program.

4)The displayed instructions directly correspond to the C code of the main program, providing insights into the program's execution flow.
**Explanation of Key Commands and Options:**

1. spike:RISC-V simulator that runs RISC-V programs on a virtual machine.

2. pk:Proxy kernel that acts as a minimal runtime environment for RISC-V programs, handling system calls like I/O and memory management.

3. swift.o:The compiled RISC-V binary of your program (created using a RISC-V GCC compiler).

4. -d (for debugging):Debugging mode in SPIKE, allows stepping through the instructions and inspecting the program's behavior.

5. riscv64-unknown-elf-gcc:RISC-V GCC compiler used to compile the C program into a RISC-V object file (.o).

6. -O1, -Ofast:Compiler optimization flags:
      a.-O1: Basic optimizations for performance.
      b.-Ofast: Aggressive optimizations for maximum speed.

7. riscv64-unknown-elf-objdump:Disassembles RISC-V binaries to examine assembly code.

These tools together enable compiling, running, and debugging RISC-V programs on a simulated environment.

</details>

---

<details>
<summary><b>Task 3:</b> The goal is to analyze and categorize each of the provided instructions based on their type, whether it be R-type, I-type, or J-type, and then translate them into their respective 32-bit machine instruction codes. These instruction codes should be represented in the appropriate format, ensuring that each instruction is properly encoded according to the specific structure and opcode requirements of the given architecture. The result should provide a detailed mapping of the instructions to their corresponding binary code representations.</summary>

# Understanding RISC-V and Its Instruction Formats

## What is RISC-V?
RISC-V is an open-source Instruction Set Architecture (ISA) that enables developers to design processors tailored to specific applications. Based on Reduced Instruction Set Computer (RISC) principles, RISC-V represents the fifth generation of processors built on this concept. Its open and free nature means developers can utilize RISC-V without purchasing licenses, making it a compelling alternative to proprietary processor technologies.

## Instruction Formats in RISC-V
The instruction format of a processor defines how machine language instructions are structured for execution. These instructions are composed of binary data (0s and 1s), each segment providing details about data location and operations to be performed. In RISC-V, there are six primary instruction formats:

1. **R-format**
2. **I-format**
3. **S-format**
4. **B-format**
5. **U-format**
6. **J-format**
<img width="772" alt="instructions_types" src="https://github.com/user-attachments/assets/7ca6b3ea-bd59-4419-8410-1e14e40e911e" />


---

### 1. R-type Instruction
R-type (Register-type) instructions operate on registers rather than memory locations. These are used for arithmetic and logical operations. Each instruction is 32 bits and divided into six fields:

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| func3      | 3 bits| Specifies the type of operation       |
| rs1        | 5 bits| First source register                 |
| rs2        | 5 bits| Second source register                |
| func7      | 7 bits| Additional operation specification    |

#### Example: ADD r9, r2, r5
- **Operation:** Adds values in registers r2 and r5, storing the result in r9.
- **Field Breakdown:**

  - Opcode: `0110011`
  - rd (Destination): `r9` -> `01001`
  - rs1 (Source 1): `r2` -> `00010`
  - rs2 (Source 2): `r5` -> `00101`
  - func3: `000`
  - func7: `0000000`
- **32-bit Instruction:** `0000000_00101_00010_000_01001_0110011`


#### Example: XOR r10, r1, r4
- **Operation:** XOR operation between r1 and r4, result in r10.
- **Field Breakdown:**

  - Opcode: `0110011`
  - rd (Destination): `r10` -> `01010`
  - rs1 (Source 1): `r1` -> `00001`
  - rs2 (Source 2): `r4` -> `00100`
  - func3: `100`
  - func7: `0000000`
- **32-bit Instruction:** `0000000_00100_00001_100_01010_0110011`


#### Example: SLT r11, r2, r4
- **Operation:** Sets r11 to 1 if r2 < r4; otherwise, sets r11 to 0.
- **Field Breakdown:**

  - Opcode: `0110011`
  - rd (Destination): `r11` -> `01011`
  - rs1 (Source 1): `r2` -> `00010`
  - rs2 (Source 2): `r4` -> `00100`
  - func3: `010`
  - func7: `0000000`
- **32-bit Instruction:** `0000000_00100_00010_010_01011_0110011`

![r type](https://github.com/user-attachments/assets/33357c39-806e-4d2f-9158-cd204120dcd8)


---

### 2. I-type Instruction
I-type (Immediate-type) instructions use a register and an immediate (constant) value. These are typically used for load and immediate operations.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| func3      | 3 bits| Specifies the type of operation       |
| rs1        | 5 bits| Source register                       |
| imm[11:0]  | 12 bits| Immediate value                      |

#### Example: ADDI r12, r4, 5
- **Operation:** Adds immediate value 5 to the value in r4 and stores it in r12.
- **Field Breakdown:**
  - Opcode: `0010011`
  - rd (Destination): `r12` -> `01100`
  - rs1 (Source): `r4` -> `00100`
  - imm[11:0] (Immediate): `000000000101`
  - func3: `000`
- **32-bit Instruction:** `000000000101_00100_000_01100_0010011`

![i type](https://github.com/user-attachments/assets/76a06842-0672-46d8-b50e-c538c6f63c99)


---

### 3. S-type Instruction
S-type (Store-type) instructions store register values into memory locations.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rs1        | 5 bits| Base address register                 |
| rs2        | 5 bits| Source register                       |
| imm[11:5]  | 7 bits| Upper immediate value                  |
| imm[4:0]   | 5 bits| Lower immediate value                  |
| func3      | 3 bits| Specifies the type of operation       |

#### Example: SW r3, 2(r1)
- **Operation:** Stores the value in r3 into the memory at the address `r1 + 2`.
- **Field Breakdown:**
  - Opcode: `0100011`
  - rs1 (Base Address): `r1` -> `00001`
  - rs2 (Source): `r3` -> `00011`
  - imm[11:5] (Upper Immediate): `0000000`
  - imm[4:0] (Lower Immediate): `00010`
  - func3: `010`
- **32-bit Instruction:** `0000000_00011_00001_010_00010_0100011`

![s type](https://github.com/user-attachments/assets/a6210bc8-77c1-424d-a6e0-ada39b5189da)


---

### 4. B-type Instruction
B-type (Branch-type) instructions handle branching based on conditions.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rs1        | 5 bits| Source register 1                      |
| rs2        | 5 bits| Source register 2                      |
| imm[12|10:5|4:1|11] | 13 bits| Branch offset                      |
| func3      | 3 bits| Specifies the condition for branching |

#### Example: BNE r0, r1, 20
- **Operation:** Branches to the address `PC + 20` if r0 is not equal to r1.
- **Field Breakdown:**
  - Opcode: `1100011`
  - rs1: `r0` -> `00000`
  - rs2: `r1` -> `00001`
  - imm[12|10:5|4:1|11]: `0000010100`
  - func3: `001`
- **32-bit Instruction:** `0000000_00001_00000_001_10100_1100011`

#### Example: BEQ r0, r0, 15
- **Operation:** Branches to the address `PC + 15` if r0 equals r0 (always true).
- **Field Breakdown:**
  - Opcode: `1100011`
  - rs1: `r0` -> `00000`
  - rs2: `r0` -> `00000`
  - imm[12|10:5|4:1|11]: `000001111`
  - func3: `000`
- **32-bit Instruction:** `0000000_00000_00000_000_01111_1100011`

![b type](https://github.com/user-attachments/assets/31c67705-07f0-4d1d-86e0-2c0d8e3e2e78)

---

### 5. U-type Instruction
U-type (Upper Immediate) instructions load immediate data into the destination register.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| imm[31:12] | 20 bits| Upper immediate value                  |

![u type](https://github.com/user-attachments/assets/d5223eda-40fd-4418-8860-39f350330311)


---

### 6. J-type Instruction
J-type (Jump-type) instructions implement jump operations, often used for loops.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| imm[20|10:1|11|19:12] | 20 bits| Jump offset                        |

![j type](https://github.com/user-attachments/assets/f9841148-7b72-42c1-adea-3a9e2068d621)


---


This repository contains a list of 15 unique RISC-V instructions extracted from the assembly code along with their corresponding 32-bit instruction codes. These instructions cover different instruction formats, such as **U-type**, **I-type**, **J-type**, **B-type**, and **R-type**.


# RISC-V Instructions

This README contains a table of 23 unique RISC-V instructions, their machine codes, opcodes, formats, and instruction binaries for my assembly codes.

| Instruction                | Opcode  | Format | Machine Code | Instruction Binary                          |
|----------------------------|---------|--------|--------------|----------------------------------------------|
| addi sp, sp, -48           | 0010011 | I-type | 0xfff30313   | 11111111111100000011000000010011            |
| sd ra, 40(sp)              | 0100011 | S-type | 0x02113423   | 00000000001000010001000100010011            |
| li a5, 10                  | 0010011 | I-type | 0x00a00793   | 00000000000010100000011110010011            |
| sw a5, -24(s0)             | 0100011 | S-type | 0xfef42423   | 11111110111101000010010010010011            |
| addw a5, a4, a5            | 0110011 | R-type | 0x00f707bb   | 00000000011101000000000010010011            |
| mv a2, a4                  | 0110011 | R-type | 0x00070613   | 00000000000001110000000010010011            |
| mv a1, a5                  | 0110011 | R-type | 0x00078593   | 00000000000001110000101000010011            |
| lui a5, 0x21               | 0110111 | U-type | 0x000217b7   | 00000000000000100010011110110111            |
| jal ra, 1117c              | 1101111 | J-type | 0x7ad000ef   | 01111010110100000000000001110111            |
| subw a5, a4, a5            | 0110011 | R-type | 0x40f707bb   | 00000000111101000000000010010011            |
| and a5, a4, a5             | 0110011 | R-type | 0x00f777b3   | 00000000011101000000000010010011            |
| or a5, a4, a5              | 0110011 | R-type | 0x00f767b3   | 00000000011101000000000010010011            |
| xor a5, a4, a5             | 0110011 | R-type | 0x00f747b3   | 00000000011101000000000010010011            |
| slliw a5, a5, 0x1          | 0010011 | I-type | 0x0017979b   | 00000000000101110111000010010011            |
| sraiw a5, a5, 0x1          | 0010011 | I-type | 0x4017d79b   | 01000000000101110111000010010011            |
| sext.w a4, a4              | 0000011 | I-type | 0x0007071b   | 00000000000001110000000010010011            |
| bne a4, a5, 103c8          | 1100011 | B-type | 0x02f71063   | 00000000001011110001000001100011            |
| beq a4, a5, 103f8          | 1100011 | B-type | 0x02f70063   | 00000000001011110001000001100011            |
| bge a4, a5, 10428          | 1100011 | B-type | 0x02f75063   | 00000000001011110001000001100011            |
| blt a4, a5, 10458          | 1100011 | B-type | 0x02f74063   | 00000000001011110001000001100011            |
| j 10490                    | 1101111 | J-type | 0x0340006f   | 00000011001100000000000001101111            |
| addw a5, a4, a5            | 0110011 | R-type | 0x00f707bb   | 00000000011101000000000010010011            |
| beqz a5, 104e4             | 1100011 | B-type | 0x02078863   | 00000000001000110000000001100011            |

</details>

---
<details>
<summary> <b>Task 4:</b>This task involves simulating the RISC-V Core using the provided Verilog netlist and testbench. You will set up a simulation environment using tools like Icarus Verilog and GTKWave, run the simulation to verify the functional correctness of the core, and analyze output signals. Waveform snapshots of the executed instructions must be captured and uploaded to your GitHub repository along with a brief description, demonstrating your understanding of RISC-V functional simulation and verification.</summary> 
<br>

## 2. BLOCK DIAGRAM OF RISC-V RV32I
![image](https://user-images.githubusercontent.com/110079631/181293948-beb8622c-7696-4b06-b6c9-eeab9b8ab9d3.png)

## 3. INSTRUCTION SET OF RISC-V RV32I
![image](https://user-images.githubusercontent.com/110079631/181298133-60269bc2-01da-4b5c-8b42-69057b8dc15c.png)

# RISC-V Core Functional Simulation 
## 4. FUNCTIONAL SIMULATION

### 4.1 About iverilog and gtkwave
- Icarus Verilog is an implementation of the Verilog hardware description language.
- GTKWave is a fully featured GTK+ v1. 2 based wave viewer for Unix and Win32 which reads Ver Structural Verilog Compiler generated AET files as well as standard Verilog VCD/EVCD files and allows their viewing.

### 4.2 Installing iverilog and gtkwave

- **For Ubuntu**

 Open your terminal and type the following to install iverilog and GTKWave
 ```
 $   sudo apt get update
 $   sudo apt get install iverilog gtkwave
 ```

- **To clone the repository and download the netlist files for simulation , enter the following commands in your terminal.**

 ```
 $ git clone https://github.com/vinayrayapati/iiitb_rv32i
 $ cd iiitb_rv32i
 ```
- **To simulate and run the verilog code , enter the following commands in your terminal.**

```
$ iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
$ ./iiitb_rv32i
```
- **To see the output waveform in gtkwave, enter the following commands in your terminal.**

`$ gtkwave iiitb_rv32i.vcd`

### 4.3 The output waveform

 The output waveform showing the instructions performed in a 5-stage pipelined architecture.

## Instructions and Pipeline Details  

Below are the 15 instructions and their corresponding pipeline details:  

---

### 1. `add r6, r2, r1`  
**Purpose:** Add `r2` and `r1`, store the result in `r6`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `add` instruction.
  - IF_ID_NPC: Holds the next program counter value.
Decode Stage:
  - ID_EX_IR: Ensures the instruction is decoded.
  - ID_EX_A: Value of register `r2`.
  - ID_EX_B: Value of register `r1`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r2 + r1`.
  - EX_MEM_IR: Holds the `add` instruction.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r6`.
```

---

### 2. `sub r7, r1, r2`  
**Purpose:** Subtract `r2` from `r1`, store the result in `r7`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `sub` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_B: Value of register `r2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 - r2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r7`.
```

---

### 3. `and r8, r1, r3`  
**Purpose:** Perform bitwise AND between `r1` and `r3`, store the result in `r8`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `and` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_B: Value of register `r3`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 & r3`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r8`.
```

---

### 4. `or r9, r2, r5`  
**Purpose:** Perform bitwise OR between `r2` and `r5`, store the result in `r9`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `or` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r2`.
  - ID_EX_B: Value of register `r5`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r2 | r5`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r9`.
```

---

### 5. `xor r10, r1, r4`  
**Purpose:** Perform bitwise XOR between `r1` and `r4`, store the result in `r10`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `xor` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_B: Value of register `r4`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 ^ r4`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r10`.
```

---

### 6. `addi r12, r4, 5`  
**Purpose:** Add immediate value `5` to `r4`, store the result in `r12`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `addi` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r4`.
  - ID_EX_IMMEDIATE: Immediate value `5`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r4 + 5`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r12`.
```

---

### 7. `sw r3, r1, 2`  
**Purpose:** Store the value of `r3` into memory address `r1 + 2`.  
```markdown
Memory Access Stage:
  - EX_MEM_ALUOUT: Computed memory address (`r1 + 2`).
  - EX_MEM_B: Value of `r3` to store.
```

---

### 8. `lw r13, r1, 2`  
**Purpose:** Load word from memory address `r1 + 2` into `r13`.  
```markdown
Memory Access Stage:
  - MEM_WB_LMD: Value loaded from memory.
Write-Back Stage:
  - WB_OUT: Verifies the value is written to `r13`.
```

---

### 9. `beq r0, r0, 15`  
**Purpose:** Branch to PC + 15 if `r0 == r0` (always true).  
```markdown
Decode Stage:
  - BR_EN: High (branch taken).
Fetch Stage:
  - IF_ID_NPC: Updated program counter.
```

---

### 10. `add r14, r2, r2`  
**Purpose:** Add `r2` to itself, store the result in `r14`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `add` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r2`.
  - ID_EX_B: Value of register `r2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r2 + r2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r14`.
```

---

### 11. `bne r0, r1, 20`  
**Purpose:** Branch to PC + 20 if `r0 != r1`.  
```markdown
Decode Stage:
  - BR_EN: High if `r0 != r1`.
Fetch Stage:
  - IF_ID_NPC: Updated program counter.
```

---

### 12. `addi r12, r4, 5`  
**Purpose:** Add immediate value `5` to `r4`, store the result in `r12`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `addi` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r4`.
  - ID_EX_IMMEDIATE: Immediate value `5`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r4 + 5`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r12`.
```

---

### 13. `sll r15, r1, r2 (2)`  
**Purpose:** Perform logical left shift of `r1` by 2 (specified in `r2`), store the result in `r15`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `sll` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_SHAMT: Immediate shift value `2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 << 2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r15`.
```

---

### 14. `srl r16, r14, r2 (2)`  
**Purpose:** Perform logical right shift of `r14` by 2 (specified in `r2`), store the result in `r16`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `srl` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r14`.
  - ID_EX_SHAMT: Immediate shift value `2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r14 >> 2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r16`.
```


#### *Analysing the Output Waveform of various instructions*  
**```Instruction 1: ADD R6, R2, R1```**  
  
![add](https://github.com/user-attachments/assets/44851b1c-806a-4182-81ab-47af3cf725be)


**```Instruction 2: SUB R7, R1, R2```**  
  
![sub](https://github.com/user-attachments/assets/1104fc06-491a-4e9c-971c-8b51387bd2d6)


**```Instruction 3: AND R8, R1, R3```**  

![and](https://github.com/user-attachments/assets/ddeb5386-04ac-4ea7-a4ee-1e4d2968d2c9)


**```Instruction 4: OR R9, R2, R5```**  

![or](https://github.com/user-attachments/assets/c10ba03d-4f25-49f6-a1c4-b68dde3c1383)


**```Instruction 5: XOR R10, R1, R4```**  

![xor](https://github.com/user-attachments/assets/ed7a6299-92a0-4ed5-b812-97050af83c54)


**```Instruction 6: SLT R1, R2, R4```**  

![slt](https://github.com/user-attachments/assets/d463ee88-c39f-41c3-a4b3-31ee670da5e3)


**```Instruction 7: ADDI R12, R4, 5```**  

![addi](https://github.com/user-attachments/assets/4581b98f-e445-4776-8700-68b03f26131f)


**```Instruction 8: BEQ R0, R0, 15```**  
  
![BEQ](https://github.com/user-attachments/assets/02bbbd72-6d84-4595-a0af-5157524ccdf8)

 
**```Instruction 9:sw r3,r1,2```**

![sw](https://github.com/user-attachments/assets/65fd8529-9b5e-4572-a796-c370ab6b7051)

  
**```Instruction 10:lw r13,r1,2```**  

![lw](https://github.com/user-attachments/assets/58c72387-6ca2-4e15-a7c3-ca68f906ee3f)

**``` Full 5-stage instruction pipeline and pc-increment description Waveform```**

![5-stage instruction pipeline and pc-increment description Waveform](https://github.com/user-attachments/assets/2bce01e3-3405-432d-a1d6-ec359d45d560)



</details>

---

<details>
<summary> <b>Task 5:</b>An automatic light system is an intelligent setup designed to control lighting based on the presence or absence of individuals within its detection range. The system utilizes an IR sensor to continuously monitor its surroundings for any movement. When motion is detected, the system automatically turns OFF the LED, providing illumination. Additionally, to indicate the presence of movement. If no motion is detected for a certain period, the LED turns ON, ensuring process coninuation. This system is widely used in home automation, security lighting, Protected Area, Military surveillance, safety.</summary> 
<br>

# Automatic Light System using VSDSquadron Mini RISC-V Board

## Project Overview
An **automatic light system** is a setup designed to automatically control the lighting based on the presence or absence of individuals within its detection range. This system will also give an indication of motion detected by stoping the Blinking LED.

### Features:
✅ **Automatic Light Control**: Lights up based on motion detection  
✅ **Motion Indication**: LED blinks OFF when motion is detected   
✅ **Security and Automation**: Enhances convenience and safety  

---

## Required Components  
| Component | Quantity | Description |
|-----------|----------|-------------|
| **VSDSquadron Mini Board** | 1 | RISC-V SoC-based development board |
| **IR Sensor** | 1 | Detects motion based on infrared radiation |
| **LEDs** | 1 | Indicates motion detection |
| **Breadboard** | 1 | For circuit connections |
| **USB Cable** | 1 | Power and programming |
| **Jumper Wires** | - | For making connections |

---

## Pin Connections  

| **Component** | **Board Pin** | **Purpose** |
|--------------|-------------|-------------|
| **VCC of IR Sensor** | **3.2V** | Power supply |
| **GND of IR Sensor** | **GND** | Ground connection |
| **OUT of IR Sensor** | **Pin 4** | Motion detection signal |
| **LED** | **Pin 6** | Indicates motion detected |


## Pin connection diagram

![Automatic-light-system circuit diagram](https://github.com/user-attachments/assets/bfd0cca4-c559-4201-921b-378f1be785f1)

---
## breadboard connections

![physical connections on breadboard](https://github.com/user-attachments/assets/989f1c29-0fc7-4bb4-a938-f870a1d14c26)

---
## Working  
- The **IR sensor** is placed in a location where it can detect motion within its range.
- It continuously monitors infrared radiation for any changes caused by movement.
- When an individual enters the detection range, the IR sensor sends a signal to the microcontroller.
- Upon detecting motion, the system turns OFF the LED and blinks on when no motion Detected which indicates process will continue.

---
</details>

---


<details>
<summary> <b>Task 6:</b>The Automatic Light System uses the VSDSquadron Mini RISC-V Board, an IR sensor, and an LED for motion-based lighting control. The IR sensor detects movement, triggering the LED to blink three times before staying ON. If no motion is detected, the LED turns OFF. This system is ideal for home automation, security, offering smart, hands-free lighting control.</summary> 
<br>

## Project Implementation  

### Steps to Implement:  
1. **Hardware Setup:**  
   - Connect the **IR sensor** to the board's GPIO pins.  
   - Wire an **LED** to indicate motion detection.  
   - Use a **breadboard** for easy prototyping and secure connections.  

2. **Software Development:**  
   - Write the **C firmware** to read the IR sensor output.  
   - Configure the GPIO pins for input (IR sensor) and output (LED).  
   - Implement logic to **blink the LED three times** upon detecting motion.  
   - Keep the LED **OFF** as long as movement is detected.  
   - Turn the LED **ON** after a delay when no movement is present.  

3. **Compilation & Upload:**  
   - Compile the code using a **RISC-V compatible toolchain**.  
   - Flash the program onto the **VSDSquadron Mini Board**.  

4. **Testing & Debugging:**  
   - Test the system in different lighting conditions.  
   - Adjust sensor sensitivity if needed.   

### Expected Output:  
- If motion is detected for a certain period, the LED automatically **turns OFF**. 
- If no motion is detected for a certain period, the LED automatically **turns ON**.  

This implementation ensures **automatic lighting control**, **energy efficiency**, and **security enhancements** for various applications.
---

## Code Implementation  
```c
#include <ch32v00x.h>
#include <debug.h>

void GPIO_Config(void)
{
    GPIO_InitTypeDef GPIO_InitStructure = {0};
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE);
    
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_4;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU;
    GPIO_Init(GPIOD, &GPIO_InitStructure);
    
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_6;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOD, &GPIO_InitStructure);
}

int main(void)
{
    uint8_t IR = 0;
    uint8_t set = 1;
    uint8_t reset = 0;
    uint8_t a = 0;
    
    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_2);
    SystemCoreClockUpdate();
    Delay_Init();
    GPIO_Config();
    
    while (1)
    {
        IR = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_4);
        if (IR == 1)
        {
            for (a = 0; a < 3; a++)
            {
                GPIO_WriteBit(GPIOD, GPIO_Pin_6, set);
                Delay_Ms(200);
                GPIO_WriteBit(GPIOD, GPIO_Pin_6, reset);
                Delay_Ms(100);
            }
        }
    }
}
```
## Applications
✅ **Security Lighting**: These systems can be used for security lighting in outdoor spaces, such as gardens, driveways, and pathways, to deter intruders and provide visibility at night.
✅ **Home Automation**: Automatic light systems can be installed in homes, particularly in areas such as hallways, staircases, and bathrooms, where lights need to be turned on/off based on occupancy.
✅ **Accessibility**: These systems can improve accessibility for individuals with disabilities by providing automatic illumination in response to their movement.


# Conclusion
During the VSD Squadron mini Internship, I embarked on a journey exploring various aspects of VLSI system design on the RISC-V architecture, alongside open-source EDA tools.

</details>
---
