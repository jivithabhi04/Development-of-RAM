# Development-of-RAM

## Multi-Bank RAM in FPGA

This project implements a multi-bank RAM system on an FPGA using Verilog. The system includes a controller for managing four individual 32x32 RAM blocks, allowing for efficient memory access and management. This project provides a template for understanding and implementing memory systems in FPGA designs.
Introduction
The multi-bank RAM system consists of four 32x32 RAM blocks, controlled by a single controller module. Each RAM block can be individually accessed for read and write operations. The controller uses a 2-bit chip select input to determine which RAM block to access.

## Features

- Four independent 32x32 RAM blocks
- Single controller for managing multiple RAM blocks
- Configurable read and write operations
- Simple and modular design

## Usage

The multi-bank RAM system can be used in various FPGA applications requiring efficient memory access. The main modules of the system include `RAM_32x32` and `RAM_FOUR_32x32`.

`RAM_32x32` Module
The `RAM_32x32` module represents a simple 32x32 RAM block with read and write capabilities.

- `reset`: Asynchronous reset signal
- `clk`: System clock input
- `cs`: Chip select (active-high)
- `rw`: Read/Write control (1 for write, 0 for read)
- `data_in`: Data input for write operations
- `addr`: Address input for memory access
- `data_out`: Data output for read operations

RAM_FOUR_32x32` Module
The `RAM_FOUR_32x32` module combines four `RAM_32x32` instances, enabling a multi-bank RAM system with a 2-bit chip select input to select one of the four RAM banks.

- `rst`: Synchronous reset signal
- `reset`: Asynchronous reset signal
- `clk`: System clock input
- `rw`: Read/Write control (1 for write, 0 for read)
- `data_in`: Data input for write operations
- `addr`: Address input for memory access
- `cs_in`: 2-bit chip select input for selecting one of the four RAM banks
- `data_out`: Data output for read operations
