Android
=======

Serial Bluetooth Terminal

![Serial Bluetooth Terminal - Settings -> Receive](B01.jpg "Serial Bluetooth Terminal - Settings -> Receive")
![Serial Bluetooth Terminal - Settings -> Send](B02.jpg "Serial Bluetooth Terminal - Settings -> Send")

Upload sketch
=============
```
arduino-cli upload -p /dev/ttyUSB0 --fqbn esp32:esp32:esp32-poe-iso BLUETOOTH.ino
```