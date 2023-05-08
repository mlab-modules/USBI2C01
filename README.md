
<!--- module --->
# USBI2C01A - USB to I2C converter
<!--- Emodule --->

USBI2C01A is USB to I²C master adapter, it provides you ability to connect almost any I2C/SMBUS sensor or other device to a computer trought USB.
Converter is based on [CP2112](https://www.silabs.com/interface/usb-bridges/classic/device.cp2112?tab=specs) integrated USB brigde with native Linux kernel support. 
Therefore device create kernel accesible I2C interface intstantly on almost any Linux distributions. If your computer doesn't support CP2112 converter, it's possible to use the USB-HID interface of the converter. Thanks to that, the device can be used with other operating systems as well, as Windows or Android.

![USBI2C01A](doc/img/USBI2C01A_top_big.jpg)

<!--- description --->


## Drivers and software
The USB device behaves as a standard [USB-HID](https://en.wikipedia.org/wiki/USB_human_interface_device_class) device, so you do not need non-standard drivers. It also allows control of devices in the I2C system bus.

In case of Linux the drivers are available in kernel. Therefore the module creates the system-wide I2C bus. 


## Usage
The functional examples are available in [pymblab](https://github.com/MLAB-project/pymlab) control library. The details are available on [MLAB wiki](https://wiki.mlab.cz/doku.php?id=en:usbi2c). The Pymlab library supports accessing the device both through the I2C interface in the Linux kernel and through the USB-HID interface. Thanks to this, you can use these modules on different operating systems.

<!--- Edescription --->
            
