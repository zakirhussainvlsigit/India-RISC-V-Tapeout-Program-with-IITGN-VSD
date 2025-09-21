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
<img width="812" height="188" alt="image" src="https://github.com/user-attachments/assets/f9949cd2-18ce-4cd3-a342-fe8246bcb313" />

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
<img width="810" height="143" alt="image" src="https://github.com/user-attachments/assets/f5c818dc-5093-48f7-9596-424a3ad042ce" />

<ins>3. Yosys</ins>
```
sudo apt-get update
sudo apt install make --assume-yes
sudo apt-get install build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev --assume-yes
sudo apt-get install libboost-python-dev libboost-filesystem-dev zlib1g-dev --assume-yes
cd $HOME
git clone https://github.com/YosysHQ/yosys.git
cd yosys
git submodule update --init
make config-gcc
make
sudo make install
```
<img width="815" height="148" alt="image" src="https://github.com/user-attachments/assets/68ed6e88-c2d6-442b-99b7-adc7be73be11" />

<ins>4. ngspice</ins>
```
sudo apt install libxaw7-dev libx11-dev libxext-dev libxt-dev --assume-yes
cd $HOME
curl -L -o ngspice-45.2.tar.gz https://excellmedia.dl.sourceforge.net/project/ngspice/ng-spice-rework/45.2/ngspice-45.2.tar.gz
tar -zxvf ngspice-45.2.tar.gz
cd ngspice-45.2
mkdir release
cd release
../configure --with-x --with-readline=yes --disable-debug
make
sudo make install
```
<img width="807" height="172" alt="image" src="https://github.com/user-attachments/assets/8ee2662c-c00a-49ff-b13e-7d83baf93ac8" />

<ins>5. magic</ins>
```
echo "*********************************  Installing Magic dependancies   ********************************"
echo
echo
sudo apt-get update
sudo apt-get install m4 --assume-yes
sudo apt-get install tcsh --assume-yes
sudo apt-get install csh --assume-yes
sudo apt-get install libx11-dev --assume-yes
sudo apt-get install tcl-dev tk-dev --assume-yes
sudo apt-get install libcairo2-dev --assume-yes
sudo apt-get install mesa-common-dev libglu1-mesa-dev --assume-yes
sudo apt-get install libncurses-dev --assume-yes
cd $HOME
echo
echo
echo "****************************** Cloning magic and will start installation of magic*********************"
echo
echo
cd $HOME
git clone https://github.com/RTimothyEdwards/magic.git
cd magic
./configure 
make
sudo make install
```
<img width="807" height="151" alt="image" src="https://github.com/user-attachments/assets/56059940-39ae-451b-a52d-1d44912d2f53" />

<ins>6. OpenSTA</ins>
```
echo "*********************************  Installing OpenSTA dependancies   ********************************"
sudo apt update

# Core build tools
sudo apt install --assume-yes cmake clang gcc g++ make

# Parser tools
sudo apt install --assume-yes tcl swig bison flex

# Libraries
sudo apt install --assume-yes libeigen3-dev libcudd-dev tclreadline zlib1g-dev

sudo apt install cmake --assume-yes
sudo apt-get install -y swig --assume-yes
sudo apt install libeigen3-dev --assume-yes
sudo apt install tcl-dev tk-dev --assume-yes


cd $HOME
curl -L -o cudd-3.0.0.tar.gz https://github.com/davidkebo/cudd/raw/main/cudd_versions/cudd-3.0.0.tar.gz
tar xvfz cudd-3.0.0.tar.gz
cd cudd-3.0.0
./configure
make
sudo make install

echo "****************************** Cloning OpenSTA and will start installation of OpenSTA*********************"
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make
sudo make install
```
<img width="808" height="136" alt="image" src="https://github.com/user-attachments/assets/abedf7ed-1a3b-4e32-8c54-c68414f8af1d" />

<ins>7. OpenLane</ins>
```
echo "*********************************  Installing OpenLane dependancies   ********************************"
#### step1. Installation of required packages
sudo apt-get update --assume-yes
sudo apt-get upgrade --assume-yes
sudo apt install -y build-essential python3 python3-venv python3-pip make git --assume-yes

#### step2. Docker

# Remove old installations
sudo apt-get remove docker docker-engine docker.io containerd runc --assume-yes
# Installation of requirements
sudo apt-get install ca-certificates curl gnupg lsb-release --assume-yes
# Add the keyrings of docker
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
# Add the package repository
echo \
   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin --assume-yes

# Check for installation
sudo docker run hello-world

#### step3. Making Docker available without root (Linux)
sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot # REBOOT!


echo "****************************** After System's Reboot Cloning OpenLane and will start installation of OpenLane*********************"

#### step4. Checking the Docker Installation

# After reboot
docker run hello-world

#### step5. Download and Install OpenLane
#git clone --depth 1 https://github.com/The-OpenROAD-Project/OpenLane.git
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test

```
<img width="825" height="283" alt="image" src="https://github.com/user-attachments/assets/4253dcaa-aa65-47cf-b7ea-170846fdf1ec" />

