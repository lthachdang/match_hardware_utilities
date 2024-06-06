# match Hardware Utilities

### Installation of DualShock Support

#### Install driver ds4drv
1. Install pip for python
.. code-block:: bash
$ sudo apt install pip

2. Install Dualshock ds4drv driver to use ds4ros
.. code-block:: bash
$ sudo -H pip install git+https://github.com/gerardcanal/ds4drv

3. Add ds4drv rule
.. code-block:: bash
$ sudo wget https://raw.githubusercontent.com/chrippa/ds4drv/master/udev/50-ds4drv.rules -O /etc/udev/rules.d/50-ds4drv.rules

4. Update udevadm
.. code-block:: bash
$ sudo udevadm control --reload-rules && sudo udevadm trigger

5. Reboot

#### Connect the DualShock controller
1. Open bluetoothctl in a terminal
$ bluetoothctl

2. Enable scan
$ scan on

3. Press Share-button and PlayStation-button on DualShock controller for 5s

"Wireless Controller" with MAC-adress should pop up

4. Connect to Wireless Controller:

$ connect "MAC"

5. Trust Wireless Controller

$ trust "MAC"

6. Exit bluetoothctl

$ exit

DualShock-Controller should now automatically connect to the MUR after a reboot by pressing the PlayStation-Button