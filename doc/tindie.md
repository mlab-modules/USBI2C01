## USBI2C01A - USB to I²C Master Converter

The [USBI2C01A](https://github.com/mlab-modules/USBI2C01) is a USB to I²C master adapter that allows you to connect almost any I2C/SMBUS sensor or other device to a computer through USB.
This converter is based on the [CP2112](https://www.silabs.com/interface/usb-bridges/classic/device.cp2112?tab=specs) USB-SMBus/I2C bridge with Linux kernel support, which creates a kernel-accessible I2C interface
directly on almost any Linux distribution. If your computer doesn't support the CP2112 converter, you can use the USB-HID interface of the converter,
making it compatible with other operating systems such as Windows or Android.

![](https://github.com/mlab-modules/USBI2C01/blob/385029d61cb48975566b024203a44f2382d34088/doc/img/USBI2C01A_small-5.jpg)

The module is connected to the computer using a USB-B connector, which provides a high-quality connection. Converter contains three LED diodes
that indicate power and communication via the I2C bus in the default configuration. Communication pins are doubled, that allows you create complex devices. 

I2C is connected to the 5-pin header in the MLAB I2C pinout (GND-SDA-VCC-SCL-GND). Using jumpers, you can set
the power supply voltage in the I2C bus connector. This can be 5V from USB, which is protected by a 750 mA fuse, or 3.45V from
the integrated LDO with a maximum allowed load of 100 mA.

Converter is equipped with a set of GPIO ports that can be controlled via USB. In addition to communication via I2C,
you can check the status of digital signals or control them with software. Similarly, you can use LEDs on the module to
indicate your own states because they are software-controllable.

#### Parameters
* USB-HID to SMBus (I2C) master bridge
* 8 GPIO ports (2 equipped with LED indicators)
  * Configurable as Input/Output, Open-drain/Push-pull
  * Configurable as clock output (48 MHz to 94 kHz)
* Selectable 5V or 3.3V power supply
* USB-B - FullSpeed USB support (up to 12 Mbps)
  * Powered from USB
* Support in Linux kernel
* Configurable clock speed, 7-bit I2C addressing
* Ready to use

#### Drivers and Software
The USB device behaves as a standard USB-HID device, so you don't need non-standard drivers. It also allows control of devices in the I2C system bus.

In the case of Linux, the drivers are available in the kernel. Therefore, the module creates the system-wide I2C bus. This is the same interface that you can
find on single-board computers like the Raspberry Pi. Thanks to this, you can run your Raspberry Pi programs directly on your computer.

** More informations about device, you can find in [README](https://github.com/mlab-modules/USBI2C01).
