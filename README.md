![Screenshot 2025-01-13 095822](https://github.com/user-attachments/assets/8a17b4d6-d073-4cc9-96b9-de92e7f0e18e)# samsung-rscv![WhatsApp Image 2025-01-03 at 1 09 17 PM](https://github.com/user-attachments/assets/87feb793-6d4f-4bb1-a1dc-e5d0eda69ca1)
![WhatsApp Image 2025-01-03 at 1 14 26 PM](https://github.com/user-attachments/assets/6221d487-2885-4584-ba84-771e013f2a71)
# This project is focused on the development and integration of RISC-V architecture with Samsung's technology stack. The RISC-V architecture is an open-source instruction set architecture (ISA) designed to be modular, customizable, and extensible. This project aims to explore, contribute to, and optimize RISC-V cores and related systems for a variety of use cases, including mobile devices, IoT, and high-performance computing solutions.
## task2:![O1](https://github.com/user-attachments/assets/c60b6145-66f7-4788-b5e0-86cd6c5b1e62)
- ![Ofast](https://github.com/user-attachments/assets/6519e3e7-2d47-4037-a938-93ecd35a8e1b)
- ![spike](https://github.com/user-attachments/assets/ab265834-aac4-4254-be41-8b9aeee6baaa)
  ![WhatsApp Image 2025-01-17 at 21 01 35_93460aec](https://github.com/user-attachments/assets/9bc968e0-2cfd-44f4-ace2-e06742f35312)
![WhatsApp Image 2025-01-17 at 21 02 45_f5d2ad52](https://github.com/user-attachments/assets/481bc67b-26bc-4d50-b184-77d20cf9383d)
##task3
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
## J Instruction
## Instruction: j 15d24
> This instruction jumps to the specified target address (15d24).
> 
 * Type: J-Type (Jump)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for J: 1101111
   * imm[20|10:1|11:19]: 15d24 (20-bit immediate value representing the target address)
32-bit Instruction Encoding:
 * Binary Representation:
   1101111 00000 00000000000 1111011010010100

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
- ## SD Instruction
#  Instruction: sd s0, 16(sp)

This repository provides a breakdown of the MIPS instruction `sd s0, 16(sp)`.

## Instruction Details

* **Type:** I-Type (Immediate)
* **Opcode:** 111111 (binary for 0x2F)
* **rs (sp):** 29 (Register number for $sp)
* **rt (s0):** 16 (Register number for $s0)
* **offset:** 16 (Immediate offset, a 16-bit signed integer)

## 32-bit Instruction Encoding

111111 00000 10000 11111 00000 00001000
## BEQZ Instruction
## Instruction: beqz a5, 10200
> This instruction branches to the specified offset (10200) if the value in register a5 is equal to zero.
> 
 * Type: I-Type (Immediate)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for BEQZ: 1100011
   * rs1 (a5): 15 (Register number for a5)
   * rs2: 0 (Not used in BEQZ)
   * imm: 10200 (Immediate value, which is a 12-bit signed integer)
32-bit Instruction Encoding:
 * Binary Representation:
   1100011 000 15 0000000 0111110011010000
## CLW Instruction
#  Instruction:Clw a3, 12(sp)
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
## ADDIW Instruction
## Instruction:addiw a3, a3, 1

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
## BLEZ Instruction
## Instruction: blez a3, 10140
> This instruction branches to the specified offset (10140) if the value in register a3 is less than or equal to zero.
> 
 * Type: I-Type (Immediate)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for BLEZ: 1100011
   * rs1 (a3): 9 (Register number for a3)
   * rs2: 0 (Not used in BLEZ)
   * imm: 10140 (Immediate value, which is a 12-bit signed integer)
32-bit Instruction Encoding:
 * Binary Representation:
   1100011 000 9 0000000 0111110010100000
## LBU Instruction
## Instruction: lbu a5, 1944(gp)
> This instruction loads an unsigned byte of data from the memory address calculated by adding the immediate value (1944) to the value in register gp (global pointer) and stores it in register a5.
> 
 * Type: I-Type (Immediate)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for LBU: 0001000
   * funct3: 000 (for lbu)
   * rs1 (gp): 3 (Register number for gp)
   * rd (a5): 15 (Register number for a5)
   * imm: 1944 (Immediate value, which is a 12-bit signed integer)
32-bit Instruction Encoding:
 * Binary Representation:
   0001000 000 3 15 0111011100000000
#  Instruction:auipc gp, 0x1e

**Type:** U-Type (Immediate)

**Label:** gp (destination register is x28)

**Details:**

**Opcode for AUIPC:** 0111111 (binary for AUIPC)
**rd (gp):** 28 (Register number for gp, which corresponds to x28)
**imm:** 0x1e (Immediate value, represented as a 20-bit unsigned integer)

32-bit Instruction Encoding:
### Binary Representation:
00000000000000000000  11100 0111111
## SUB Instruction
## Instruction: sub a2, a2, a0
> This instruction subtracts the value in register a0 from the value in register a2 and stores the result in register a2.
> 
 * Type: R-Type (Register)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for SUB: 0000000
   * funct3: 000 (for sub)
   * rd (a2): 6 (Register number for a2)
   * rs1 (a2): 6 (Register number for a2)
   * rs2 (a0): 0 (Register number for a0)
   * funct7: 0100000 (for sub)
32-bit Instruction Encoding:
 * Binary Representation:
   0000000 6 000 6 0 0100000
## ANDI Instruction
## Instruction: andi a4, a5, 1
> This instruction performs a bitwise AND operation between the value in register a5 and the immediate value 1, and stores the result in register a4.
> 
 * Type: I-Type (Immediate)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for ANDI: 0011001
   * funct3: 111 (for andi)
   * rd (a4): 10 (Register number for a4)
   * rs1 (a5): 15 (Register number for a5)
   * imm: 1 (Immediate value, which is a 12-bit signed integer)
32-bit Instruction Encoding:
 * Binary Representation:
   0011001 111 15 10 0000000000000001
## BNE Instruction
## Instruction: bne a3, a5, 10100
> This instruction branches to the specified offset (10100) if the values in registers a3 and a5 are not equal.
> 
 * Type: I-Type (Immediate)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for BNE: 1100011
   * rs1 (a3): 9 (Register number for a3)
   * rs2 (a5): 15 (Register number for a5)
   * imm: 10100 (Immediate value, which is a 12-bit signed integer)
32-bit Instruction Encoding:
 * Binary Representation:
   1100011 000 9 15 0111110100000000
   ## LD Instruction
   ## Instruction: ld a5, 88(a0)

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
 ## JAL Instruction
## Instruction: jal ra, 15dd0
> This instruction jumps to the specified target address (15dd0) and stores the address of the next instruction (the return address) in register ra (register 1).
> 
 * Type: U-Type (Immediate)
 * Label: None (it's a direct instruction without a label)
 * Details:
   * Opcode for JAL: 1101111
   * rd (ra): 1 (Register number for ra)
   * imm[20|10:1|11:19]: 15dd0 (20-bit immediate value representing the target address)
32-bit Instruction Encoding:
 * Binary Representation:
   1101111 00001 00000000000 1111011011010000
