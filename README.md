# match Hardware Utilities

## Installation of DualShock Support

### Install driver ds4drv
Install pip for python
`sudo apt install pip`
Install Dualshock ds4drv driver to use ds4ros
`sudo -H pip install git+https://github.com/gerardcanal/ds4drv`
Add ds4drv rule
`sudo wget https://raw.githubusercontent.com/chrippa/ds4drv/master/udev/50-ds4drv.rules -O /etc/udev/rules.d/50-ds4drv.rules`
Update udevadm
`sudo udevadm control --reload-rules && sudo udevadm trigger` 
Reboot

### Connect the DualShock controller
Open bluetoothctl in a terminal
`bluetoothctl`
Enable scan
`scan on`
Press Share-button and PlayStation-button on DualShock controller for 5s
"Wireless Controller" with MAC-adress should pop up
Connect to Wireless Controller
`connect "MAC"`
Trust Wireless Controller
`trust "MAC"`
Exit bluetoothctl
`exit`
DualShock-Controller should now automatically connect to the MUR after a reboot by pressing the PlayStation-Button