# Open FPGA platform for battery-free UHF RFID sensing

> **Status: planning.** The source code will be published here once the project starts.

## About

This project turns a low-cost, low-power FPGA (Lattice MachXO2-4000ZE) into an open, battery-free EPC Gen2 UHF RFID sensor tag. The FPGA implements the complete tag in hardware (PIE decoding, CRC, Gen2 command handling, FM0/Miller backscatter encoding, tag memory) next to a small RISC-V microcontroller (SERV) that reads sensors over SPI/I2C. Firmware is loaded over the air through standard Gen2 Write commands to User memory, so any commercial reader can reprogram the tag and read its data.

Existing platforms either fix the protocol in closed silicon or implement it as firmware on a commercial microcontroller. Here, both layers are open: users can change the sensing application and also the tag's protocol logic itself.

## Planned deliverables (first version)

- FPGA design of the EPC Gen2 tag and RISC-V subsystem
- Firmware SDK with example sensor applications
- Carrier board with a simple RF front-end and energy harvester
- Power measurements and documentation

Later work will improve the analog front-end and the integration.

## Planned licenses

- Hardware (PCB): CERN-OHL-S-2.0
- RTL: Solderpad Hardware License 2.1
- Firmware and software: Apache-2.0

## Author

Karim Chaffai, University of Navarra
