# RISC_V_SoC_Tapeout_Program_VSD
This report documents the installation of open-source EDA tools required for the RISC‑V Reference SoC Tapeout Program. Ubuntu 20.04 VM is used to set up the environment. Tools installed include Yosys, Icarus Verilog, and GTKWave.
RISC V REFERENCE SOC TAPEOUT PROGRAM: INSTALLATION OF OPEN-SOURCE TOOLS
1. Introduction
The RISC V Reference SoC Tapeout Program requires a set of open-source EDA (Electronic Design Automation) tools for design, simulation, synthesis, and verification. This report documents the installation and setup of the essential tools on Ubuntu, including Yosys, GTKWave, and Icarus Verilog.
2. System Configuration
Parameter	Specification
Virtual Machine	Oracle VirtualBox Download
Operating System	Ubuntu 20.04+
RAM	6 GB
Hard Disk	50 GB
CPU	4 vCPU

3. Open-Source Tool Overview
Tool	Purpose	Official Website
Yosys	RTL synthesis, converts Verilog HDL to gate-level netlist	YosysHQ
Icarus Verilog	Verilog simulation, compiles and simulates Verilog code	Icarus Verilog
GTKWave	Waveform viewer for simulation results	GTKWave
4. Installation Steps
4.1 Yosys Installation
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make           # if make is not installed
sudo apt-get install build-essential clang bison flex \
 libreadline-dev gawk tcl-dev libffi-dev git \
 graphviz xdot pkg-config python3 libboost-system-dev \
 libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make installA
# Verify installation
yosys -V
4.2 Icarus Verilog Installation
sudo apt-get update
sudo apt-get install iverilog
# Verify installation
iverilog -V
4.3 GTKWave Installation
sudo apt-get update
sudo apt install gtkwave
# Verify installation
gtkwave –version	






<img width="1592" height="822" alt="GTKWAVE_TOOL_VERIFY" src="https://github.com/user-attachments/assets/048c4590-960b-41c2-8431-0d77938738f7" />

5. Verification
After installing all tools:
•	Verify that Yosys runs without errors:
“yosys -h”
•	Compile and simulate a sample Verilog code using Icarus Verilog:
“iverilog -o test test.v”
              “vvp test”
•	Open generated .vcd waveform file in GTKWave:
             “gtkwave test.vcd”
5. Tool Snapshot Documentation	
Take screenshots after installation and verification to include in your GitHub repository. Example table format:
5.1 YOSYS:
Command to Verify: yosys -V
5.2 GTKWave:
Command to Verify: gtkwave --version
5.3 Icarus Verilog: 
Command to Verify: iverilog -V
6. Conclusion
All required tools for RISC V SoC tapeout have been successfully installed on Ubuntu 20.04 VM. The system meets the required configuration, and verification commands confirm the tools are functioning. Screenshots and documentation are prepared for GitHub submission.


