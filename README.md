# 8-Bit-ALU-using-Verilog-code-in-Vivado


Here’s a technical description you can include in the `README.md` file under a **"Technical Description"** section:

---

### 🔧 Technical Description

This project implements an **8-bit Arithmetic Logic Unit (ALU)** in Verilog HDL. The ALU accepts two 8-bit input operands (`A` and `B`) and performs a variety of arithmetic and logical operations based on a 4-bit control signal (`ALU_Sel`). The output is an 8-bit result (`ALU_Out`) and a 1-bit `Zero` flag to indicate if the result is zero.

**Supported Operations:**

| ALU\_Sel | Operation   | Description              |     |
| -------- | ----------- | ------------------------ | --- |
| 0000     | Addition    | `A + B`                  |     |
| 0001     | Subtraction | `A - B`                  |     |
| 0010     | AND         | `A & B`                  |     |
| 0011     | OR          | \`A                      | B\` |
| 0100     | XOR         | `A ^ B`                  |     |
| 0101     | NOT         | `~A`                     |     |
| 0110     | Increment A | `A + 1`                  |     |
| 0111     | Decrement A | `A - 1`                  |     |
| 1000     | Pass B      | `B`                      |     |
| 1001     | Multiply    | `A * B` (limited result) |     |

**Inputs:**

* `A` \[7:0] – First operand
* `B` \[7:0] – Second operand
* `ALU_Sel` \[3:0] – Control signal to select the operation

**Outputs:**

* `ALU_Out` \[7:0] – Result of the selected operation
* `Zero` – Flag set to 1 if `ALU_Out == 0`, else 0

**File Structure:**

* `alu.v` – Main ALU module
* `alu_tb.v` – Testbench to verify functionality
* `README.md` – Project description and usage instructions

**Simulation:**
The testbench runs a series of operations, displays output values for each operation, and verifies correctness through waveform analysis or console output in tools like ModelSim or Vivado.

