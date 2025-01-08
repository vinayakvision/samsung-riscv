# samsung-riscv
The program focuses on the RISC-V architecture and leverages open-source tools to educate participants about VLSI chip design and RISC-V. The internship is led by Kunal Ghosh Sir.

# Basic Details

Name: Vinayak Venkappa Pujeri

College: Vidyavardhaka College of Engineering

Email ID: vision.vinayak12@gmail.com

GitHub Profile: Samratvinayak

LinkedIN Profile: Samratvinayak

# Task 1: Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler

## C Language based LAB
## C and RISC-V Based Labs

This repository demonstrates the processes involved in compiling C programs and generating assembly code using both a standard GCC compiler and a RISC-V GCC compiler. It includes comprehensive steps and explanations to guide users through each stage of the compilation and debugging workflow.

### C Language-Based Lab

#### Steps to Compile a .c File on Your Machine:

1. Open the bash terminal and navigate to the directory where you want to create your file.
2. Use the following command to create and edit a new .c file:
   ```sh
   leafpad sum1ton.c


#### Steps to Compile a .c File on our Machine:
 ```sh
 gcc sum1ton.c
 ./a.out
```

 
 ## Compilation and execution complete.
 
![2](https://github.com/user-attachments/assets/5363e456-21a1-498f-b360-5f5d66a58029)
)
### RISC-V Based Lab

#### Steps to Compile Using RISC-V GCC Compiler:
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

### Explanation of Key Commands and Options: 
1. -mabi=lp64: Specifies the Application Binary Interface (ABI) for 64-bit integers, pointers, and long data types, suitable for 64-bit RISC-V architecture.

2. -march=rv64i: Indicates the 64-bit RISC-V base integer instruction set architecture.

3. -O1: Enables basic optimization for better performance without significantly increasing compilation time.

4. -Ofast: Optimize the code aggressively for the best possible speed.

5. riscv64-unknown-elf-objdump: A tool for disassembling RISC-V binaries to examine the code structure and debug it effectively.
