
<!--- module --->
# USBI2C01A - USB to I2C converter
<!--- Emodule --->

USB device to I²C master adapter. It is based on [CP2112](https://www.silabs.com/interface/usb-bridges/classic/device.cp2112?tab=specs) integrated USB brigde with native Linux kernel support. 
Therefore device create kernel accesible I2C interface intstantly on almost any Linux distributions. 

![USBI2C01A](/doc/img/USBI2C01A_top_big.jpg)

<!--- description --->


## Drivers and software
The USB device behaves as a standard HID device, so you do not need non-standard drivers. It also allows control of devices in the I2C system bus.

In case of Linux the drivers are available in kernel. Therefore the module creates the system-wide I2C bus. 


## Usage

The functional examples are available in [pymblab](https://github.com/MLAB-project/pymlab) control library. The details are available on [MLAB wiki](https://wiki.mlab.cz/doku.php?id=en:usbi2c)

<!--- Edescription --->
            
