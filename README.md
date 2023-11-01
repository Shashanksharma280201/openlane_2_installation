# openlane_2_installation

## github link for openlane installation :
[openlane2](https://github.com/efabless/openlane2)

## Steps to follow to install openlane on ubuntu 20.04+ :

### python installation :
  - python 3.8 or higher
  - PIP
  - VENV
  - Tkinter


### commands to install all the above : 
```
#installing python 3.8 or higher

sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.8
sudo apt upgrade

#installing pip , VENE , Tkinter

sudo apt update
sudo apt install python3 python3-pip
sudo apt install python3-tk
python3 -m venv venv_name
source venv_name/bin/activate
deactivate
pip install --upgrade pip
```

## NIX installatio (Recommended)

Works for macOS and Linux (x86-64). Recommended, as it is more integrated with your filesystem and overall has less upload and download deltas.

Follow the steps mentiond in this [document](https://openlane2.readthedocs.io/en/latest/getting_started/nix_installation/index.html)


## Docker installation 
Works for Windows, macOS and Linux (x86-64, aarch64 with emulation).

Follow the steps mentiond in this [document](https://docs.docker.com/engine/install/ubuntu/)

Do note you'll need to add `--dockerized` right after `openlane` in most CLI invocations.

### to check is docker is installed run the command mentioned:
![Screenshot from 2023-09-11 16-50-45](https://github.com/Shashanksharma280201/openlane_2_installation/assets/79470436/de004ce5-c25a-480e-a760-b54392ebd3a3)

```
docker --version
python3 --version
python3 -m pip --version
```

the following should be the updated versions of all the mentioned softwares:
```
$ docker --version
Docker version 20.10.16, build aa7e414fdc
$ python3 --version
Python 3.10.5
$ python3 -m pip --version
pip 21.0 from /usr/lib/python3.10/site-packages/pip (python 3.10)
...
Once an environment has been created, you may wish to activate it, e.g. by
sourcing an activate script in its bin directory.
```

## Installation of ngspice magic 

Download the tarball from [Download](https://sourceforge.net/projects/ngspice/files/) to a local directory

```
cd $HOME
sudo apt-get install libxaw7-dev
tar -zxvf ngspice-41.tar.gz
cd ngspice-41
mkdir release
cd release
../configure  --with-x --with-readline=yes --disable-debug
sudo make
sudo make install
```

magic 

```
sudo apt-get install m4
sudo apt-get install tcsh
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
sudo make
sudo make install
```


## Openlane2 installation commands:

```
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```

Install openlane using PIP ( is this gives error then install pipx and run the same command using pipx)
```
sudo python3 -m pip install openlane
# if the above code does not work then try :
sudo python3 -m pip install openlane --break-system-packages

sudo python3 -m openlane --dockerized --smoke-test
```
If the smoke test finishes successfully, then you are ready to use OpenLane2.

![2](https://github.com/Shashanksharma280201/openlane_2_installation/assets/79470436/7b90bb58-f461-461d-b883-662651b619fc)



