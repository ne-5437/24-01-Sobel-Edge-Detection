# Sobel Edge Detection on FPGA (ZYNQ 7000)

## Project Overview:
This project implements Sobel Edge Detection on FPGA using the ZYNQ 7000, integrating DDR memory, a DMA controller, and Image Processing IP for efficient image processing and edge detection.

## Key Components:
- **ZYNQ 7000**: Utilized for processing with efficient hardware and software integration.
- **DDR Memory**: Stores image data for processing.
- **Image Processing IP**: Implements the Sobel edge detection algorithm.
- **DMA Controller**: Manages data flow between memory and processing components.
- **AXI Bus**: Ensures high-speed data communication across the system.

## Process Highlights:
1. **Design of Line Buffer & MAC**:
   - Implemented line buffer with 512x512 pixel storage.
   - Designed MAC module for convolution with predefined kernel and pipelining.

2. **Design of Control Logic**:
   - Managed line buffers and multiplexers.
   - Implemented counter and state machine to control data flow for processing.

3. **IP Packaging & Simulation**:
   - Combined modules (line buffers, control logic, convolution) interfacing with DMA controller via AXI Stream.
   - Developed test bench for image file input and verification.

4. **System Integration & Evaluation**:
   - Used AXI Stream Data Width Converter to resolve interface mismatches.
   - Integrated DMA controller and ACP for efficient memory access and processing.

5. **Edge Detection through Sobel Operation**:
   - Optimized image transfer by storing fixed data directly in DDR.
   - Applied thresholding to detect edges in processed image data.

## Achievements:
- Robust image processing pipeline with ZYNQ 7000.
- Efficient data handling through DDR memory and DMA controller.
- Real-time edge detection with Sobel operator.

## Hardware Used:
- **ZedBoard 7000 FPGA**
- **DDR Memory**
- **ZYNQ PS & DMA Controller**

## Software Tools:
- **Xilinx Vivado**: For hardware design and simulation.
- **SDK**: For software integration and testing.
