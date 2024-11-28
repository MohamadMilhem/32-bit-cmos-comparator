# Optimized 32-Bit Comparator Design

## Overview
This project implements a high-performance **32-bit comparator** using **prefix adder (CLA) logic** and a hierarchical tree structure. The design achieves **O(log n) latency**, optimizing speed and efficiency for digital systems requiring minimal delays. It is particularly suited for applications like sorting, signal processing, and multiprocessing.

---

## Features
1. **Efficient Comparison**:
   - Determines if one 32-bit binary number is greater than, less than, or equal to another.
   - Utilizes a divide-and-conquer approach for efficient computation.

2. **Key Components**:
   - **Recursive Carry Computation**: Calculates the final carry/borrow bit to derive comparison results.
   - **Tree Architecture**: Processes sub-segments independently and combines results for optimal speed.

3. **Performance Benefits**:
   - Reduces complexity by eliminating the need for carry computation at every bit position.
   - Achieves low latency and high throughput.

---

## Architecture

### Functionality Overview
The comparator uses a modified prefix adder to compare two binary numbers, `A` and `B`. It computes:
- **A > B**: Positive final carry.
- **A = B**: No final carry or borrow.
- **A < B**: Negative final carry (borrow).

### Recursive Carry Computation
Carry bits are recursively computed using:
\( c_i = g_i + p_i c_{i-1} \)


Where:
- `ci`: Carry bit at position `i`.
- `gi`: Generate signal for position `i`.
- `pi`: Propagate signal for position `i`.

This hierarchical computation ensures speed and efficiency.

---

## Implementation Details

### Key Components
1. **Generate (gi) and Propagate (pi) Signals**:
   - Signals generated for each bit position based on input values.
2. **Tree Structure**:
   - Recursive logic processes smaller bit groups and combines results at higher levels.

### Design Goals
- Minimize hardware complexity.
- Reduce computation time for large input sizes.
- Ensure scalability for high-speed applications.

---

## Results
The proposed design demonstrates significant improvements in:
- **Delay**: Faster operation due to O(log n) latency.
- **Power**: Lower consumption compared to traditional designs.
- **Area**: Reduced hardware complexity.

---

## Applications
- **Sorting Algorithms**
- **Signal Processing**
- **Parallel Computing**
- **Multiprocessing Systems**

---

## Future Work
- Extend the architecture to support larger bit-widths.
- Explore dynamic clock gating for power efficiency.
- Adapt the design for FPGA and ASIC implementations.

---

## License
This project is for academic and research purposes. Redistribution or use without proper acknowledgment is prohibited.

---

## Contact
For questions or collaboration, contact:

- Mohammad Milhem: [mohamadmilhem100@gmail.com](mailto:mohamadmilhem100@gmail.com)
- Mumen Anbar: [mumenanbar12@gmail.com](mailto:mumenanbar12@gmail.com)
- Ameer Rabie: [ameerrabie2008@gmail.com](mailto:ameerrabie2008@gmail.com)
