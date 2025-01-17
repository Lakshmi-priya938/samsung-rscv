![Screenshot 2025-01-13 095822](https://github.com/user-attachments/assets/8a17b4d6-d073-4cc9-96b9-de92e7f0e18e)# samsung-rscv![WhatsApp Image 2025-01-03 at 1 09 17 PM](https://github.com/user-attachments/assets/87feb793-6d4f-4bb1-a1dc-e5d0eda69ca1)
![WhatsApp Image 2025-01-03 at 1 14 26 PM](https://github.com/user-attachments/assets/6221d487-2885-4584-ba84-771e013f2a71)
# This project is focused on the development and integration of RISC-V architecture with Samsung's technology stack. The RISC-V architecture is an open-source instruction set architecture (ISA) designed to be modular, customizable, and extensible. This project aims to explore, contribute to, and optimize RISC-V cores and related systems for a variety of use cases, including mobile devices, IoT, and high-performance computing solutions.
## task2:![O1](https://github.com/user-attachments/assets/c60b6145-66f7-4788-b5e0-86cd6c5b1e62)
- ![Ofast](https://github.com/user-attachments/assets/6519e3e7-2d47-4037-a938-93ecd35a8e1b)
- ![spike](https://github.com/user-attachments/assets/ab265834-aac4-4254-be41-8b9aeee6baaa)
  ![WhatsApp Image 2025-01-17 at 21 01 35_93460aec](https://github.com/user-attachments/assets/9bc968e0-2cfd-44f4-ace2-e06742f35312)
![WhatsApp Image 2025-01-17 at 21 02 45_f5d2ad52](https://github.com/user-attachments/assets/481bc67b-26bc-4d50-b184-77d20cf9383d)
## LUI Instruction

### Instruction: `lui a0, 0×2b`

> The `lui` (Load Upper Immediate) instruction is used to load a 20-bit immediate value into the upper 20 bits of a register and belongs to the *U-type* instruction set.

- **Type:** U-Type (Upper Immediate)
- **Label:** None (it's a direct instruction without a label)

- **Details:**
  - **Opcode for LUI:** 0110111
  - **funct3:** 000 (for lui)
  - **rd (a0):** 10 (Register number for a0)
  - **imm:** 0x2b000 (Immediate value, shifted left by 12 bits to occupy the upper 20 bits)

### 32-bit Instruction Encoding:

- **Binary Representation:**101010110000 01010 000 000000000000 0110111
## ADDI Instruction

### Instruction: `addi sp, sp, -32`

> All the arithmetic and logical operations are performed using *I-type instruction format*, hence this instruction belongs to the I-type instruction set.

- **Type:** I-Type (Immediate)
- **Label:** None (This is a direct instruction without any labels)

- **Details:**
  - **Opcode for ADDI:** 0010011
  - **funct3:** 000 (for addi)
  - **rd (sp):** 29 (Register number for sp)
  - **rs1 (sp):** 29 (Register number for sp)
  - **imm:** -32 (Immediate value, which is a 12-bit signed integer encoded as 0xFFFFFFE0)

### 32-bit Instruction Encoding:

- **Binary Representation:**001000 11101 11101 FFFFFFE0
## SD Instruction

### Instruction: `sd ra, 24(sp)`

> The `sd` (Store Double) instruction is used to store a 64-bit value from a register into memory and belongs to the *S-type* instruction set.

- **Type:** S-Type (Store)
- **Label:** None (it's a direct instruction without a label)

- **Details:**
  - **Opcode for SD:** 0100011
  - **funct3:** 011 (for sd)
  - **rs2 (ra):** 1 (Register number for ra)
  - **rs1 (sp):** 2 (Register number for sp)
  - **imm:** 24 (Immediate value, which is a 12-bit signed integer)

### 32-bit Instruction Encoding:

- **Binary Representation:**111111 00000 11111 11111 00000 00011000
# MIPS Instruction: sd s0, 16(sp)

This repository provides a breakdown of the MIPS instruction `sd s0, 16(sp)`.

## Instruction Details

* **Type:** I-Type (Immediate)
* **Opcode:** 111111 (binary for 0x2F)
* **rs (sp):** 29 (Register number for $sp)
* **rt (s0):** 16 (Register number for $s0)
* **offset:** 16 (Immediate offset, a 16-bit signed integer)

## 32-bit Instruction Encoding

111111 00000 10000 11111 00000 00001000
# MIPS Instruction: addi a1, sp, 12

This repository provides a breakdown of the MIPS instruction `addi a1, sp, 12`.

## Instruction Details

* **Type:** I-Type (Immediate)
* **Opcode:** 0010011 
* **funct3:** 000 (for addi)
* **rd (a1):** 11 (Register number for a1)
* **rs1 (sp):** 29 (Register number for sp)
* **imm:** 12 (Immediate value, a 12-bit signed integer)

## 32-bit Instruction Encoding

0010011 11101 01011 000 00000 000000000011
# MIPS Instruction:Clw a3, 12(sp)
**Type:** I-Type (Immediate)

**Label:** None (it's a direct instruction without a label)

**Details:**

**Opcode for LW:** 0000011 (binary for opcode 0x23)
**funct3:** 010 (for lw)
**rd (a3):** 11 (Register number for $a3)
**rs1 (sp):** 29 (Register number for $sp)
**imm:** 12 (Immediate offset, a 12-bit signed integer)
### 32-bit Instruction Encoding:

0000011 11101 01011 010 00000 000000001100
# MIPS Instruction:addiw a3, a3, 1

**Type:** I-Type (Immediate)

**Label:** None (it's a direct instruction without a label)

Details:

**Opcode for ADDIW:** 0011011 (binary for opcode 0x3)
**funct3 for ADDIW:** 000 (for addiw)
**rd (a3):** 11 (Register number for $a3)
**rs1 (a3):** 11 (Register number for $a3)
**imm:** 1 (Immediate value, a 12-bit signed integer)

### 32-bit Instruction Encoding:
Binary Representation:
0011011 01011 01011 000 00000 000000000001
# MIPS Instruction:li s0, 0

**Type:** I-Type (Immediate)

**Label:** None (it's a direct instruction without a label)

**Details:**

**Opcode for LI:** 0010011 (This is the opcode for I-type instructions like addi, li, etc.)
**funct3:** 000 (For the addi instruction, used with li as well)
**rd (s0):** 8 (Register number for s0)
**rs1:** N/A (There is no second register involved in this instruction)
**imm:** 0 (Immediate value, which is a 12-bit signed integer)

32-bit Instruction Encoding:
### Binary Representation:
000000000000 00000 000 01000 0010011li s0, 0
# MIPS Instruction:mv a1, s0

**Type:** I-Type (Immediate)

**Label:** None (it's a direct instruction without a label)

**Details:**

**Opcode for MV:** 0010011 (The opcode for I-type instructions, similar to addi)
**funct3:** 000 (For the addi instruction, used in mv as well)
**rd (a1):** 11 (Register number for a1)
**rs1 (s0):** 8 (Register number for s0)
**imm:** 0 (Immediate value, indicating no change to the value being moved)

### 32-bit Instruction Encoding:
Binary Representation:

000000000000 01000 000 01011 0010011
# MIPS Instruction:auipc gp, 0x1e

**Type:** U-Type (Immediate)

**Label:** gp (destination register is x28)

**Details:**

**Opcode for AUIPC:** 0111111 (binary for AUIPC)
**rd (gp):** 28 (Register number for gp, which corresponds to x28)
**imm:** 0x1e (Immediate value, represented as a 20-bit unsigned integer)

32-bit Instruction Encoding:
### Binary Representation:
00000000000000000000  11100 0111111
auipc a2, 0x1e
 

**Type:** U-Type (Upper Immediate)
   **Label:** None (it's a direct instruction without a label)
   **Details:**
   **Opcode for AUIPC:** 0000111
     **rd (a2):** 010 (Register number for a2)
     **imm[31:12]:** 0x1e (Immediate value, which is a 20-bit unsigned integer)

32-bit Instruction Encoding:
 ### Binary Representation: 0000111 010 00000000000000000011110 
 # MIPS Instruction:LI a1, 0 

**Type:** I-Type (Immediate)
**Label:** None (it's a direct instruction without a label)
**Details:**
  **Opcode for LI:** 0010011
  **funct3:** 000 (for addi)
  **rd (a1):** 011 (Register number for a1)
**rs1 (implicit):** 00000 (Zero register, not explicitly specified)
  **imm:** 000000000000 (Immediate value, which is a 12-bit signed integer)

32-bit Instruction Encoding:
 ### Binary Representation: 0010011 011 00000 000000000000
 # MIPS Instruction:auipc s0, 0x1d

**Type:** U-Type (Upper Immediate)
**Label:** None (it's a direct instruction without a label)
**Details:**
**Opcode for AUIPC:** 0000111
**rd (s0):** 01100 (Register number for s0)
**imm[31:12]:** 0x1d (Immediate value, which is a 20-bit unsigned integer)
32-bit Instruction Encoding:
**Opcode for AUIPC:** 0000111
   **rd (s0):** 01100
   **imm[31:12]:** 00000000000000011101
   ### Binary Representation: 0000111 01100 00000000000000011101
   # MIPS Instruction: ld a5, 88(a0)

**Type:** I-Type (Immediate)

**Label:** None (it's a direct instruction without a label)

**Details:**

**Opcode for LD:** 0000011
**funct3:** 011 (for ld)
**rd (a5):** 15 (Register number for a5)
**rs1 (a0):** 10 (Register number for a0)
**imm:** 88 (Immediate value, which is a 12-bit unsigned integer)

32-bit Instruction Encoding:
### Binary Representation:
0000011 01010 01111 0000000001011000
 # MIPS Instruction:auipc ti, 0x0

**Type:** U-Type (Upper Immediate)

**Label:** None (it's a direct instruction without a label)

**Details:**

**Opcode for AUIPC:** 0010111
**rd (ti):** 28 (Register number for ti in RISC-V)
**imm:** 0x0 (Immediate value, which is a 20-bit unsigned integer)

32-bit Instruction Encoding:
### Binary Representation:
0010111 00000 11100 0000000000000000
