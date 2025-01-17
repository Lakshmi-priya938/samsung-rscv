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
## Instruction: SD s0, 16(sp) ### Type - I-Type (Immediate) ### Label - None (it's a direct instruction without a label) ### Details - **Opcode for SD**: 111111 (binary for opcode 0x2F) - **rs (sp)**: 29 (Register number for $sp) - **rt (s0)**: 16 (Register number for $s0) - **Offset**: 16 (Immediate offset, a 16-bit signed integer) ### 32-bit Instruction Encoding - **Binary Representation**: `111111 00000 10000 11111 00000 00001000`


