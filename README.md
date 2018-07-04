# vagrants
Contains some vagrant configuration for different development environments.

## Available vagrant configurations
* **12.04_precise_hydro_amd64**: vagrant with Ubuntu 12.04 (Precise) 64bit and bootstrapped to install with unity desktop and ROS Hydro (ros-hydro-desktop-full)
* **14.04_trusty_indigo_i386**: vagrant with Ubuntu 14.04 (Trusty) 32bit and bootstrapped to install with unity desktop and ROS Indigo (ros-indigo-desktop-full)
* **14.04_trusty_indigo_amd64**: vagrant with Ubuntu 14.04 (Trusty) 64bit and bootstrapped to install with unity desktop and ROS Indigo (ros-indigo-desktop-full)
* **16.04_xenial_kinetic_amd64**: vagrant with Ubuntu 16.04 (Xenial) 64bit and bootstrapped to install with unity desktop and ROS Kinetic (ros-kinetic-desktop-full)
* **14.04_trusty_indigo_amd64**: vagrant with Ubuntu 14.04 (Trusty) 64bit and bootstrapped to install with unity desktop and ROS Indigo (ros-indigo-desktop-full)


## Usage
For more in-depth information, see the [Vagrant Homepage](https://www.vagrantup.com/).

To use the availabe vagrant boxes, follow the following steps:

1. `cd` into the respective directory
1. `vagrant up` will bring up the machine
1. to shut down, simply shut down from the guest, or call `vagrant halt`

## Installation
1. To use this repo, you need to install Vagrant.

  ```bash
  apt install vagrant
  ```

1. Next, install Virtualbox, see [here](https://www.virtualbox.org/wiki/Linux_Downloads) or [here](https://wiki.ubuntuusers.de/VirtualBox/Installation/).

## possible issues
- After the bootstrap process, you might have to manually call 'sudo apt-get install -f' to install hddtemp correctly, as it requires interaction, to complete the installation correctly. (Encountered on `precise_hydro`)
- the bootstrap process might not work in one go, you might need to `vagrant halt` the box and do another `vagrant up --provision` run.
