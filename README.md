# Fpga-8x8-Systolic-Array-Accelerator-for-LLM-
In this we maked 8x8 systolic array on fpga and throught its jupyter interfcae of fpga we maked LLM that predicts forex price and maked process very fast with this systolic array, altough i will not share my codes as of because my research paper is under review on this topic 
# Hardware Design Details

### Systolic Array Architecture
<img width="1838" height="922" alt="Screenshot 2025-10-22 010236" src="https://github.com/user-attachments/assets/4d7cce91-bfcd-4195-bd01-f6b9b9736656" />

The 8x8 systolic array implements a matrix multiplication accelerator where:
- Data flows horizontally (input matrices)
- Partial results accumulate vertically
- Each PE performs multiply-accumulate (MAC) operations
- Fully pipelined for maximum throughput

### Memory Interface

- **AXI Memory Mapped Interface**: 8 independent channels (m_axi_gmem_0 to m_axi_gmem_7)
- **Control Interface**: AXI-Lite slave for configuration
- **BRAM Interface**: Fast on-chip memory access

### Clock and Reset

- **Clock**: 100 MHz (FCLK_CLK0 from PS)
- **Reset**: Active-low synchronous reset
- All components synchronized to single clock domain

## Getting Started

### Prerequisites

- Xilinx Vivado 2020.2 or later
- Xilinx Vitis HLS 2020.2 or later
- PYNQ-Z2 board
- PYNQ v2.7 or later
# Results 
<img width="1036" height="547" alt="image" src="https://github.com/user-attachments/assets/01b83779-8e00-47c0-a81b-8da978e79589" />
