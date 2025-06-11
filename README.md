# ComputerArchitecture_Divider

This section of the project implements a **32-bit hardware divider** using RTL (Register Transfer Level) modeling and is designed in **Logisim-Evolution**. The divider performs integer division and outputs both the quotient and the remainder.

### 🧾 Problem Description

Design a sequential circuit that divides a 32-bit dividend by a 32-bit divisor. The operation is triggered by a `start` signal and should complete in a finite number of clock cycles, after which a `done` signal is raised to indicate completion.

The system should be built using **Logisim-Evolution** and optionally described in RTL.

---

### ⚙️ Inputs and Outputs

| Signal     | Width    | Description                         |
|------------|----------|-------------------------------------|
| `dividend` | 32 bits  | Dividend for the division           |
| `divisor`  | 32 bits  | Divisor for the division            |
| `start`    | 1 bit    | Starts the division when set to 1   |
| `clk`      | 1 bit    | Clock signal                        |
| `quotient` | 32 bits  | Output: result of the division      |
| `remainder`| 32 bits  | Output: remainder of the division   |
| `done`     | 1 bit    | Goes high when operation is complete|

---

### 🏗️ Implementation Requirements

- The divider must perform the operation **after `start` is set**, and assert the `done` signal once the result is available.
- A **flowchart or FSM** is used to guide RTL development.
- Designed and tested in **Logisim-Evolution**.
- The output must be visible after a number of clock cycles and only after `done = 1`.

---

### 🧪 Testing & Evaluation

The implementation is tested using a provided Verilog testbench and synthesis script.

Run the following in your terminal:

```bash
./synth_valid.sh schematic.circ HW2/tb2.v
