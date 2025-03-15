 Combinational Circuits - Multiplexer (MUX) and Demultiplexer (DEMUX)

### Concept Overview
Combinational circuits are logic circuits whose outputs depend only on the current input values. MUX and DEMUX are essential combinational circuits widely used in data routing and communication systems.

### Detailed Explanation

#### ✅ Multiplexer (MUX)
- **Definition:** A MUX selects one input from multiple data inputs based on control (select) signals and forwards it to the output.
- **Symbol:** Shown as a box with multiple data inputs, select lines, and one output.
- **Boolean Expression for 4:1 MUX:** `Y = (I0 • ~S1 • ~S0) + (I1 • ~S1 • S0) + (I2 • S1 • ~S0) + (I3 • S1 • S0)`
- **Truth Table (4:1 MUX):**

| S1 | S0 | Output |
|:--:|:--:|:--------|
|  0 |  0 | I0       |
|  0 |  1 | I1       |
|  1 |  0 | I2       |
|  1 |  1 | I3       |

**Example Application:** Used in data selection, communication systems, and arithmetic circuits.

#### ✅ Demultiplexer (DEMUX)
- **Definition:** A DEMUX takes a single input and routes it to one of several outputs based on control (select) signals.
- **Symbol:** Shown as a box with one data input, select lines, and multiple outputs.
- **Boolean Expression for 1:4 DEMUX:**
  - `Y0 = D • ~S1 • ~S0`
  - `Y1 = D • ~S1 • S0`
  - `Y2 = D • S1 • ~S0`
  - `Y3 = D • S1 • S0`

- **Truth Table (1:4 DEMUX):**

| S1 | S0 | Y0 | Y1 | Y2 | Y3 |
|:--:|:--:|:--:|:--:|:--:|:--:|
|  0 |  0 |  1 |  0 |  0 |  0 |
|  0 |  1 |  0 |  1 |  0 |  0 |
|  1 |  0 |  0 |  0 |  1 |  0 |
|  1 |  1 |  0 |  0 |  0 |  1 |

**Example Application:** Used in data distribution, memory decoding, and signal routing.



### Code Explanation
- **`assign` Statements:** Implements data selection logic for both MUX and DEMUX.
- **`$monitor` Task:** Displays data values, select signals, and corresponding outputs.
- **Test Cases:** Tests all combinations of select signals for both circuits.

### Execution Steps
1. Copy the Verilog code into your simulator (e.g., ModelSim, Xilinx Vivado, etc.).
2. Compile and run the code.
3. Verify that the outputs match the expected truth table values.

### Real-World Example for Practice
- Design a **4-bit ALU** that performs AND, OR, ADD, and SUBTRACT operations using a 4:1 MUX.



