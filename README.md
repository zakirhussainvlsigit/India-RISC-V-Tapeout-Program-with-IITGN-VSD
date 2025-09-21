# India-RISC-V-Tapeout-Program-with-IITGN-VSD
## System Requirements  
  
System Requirements  
6 GB RAM  
50 GB HDD  
Ubuntu 20.04 or higher  
4 vCPU  
  
## Tools Installation
<ins>**All the instructions for installation of required tools can be found here:**</ins>  

     <ins>1. iverilog</ins>  
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
     
     <ins>2. GTKWave</ins>
        ```
        sudo apt update
        sudo apt install build-essential meson gperf flex desktop-file-utils libgtk-3-dev --assume-yes
        sudo apt install libbz2-dev libjudy-dev libgirepository1.0-dev --assume-yes
        sudo apt install cmake --assume-yes
        sudo apt install libgtk-4-dev --assume-yes
        cd $HOME
        git clone "https://github.com/gtkwave/gtkwave.git"
        cd gtkwave
        meson setup build && cd build && sudo meson install

        ```
