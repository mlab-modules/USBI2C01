
<!--- module --->
# USBI2C01A - USB to I2C converter
<!--- Emodule --->

USBI2C01A is USB to I²C master adapter, it provides you ability to connect almost any I2C/SMBUS sensor or other device to a computer trought USB.
Converter is based on [CP2112](https://www.silabs.com/interface/usb-bridges/classic/device.cp2112?tab=specs) integrated USB brigde with native Linux kernel support. 
Therefore device create kernel accesible I2C interface intstantly on almost any Linux distributions.
If your computer doesn't support CP2112 converter, it's possible to use the USB-HID interface of the converter.
Thanks to that, the device can be used with other operating systems as well, as Windows or Android.

![USBI2C01A](doc/img/USBI2C01A_top_big.jpg)

The module is connected to USB using a USB-B connector, which provides a quality connection to the computer. The module contains three LED diodes that indicate power and communication via the I2C bus in the default configuration. The communication pins are doubled, so you will have enough space to connect your circuit.

I2C is connected to the 5-pin header in the MLAB I2C pinout. This is specific in that the rotation of cable (connector) will only result in not functioning state. However, there is no risk of electrical damage. Using jumpers, it is possible to set the power supply voltage in the I2C bus connector. This can either be 5V from USB, which is protected by a 750 mA fuse, or 3.45V from the integrated LDO with a maximum allowed load of 100 mA.




## Drivers and software
The USB device behaves as a standard [USB-HID](https://en.wikipedia.org/wiki/USB_human_interface_device_class) device, so you do not need non-standard drivers. It also allows control of devices in the I2C system bus.

In case of Linux the drivers are available in kernel. Therefore the module creates the system-wide I2C bus. 




## Usage
The functional examples are available in [pymblab](https://github.com/MLAB-project/pymlab) control library. The details are available on [MLAB wiki](https://wiki.mlab.cz/doku.php?id=en:usbi2c). The Pymlab library supports accessing the device both through the I2C interface in the Linux kernel and through the USB-HID interface. Thanks to this, you can use these modules on different operating systems.


## Hardware

[![schematics](doc/gen/USBI2C01-schematic.svg)](doc/gen/USBI2C01-schematic.pdf)
