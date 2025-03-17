
Ranked from most difficult to least (not finished ranking)

• Operate up to 4 motors bidirectionally with the pins available to you (listed in the power pinout table). You will need to control 2x brushed DC motors which could each draw 200mA at the highest voltage of a 1S1P battery (the battery is further specified in the battery section).
The other 2x motors are for the auxiliary connection and need to operate 500mA each.

• Place an INA219 for monitoring the battery on the I2C Bus and configure it correctly with
respect to the hardware (cannot have BOTH A0 AND A1 on GND)

• Charge the battery from the 9V input pin (listed in the power pinout table).

• Have two charging modes for a higher and lower charging current for the battery (200mA, and approximately 600mA ±100mA from the battery perspective.

• Integrate USB C and get 9V out of the USB Host

• Provide 2x External Load Switching at 1A each (High Side connected to your 5V)

• Provide an ON/OFF switch. OFF state: battery draw <30uA. ON state: can provide your robot peak current of 2A. The switch needs to shut down 5V and 3V3.


• Provide a 3V3 5% accuracy (300mA max) and 5V Out 5% accuracy (1.5A max)
