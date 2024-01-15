# Molecular-Docking
Here I am going to describe from installation to running basic molecular docking 



#Installation required Software

1. AutoDock Vina
2. ADFR software suite
3. Meeko

#Installing AutoDock Vina: 
I used debian in conda environment for installation for auto dock vina

Step 1: Create conda environnment
$ conda create -n vina python=3.7

Newest version of python can not create wheel for dpendencies that why I specified python3.7

$ conda activate vina

$ conda config --env --add channels conda-forge

Install dependencies wheel before install AutoDock Vina

$ conda install -c conda-forge numpy swig boost-cpp sphinx sphinx_rtd_theme

install vina through pip

$pip install vina

#2 Installing ADFR software suite
Which is requred for recpetor and ligand preperation and other dependencies
ADFR v1.2 and associate scripts

AGFR v1.2

AutoSite v1.0 and v1.1

ADCP v1.0

AutoGrid4.2

prepare_ligand

prepare_receptor

Download the appropriate software from https://ccsb.scripps.edu/adfr/downloads/

I used ADFRsuite 1.0 Linux 64 tarball installer (See the instruction bellow that is provided

$ tar zxvf ADFRsuite_x86_64Darwin_1.0.tar.gz

$ cd ADFRsuite_x86_64Darwin_1.0

./install.sh -d vinadock -c 0

vinadock was my installation location folder

Then, I exported path to .bashrc script to gain access the bin folder of ADFR where all required package there

$ nano ~/.bashrc

add the following line (you can find this by writing pwd in you linux terminal)

export PATH="/home/vinadock/bin: $PATH"


Now you are ready to go for basic docking simulations

#3. Install meeko in your conda environment
$pip3 install meeko
