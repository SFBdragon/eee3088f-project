
• Integrate USB C and get 9V out of the USB Host


---


https://www.usb.org/sites/default/files/USB%20Type-C%20Spec%20R2.0%20-%20August%202019.pdf

USB PD 
https://jlcpcb.com/parts/2nd/Power_Management_(PMIC)/USB_PD_1639


Relevant pins:

| Pin No | Name               | Purpose                                   |
| ------ | ------------------ | ----------------------------------------- |
| 13     | `FAST_CHARGE_CTRL` | Logic-level signal for fast charge ON/OFF |
| 14     | `BATTERY`          | Connect to VBAT+                          |
| 19     | `GND`              | Connect to GND                            |
| 22     | `HV`               | Connect to 9V from USB PD                 |

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

https://www.ti.com/lit/ds/symlink/tusb320.pdf?ts=1745478480336
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
