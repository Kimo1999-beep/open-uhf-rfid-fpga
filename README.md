# Open FPGA platform for battery-free UHF RFID sensing

## About

This project turns a low-power FPGA (Lattice MachXO2-4000ZE) into a battery-free EPC Gen2 UHF RFID sensor tag. The FPGA runs the tag protocol in hardware, next to a small RISC-V microcontroller (SERV) that talks to sensors. Both layers are open: you can program the microcontroller like any other, and you can also change the tag hardware itself, for example the protocol logic or an added encryption core.

The digital design (EPC Gen2 tag + RISC-V) comes from a tag SoC developed during a PhD at the University of Navarra, and it already works on FPGA with a commercial reader. The work here is to turn it into a platform others can use and modify.


## Author note:
I don't have the time to work on this, so I am currently looking for some funding to hire a couple of students to do the work.
If somebody is interested, feel free to contact me
