

#### Place an INA219 for monitoring the battery on the I2C Bus and configure it correctly with respect to the hardware (cannot have BOTH A0 AND A1 on GND)

**USB-C PD Trigger Module**: A small board that negotiates the desired voltage (e.g., 9V) with the charger. Examples include the "USB-C PD Decoy" or "WUSB3801" modules.

https://www.usb.org/sites/default/files/USB%20Type-C%20Spec%20R2.0%20-%20August%202019.pdf

USB PD 
https://jlcpcb.com/parts/2nd/Power_Management_(PMIC)/USB_PD_1639

• Have two charging modes for a higher and lower charging current for the battery (200mA, and approximately 600mA ±100mA from the battery perspective.

• Integrate USB C and get 9V out of the USB Host

• Charge the battery from the 9V input pin (listed in the power pinout table).
