# simple-conky

A simple .conkyrc file for showing basic system information within Linux.

## Installation

Download to your home directory i.e. /home/admin 

open a terminal emulator and cd into the simple-conky folder

```
cd ~/simple-conky
```
then copy the .conkyrc file into your home directory by typing the below into your terminal
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
you should see a list of files and one should be named .conkyrc.

### Configuration

Configuring the .conkyrc config file to work for your particular system is a matter of simply adding the name of your network interface and the storage path of any HDD/SSD/USB that you would like conky to show into the .conkyrc file.

To begin with find out the network interface that your device is currently using by typing the below command into your terminal

```
lshw -C network
```
the command should return something like this:

![lshw -C network](https://imgur.com/AzAVPBx)

