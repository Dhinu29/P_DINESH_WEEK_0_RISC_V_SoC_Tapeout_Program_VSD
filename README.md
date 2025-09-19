RISC-V REFERENCE SOC TAPEOUT PROGRAM: INSTALLATION OF OPENSOURCE
TOOLS
1. Introduction
The RISC-V Reference SoC Tapeout Program requires a set of open-source EDA (Electronic Design
Automation) tools for design, simulation, synthesis, and verification. This report documents the installation
and setup of the essential tools on Ubuntu, including Yosys, GTKWave, and Icarus Verilog

 2. System Configuration

| Parameter        | Specification                                |
|------------------|----------------------------------------------|
| Virtual Machine  | Oracle VirtualBox [Download](https://www.virtualbox.org/wiki/Downloads) |
| Operating System | Ubuntu 20.04+                                |
| RAM              | 6 GB                                         |
| Hard Disk        | 50 GB                                        |
| CPU              | 4 vCPU                                       |


3. Open-Source Tool Overview

| Tool           | Purpose                                              | Official Website |
|----------------|------------------------------------------------------|------------------|
| **Yosys**      | RTL synthesis, converts Verilog HDL to gate-level netlist | [YosysHQ](https://github.com/YosysHQ/yosys) |
| **Icarus Verilog** | Verilog simulation, compiles and simulates Verilog code | [Icarus Verilog](http://iverilog.icarus.com/) |
| **GTKWave**    | Waveform viewer for simulation results              | [GTKWave](http://gtkwave.sourceforge.net/) |


4. Installation Steps

### 4.1 Install Yosys
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make    # if make is not installed
sudo apt-get install build-essential clang bison flex \
 libreadline-dev gawk tcl-dev libffi-dev git \
 graphviz xdot pkg-config python3 libboost-system-dev \
 libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install
# Verify installation
yosys -V

