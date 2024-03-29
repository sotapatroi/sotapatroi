Android
=======

Serial Bluetooth Terminal

https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal&hl=en_US&gl=US

![Serial Bluetooth Terminal - Settings -> Receive](B01.jpg "Serial Bluetooth Terminal - Settings -> Receive")
![Serial Bluetooth Terminal - Settings -> Send](B02.jpg "Serial Bluetooth Terminal - Settings -> Send")

gnu/linux
=========

Add user to dialout group

```
usermod -a -G dialout zital
```

arduino-cli
===========

1. Install
```
su
cd /tmp
curl -fsSL https://raw.githubusercontent.com/arduino/arduino-cli/master/install.sh > install.sh
```

Edit install.sh and replace:
```
DEFAULT_BINDIR="$PWD/bin"
```

by
```
DEFAULT_BINDIR="/usr/local/bin"
```

```
bash install.sh
exit
```

2. Get port list

```
arduino-cli board list
```

Output example:
```
Port         Protocol Type    Board Name FQBN Core
/dev/ttyS0   serial   Unknown                
/dev/ttyUSB0 serial   Unknown                
```

3. Upload sketch

Exec command while BOOT button is pressed

![ESP32 BOOT button](ESP3201.jpg "ESP32 BOOT button")

```
arduino-cli upload -p /dev/ttyUSB0 --fqbn esp32:esp32:esp32-poe-iso EXAMPLE.ino
```