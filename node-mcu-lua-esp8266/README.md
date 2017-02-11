# resources

[API](http://bbs.espressif.com/download/file.php?id=253)

# setup
- [Setup Ubunutu](http://www.esp8266.com/wiki/doku.php?id=toolchain#how_to_setup_a_vm_to_host_your_toolchain)
- add a usb filter for the virtual machine
- `sudo adduser <user> dialout`
- `sudo chmod a+rw /dev/ttyUSB0`
- start ubuntu
  - `VBoxHeadless -s "Ubuntu"`
  - install pip `sudo apt-get -y install python-pip`
  - [Install esptool](https://github.com/espressif/esptool)
- run `esptool.py -p <serial port> chip_id` to confirm device connection
  - port will likely be /dev/ttyUSB0

# notes

The baud rate is the rate at which information is transferred in a communication channel.
In the serial port context, "9600 baud" means that the serial port is capable of transferring a maximum of 9600 bits per second.

Serial port is a type of device that uses an UART chip, a Universal Asynchronous Receiver Transmitter. One of the two basic ways to interface a computer in the olden days, parallel ports were the other way. Serial is simple to hook up, it doesn't need a lot of wires. Parallel was useful if you wanted to go fast, typ 8 times faster than serial, but cables and connectors were expensive. Parallel I/O has completely disappeared from computer designs, caught up by tremendous advances in bus transceivers, the kind of chip that can transmit an electrical signal down a wire.
