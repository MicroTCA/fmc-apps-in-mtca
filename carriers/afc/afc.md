# AFC

Designed by: WUT-ISE and LNLS

Commercially available: Creotech

FPGA: Xilinx Artix-7

Description:

The AMC FMC Carrier (AFC) is an open hardware general purpose carrier board with the ability to host two FPGA Mezzanine Cards (FMC) with High Pin Count (HPC) connectors. The AMC board is designed as a double-width mid-size MTCA.4 carrier. It is an open hardware project licensed under [CERN Open Hardware License](https://www.ohwr.org/projects/cernohl/wiki). The design files can be found at [https://github.com/lnls-dig/afc-hw](https://github.com/lnls-dig/afc-hw).

The AFC features a cost-effective Xilinx Artix-7 FPGA thus making it especially appropriate for systems with high FPGA boards count. It has a flexible clock circuit that enables any clock source to be connected to any clock input, including telecom clock, FMC clocks and FPGA. A feature summary is given below:

* Xilinx Artix-7 200T FFG1156 FPGA
* 2 GB DDR3 SDRAM (32-bit interface)
* 2 high pin count (HPC) slots for 2 single width mezzanines or 1 double width mezzanine
* SPI Flash for FPGA configuration
* SPI Flash for user data storage
* JTAG multiplexer (SCANSTA) for FMC access
* Power supply for FPGA, memory, FMCs - programmable VADJ 1.8-3.3V
* Clock distribution
* White Rabbit timing system compatibility
* Temperature, voltage and current monitoring for critical power buses
* Stand-alone power connector
* Mini-USB connected to the IPMI processor
* SATA connector for Port2, Port3 with possibility of switching to FPGA MGT
* MGT connected to FMC1, FMC2, Fat Pipe 1, Fat Pipe 2 (optional), Port0, Port1, Port2 (optional), Port3 (optional), RTM (optional)
* EEPROM with MAC and unique ID
* RTM connector pins routed to 8 MGTs and general-purpose I/O

## Mezzanines

### FMC ADC 250M 16b 4cha

The FMC ADC 250M 16b 4cha is a 4-channel RF signal digitizer with the following main features:

* VITA 57.1 compliant - high pin count (HPC) mezzanine
* 4 ADC channels: 16-bit 250 MS/s, 700 MHz bandwidth
* ADC device: ISLA216P25
* Clock distribution and PLL: AD9510
* On-board oscillator: Si571
* External ADC clock input
* External digital trigger input
* External reference clock input
* Reference clock can be sourced either from front panel or from FMC bidirectional clocks

The board is licensed under [CERN Open Hardware License](https://www.ohwr.org/projects/cernohl/wiki).

Hardware design files:
[https://github.com/lnls-dig/fmc250-hw](https://github.com/lnls-dig/fmc250-hw)

Gateware example:
[https://github.com/lnls-dig/bpm-gw](https://github.com/lnls-dig/bpm-gw)

Software library:
[https://github.com/lnls-dig/halcs](https://github.com/lnls-dig/halcs)


### FMC POF

The FMC POF is a 5-channel plastic optical fiber receiver/transmitter low pin count FMC mezzanine. Each channel can be assembled as receiver or transmitter individually.

The board is licensed under [CERN Open Hardware License](https://www.ohwr.org/projects/cernohl/wiki).

Hardware design files:
[https://github.com/lnls-dig/fmc-5POF-hw](https://github.com/lnls-dig/fmc-5POF-hw)


### FMC-Pico-1M4

The FMC-Pico-1M4 is a low pin count FMC card that allows digitizing bipolar currents up to 1 mA with high resolution and low drift for current sources floating up to +/- 300 V.

The board is supplied by [CAENels](http://www.caenels.com/products/fmc-pico-1m4/).

Gateware example:
[https://github.com/lnls-dig/bpm-gw](https://github.com/lnls-dig/bpm-gw)

Software library:
[https://github.com/lnls-dig/halcs](https://github.com/lnls-dig/halcs)
