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
   
   
   4.1 Install Yosys
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
   ```
   
   
   4.2 Install Icarus Verilog
   ```bash
   sudo apt-get update
   sudo apt-get install iverilog
   
   # Verify installation
   iverilog -V
   ```
   
   
   4.3 Install GTKWave
   ```bash
   sudo apt-get update
   sudo apt install gtkwave
   
   # Verify installation
   gtkwave --version
   ```
5. Tool Snapshot Documentation	
Take screenshots after installation and verification to include in your GitHub repository. Example table format:
5.1 YOSYS:
Command to Verify: yosys -V
<img width="1595" height="852" alt="YOSYS_TOOL_VERIFY" src="https://github.com/user-attachments/assets/1653c5c5-17bb-4ea1-a138-086c0e8c973a" />

5.2 GTKWave:
Command to Verify: gtkwave --version
<img width="1592" height="822" alt="GTKWAVE_TOOL_VERIFY" src="https://github.com/user-attachments/assets/cccd9b53-fbd0-48e9-8a37-63fdd4ead4df" />




5.3 Icarus Verilog: 
Command to Verify: iverilog -V
<img width="1587" height="845" alt="IVERILOG_TOOL_VERIFY" src="https://github.com/user-attachments/assets/0c0c55c8-1737-44c2-9f67-ad9f2439c6b2" />




6. Conclusion
All required tools for RISC V SoC tapeout have been successfully installed on Ubuntu 20.04 VM. The system meets the required configuration, and verification commands confirm the tools are functioning. Screenshots and documentation are prepared for GitHub submission.


