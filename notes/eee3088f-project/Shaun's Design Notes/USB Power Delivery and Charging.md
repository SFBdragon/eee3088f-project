
• Have two charging modes for a higher and lower charging current for the battery (200mA, and approximately 600mA ±100mA from the battery perspective.

• Integrate USB C and get 9V out of the USB Host

• Charge the battery from the 9V input pin (listed in the power pinout table).


---


https://www.usb.org/sites/default/files/USB%20Type-C%20Spec%20R2.0%20-%20August%202019.pdf

USB PD 
https://jlcpcb.com/parts/2nd/Power_Management_(PMIC)/USB_PD_1639


Relevant pins:

| Pin No | Name               | Purpose                                                      |
| ------ | ------------------ | ------------------------------------------------------------ |
| 9      | `USART2_RX`        |                                                              |
|        |                    |                                                              |
|        |                    |                                                              |
| 13     | `FAST_CHARGE_CTRL` | Control the current to charge at. TODO: VSCS? What voltages? |
| 14     | "Battery"?         |                                                              |
| 19     | `GND`              |                                                              |
| 22     | `HV`               | Connect to 9V                                                |

CH224K
https://jlcpcb.com/partdetail/wch_jiangsu_Qin_heng-CH224K/C970725
??????????
https://www.laskakit.cz/user/related_files/ch224ds1.pdf
YESSSSSSSSSSSSSSSSS

ACTUALLY NEEDS MAX12 AND THERE'S NONE AVAILABLE
https://jlcpcb.com/partdetail/Injoinic-IP2721/C603176
https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8588893818120769536
IP2721
Can request 9V directly without uC


https://www.ti.com/cn/lit/ds/symlink/tusb320lai.pdf?ts=1742499259027
Not sure if this actually does what I need

https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8589839603521269760
same deal

https://www.nxp.com/docs/en/data-sheet/PTN5150A.pdf
?

https://www.st.com/resource/en/datasheet/stusb4500.pdf
Definitely can do what I need.
$1.78 https://jlcpcb.com/partdetail/Stmicroelectronics-STUSB4500QTR/C2678061
NOT BY DEFAULT

https://www.ti.com/lit/ds/symlink/tps25730.pdf?ts=1742514233405
also seems stupidly overkill

**FUSB302B**
https://jlcpcb.com/partdetail/Onsemi-FUSB302BMPX/C132291
not passively usable?

USB C connector
**NEED TO BUY**

Battery connector
https://www.robotics.org.za/JST-PH-2P-90?search=jst
no need to buy

Battery Management
https://jlcpcb.com/partdetail/TexasInstruments-BQ24610RGER/C19384
Seems overkill

https://jlcpcb.com/partdetail/solaic-SLM6305/C711584
Seems good? (handles a wide range of voltages, stocked, can control $I_{bat}$ )
https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8588917360790659072



2x16 pins
no need to buy

| Pin No | Name        | Purpose |
| ------ | ----------- | ------- |
| 9      | `USART2_RX` |         |
| 12     | `USART2_TX` |         |
| 16     | `I2C1_SCL`  |         |
| 17     | `I2C1_SDA`  |         |


