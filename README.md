
# samsung-riscv
The program focuses on the RISC-V architecture and leverages open-source tools to educate participants about VLSI chip design and RISC-V. The internship is led by Kunal Ghosh Sir.

# Basic Details

**Name:** Vinayak Venkappa Pujeri

**College:** Vidyavardhaka College of Engineering

**Email ID:** vision.vinayak12@gmail.com / vinayakpujeri2047@gmail.com

**GitHub Profile:** vinayakvision

**LinkedIN Profile:** vinayakvision

<details>
<summary> <b>Task 1:</b></summary> 
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


<details>
<summary> <b>Task 1:</b></summary> 
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
![main program for O1 option](https://github.com/user-attachments/assets/8acff41d-ac85-413f-a537-5724c174618c)

**Run SPIKE Simulation**
*Run a compiled RISC-V program on the SPIKE simulator in non-debug mode.*
```sh
spike pk swift.o
```
*Invoke the debug mode of the SPIKE RISC-V simulator.*
```sh
spike -d pk swift.o
```
![compiling with O1 option](https://github.com/user-attachments/assets/222192e6-ca90-4749-8b50-bf4078001b0d)

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
![main program for ofast option](https://github.com/user-attachments/assets/66bbf42c-0593-4fbf-8f7f-c567b7d67276)

**Run SPIKE Simulation**
*Run -O1 Binary in SPIKE*
```sh
spike pk swift.o
```
*Invoke the debug mode of the SPIKE RISC-V simulator*
```sh
spike -d pk swift.o
```
![compiling with Ofast option](https://github.com/user-attachments/assets/a32a1593-88ae-45e8-a658-50e4cc559e86)

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
