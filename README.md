# Bluetooth module for polybar

The module on polybar looks like this:<br>
*Current device connected:*
![bt_connected](./screenshots/screenshot_device_connected.png)

*Current device disconnected:*
![bt_disconnected](./screenshots/screenshot_device_disconnected.png)

Using **scroll** loops through paired devices.

**Left mouse click** connects or disconnects with currently displayed device. <br>

**Right mouse click** turns on/off bluetooth. 
*Bluetooth off icon:*
![bt_off](./screenshots/screenshot_bluetooth_off.png)


# Installation
To install, copy the following snippet to your polybar config file(usually config.ini):<br><br>

[module/bluetooth]<br><br>

type = custom/script<br>
exec = ./bluetooth<br>
tail = true<br>
click-left = ./bluetooth --toggle &<br>
click-right = ./bluetooth --switch &<br>
scroll-up = ./bluetooth --increment &<br>
scroll-down = ./bluetooth --decrement &<br>
interval = 0.25 <br><br>

and put the **bluetooth** script in the same directory.
