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

Follow the steps mentiond in this [document](https://openlane2.readthedocs.io/en/latest/getting_started/docker_installation/index.html)

Do note you'll need to add `--dockerized` right after `openlane` in most CLI invocations.



