# Bluetooth module for polybar

The module on polybar looks like this:<br>
<br/>
*Current device connected:*
![bt_connected](./screenshots/screenshot_device_connected.png)
<br/>
*Current device disconnected:*
![bt_disconnected](./screenshots/screenshot_device_disconnected.png)
<br/>
*Bluetooth off icon:*
![bt_off](./screenshots/screenshot_bluetooth_off.png)
<br/>

<br/>
Using scroll loops through paired devices.
<br/>
Left mouse click connects or disconnects with currently displayed device. <br>
<br/>
Right mouse click turns on/off bluetooth. <br>

# Installation
Requirements:
    - A NerdFont to display icons
<br/>
To install, copy the following snippet to your polybar config file(usually config.ini):<br>
<br/>

[module/bluetooth]<br><br>

type = custom/script<br>
exec = ./bluetooth<br>
tail = true<br>
click-left = ./bluetooth --toggle &<br>
click-right = ./bluetooth --switch &<br>
scroll-up = ./bluetooth --increment &<br>
scroll-down = ./bluetooth --decrement &<br>
interval = 0.25 <br>
<br/>

and put the bluetooth script in the same directory.

