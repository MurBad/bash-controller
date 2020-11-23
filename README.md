# bash-controller
> A simple way to monitor and control your system. 

bash-controller is a simple panel running on terminal that helps you to see
information about your system, audio, brightness, battery, wireless connection,
and more. 
You can also control your system using some keys of your keyboard.

## Installation
bash-controller don't need any installation, you can simply download or clone it
to your machine and give it permissions. 
This is how you can do:

```shell
git clone https://github.com/MurBad/bash-controller.git
cd bash-controller
chmod +x bash-controller
```

### Dependencies
If you try to run bash-controller now you probably will see some messages
talking about commands you have to install before start using bash-controller.

It happens because bash-controller has some dependencies that you can probably
install using your distro package manager, `dnf` or `apt` for example. 

The dependencies that bash-controller has are:
* acpi
* pactl
* iwgetid 
* light/xbacklight 

Probably `acpi`, `pactl` and `iwgetid` are default in your distro, but I list
them for the possibility your distro don't have them natively.

After install all these dependencies bash-controller will run perfectly. 

## Usage
bash-controller is easy to use. After give permissions you can just run using
```shell
./bash-controller
```

You can also use some flags when running bash-controller. 
* `-h` shows a usage text
* `-v` shows bash-controller's version
* `-t` Needs an argument and is used to change update time inside bash-controller

After start the script, you can just type `h` to have more information about the
keys used and what you can control with bash-controller. To close the script
just type `q`.

### Config file
bash-controller works using a config file called `config` and it needs to keep
with bash-controller in the same dir. This file is used to store some variables
used to define some useful things on bash-controller. 

Between them:
* Keys used to control your system
* Log filename
* Time interval to update bash-controller information
* Command used to control brightness (this variable has to be keeped in the last
  line of the config file).

## License
The code in this project is licensed under MIT license.
