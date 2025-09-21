# India-RISC-V-Tapeout-Program-with-IITGN-VSD
## System Requirements  
  
System Requirements  
6 GB RAM  
50 GB HDD  
Ubuntu 20.04 or higher  
4 vCPU  
  
## Tools Installation
<ins>**All the instructions for installation of required tools can be found here:**</ins>  

  1. iverilog
     ```
     sudo apt-get install -y autoconf gperf make gcc g++ bison flex --assume-yes
cd $HOME
git clone https://github.com/steveicarus/iverilog.git
cd iverilog
sh autoconf.sh
./configure
make
sudo make install
```
