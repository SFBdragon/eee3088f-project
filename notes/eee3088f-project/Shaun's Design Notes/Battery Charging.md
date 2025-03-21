
• Charge the battery from the 9V input pin (listed in the power pinout table).

• Have two charging modes for a higher and lower charging current for the battery (200mA, and approximately 600mA ±100mA from the battery perspective.

---

Input: 9V

Output: $V_{BAT}$ iff not charging, else nada

$I_{BAT}$ = 200mA - 600mA ($\pm 100$mA)


| Part                                                                                      | Usable | Reason                                                  | JLC                                                                        |
| ----------------------------------------------------------------------------------------- | ------ | ------------------------------------------------------- | -------------------------------------------------------------------------- |
| TP5000                                                                                    | No     | 9V max VIN                                              |                                                                            |
| TP4056                                                                                    | No     | 8V max VIN                                              |                                                                            |
| MAX8903                                                                                   | No     | Low stock, linear instead of buck (too much power dis.) |                                                                            |
| [FM4057S52](https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8588918019694845952) | Yes    | linear, not buck                                        | [link](https://jlcpcb.com/partdetail/Shenzhen_FumanElec-FM4057S52/C841288) |
| [SLM6305](https://jlcpcb.com/partdetail/solaic-SLM6305/C711584)                           | Yes    | Main issue: weird package and setup                     | [link](https://jlcpcb.com/partdetail/solaic-SLM6305/C711584)               |
| [TP5100](https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8588884095233769472)    | Yes    | Main issue: complicated setup                           | [link](https://jlcpcb.com/partdetail/solaic-SLM6305/C711584)               |
| BQ24610RGER                                                                               |        | Seriously overkill (2x costs $1.7), lots of             |                                                                            |
|                                                                                           |        |                                                         |                                                                            |

XL1059 (buck converter IC, basic)
+FM407S42 (linear battery management IC for charging control)
+MOSFET switching the resistance







Ignore all of this, I went with something else...

SLM6305 calculations:

$R_{s,eff,fast} = \frac{0.0667}{I_{BAT}} =  \frac{0.0667}{0.6} = 111m\Omega$
$R_{s,eff,slow} = \frac{0.0667}{I_{BAT}} = \frac{0.0667}{0.2} = 333.5m\Omega$

We need more resistance when FAST is LOW.

MOSFET gate and source are roughly 4.2V
Requires logic low to turn on.
So P channel MOSFET

$R_{s,always} = R_{s,eff,fast} - R_{DS,on} = 0.111 - (0.048||R_{s,bypass})$
$R_{s,bypass} = R_{s,eff,slow} - R_{s,always} = 0.3335 - R_{s,always}$

$R_{s,always} = 70.4m\Omega$
$R_{s,bypass} = 263.1m\Omega$


We need to invert the input.

$R_{s,slow} = R_{s,eff,slow} - R_{DS,on} = $

