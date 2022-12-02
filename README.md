# Introduction 
This fixed hardware platform file implements 4 mipi csi interfaces with 4 data lanes each. 
It can be used with the 4x4 mipi csi FMC board designed to connect 4 Alvium 1500/1800 CSI cameras on a Xilinx ZCU 106. The FMC was designed for HPC0 of ZCU106 and is tested there only. 
All cameras can be used simultaniously. There is an individual IIC attached to each camera connector.


# Getting Started

1.	Plug 4x4 MIPI CSI FMC board on HPC0 connector on ZCU106
2.	Connect an external 5V/10A power supply to the power connector of the FMC board.
3.	Connect a DP display on the DP of ZCU106 (1080p30, 2160p30), connect USB-UART to host PC and boot from SDCard image


# Build and Test
AMD/Xilinx Vivado platform: zcu106avt_fmc_4x4_wrapper_750x4YUV422_8bit_750x4YUV422_8bit_750x4YUV422_8bit_750x4YUV422_8bit.xsa
yocto layer stack:

yocto Honister:

poky/core 
meta-openembedded/meta-oe
meta-openembedded/meta-python
meta-openembedded/meta-networking
meta-openembedded/meta-multimedia
meta-qt5

Xilinx layers tag xlnx-rel-v2022.2:
meta-xilinx-bsp
meta-xilinx-core
meta-xilinx-standalone
meta-xilinx-pynq
meta-xilinx-tools
meta-alvium-avt

