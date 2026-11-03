# Open FPGA platform for battery-free UHF RFID sensing

## About

This project turns a low-power FPGA (Lattice MachXO2-4000ZE) into a battery-free EPC Gen2 UHF RFID sensor tag. The FPGA runs the tag protocol in hardware, next to a small RISC-V microcontroller (SERV) that talks to sensors. Both layers are open: you can program the microcontroller like any other, and you can also change the tag hardware itself, for example the protocol logic or an added encryption core.

The digital design (EPC Gen2 tag + RISC-V) comes from a tag SoC developed during a PhD at the University of Navarra, and it already works on FPGA with a commercial reader. The work here is to turn it into a platform others can use, step by step:

1. **Survive power loss.** Store the tag data in the FPGA's internal flash and restore it at power-up. The goal is to make it work first; optimisation comes later.
2. **Run from RF power.** Connect the FPGA to an existing open analog front-end (based on the WISP 5 front-end) on a first carrier board, so a commercial reader can power and read it at close range.
3. **Improve.** Develop a better front-end, reduce power, and add sensor examples.
4. **Release.** Publish the RTL, PCB, firmware and reader tools with documentation.

The source code will be published here as the project progresses.
