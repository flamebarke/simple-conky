# simple-conky

A simple .conkyrc file for showing basic system information within Linux.

## Installation

Download to your home directory i.e. ```/home/admin```

open a terminal emulator and change directory into the ```simple-conky``` folder

```
cd ~/simple-conky
```
then copy the ```.conkyrc``` file into your home directory by typing the below into your terminal
```
sudo ./install.sh
```
if typing the above returns a permission error, type the command below to make the script executable

```
sudo chmod 777 conkyrc
```

check to see if the file is present by typing
```
cd ~/
```
```
ls -al
```
you should see a list of files and one should be named ```.conkyrc```.

### Configuration

Configuring the ```.conkyrc``` config file to work for your particular system is a matter of simply adding the logical name of your network interface and the storage path of any HDD/SSD/USB that you would like conky to show into the ```.conkyrc``` file.

To begin with find out the network interface that your device is currently using by typing the below command into your terminal

```
lshw -C network
```
the command should return something like this:

![lshw-command](https://i.imgur.com/AzAVPBx.png)

You can see that for each network device shown there is a description of the device i.e ```ethernet interface``` or ```wireless interface```.  Under the interface that you are connected to the internet through (wireless or ethernet) find the logical name of the interface and write that down. So for the image above the active network interface would be ```wlp4s0```.

** Note: if you are unsure which interface you are recieving your internet connection through, look for the one that has an ip address assigned to it under the configuration heading. If you are still not sure then type ```ifconfig``` into a terminal prompt and look for the interface with a large number of packets under TX and RX, this should be your active network interface.
