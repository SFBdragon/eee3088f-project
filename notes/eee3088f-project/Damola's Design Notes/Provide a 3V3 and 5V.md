Provide a 3V3 5% accuracy (300mA max) and 5V Out 5% accuracy (1.5A max)

## Thoughts:
Just use voltage regulators, no?
Indeed, no.

## Decisions:

$V_{out}=V_{ref}\times(1+\frac{R_{3}}{R_{4}})$ 
$\frac{V_{out}}{V_{ref}}-1=\frac{R_{A}}{R_{B}}$

$V_{ref}=0.6V$ (typical)

$V_{out1}=5V$
$V_{out2}=3V3$

### Resistor Options for 5V (Boost Converter):

$\frac{V_{out1}}{0.6}-1=\frac{R_{3}}{R_{4}}$
$\frac{5}{0.6}-1=\frac{R_{3}}{R_{4}}$
$7.33=\frac{R_{3}}{R_{4}}$

$R_{4}=1000\Omega$
$R_3=6800\Omega+510\Omega$  $(7.31)$

$R_{4}=1300\Omega$
$R_3=9100\Omega+510\Omega$  $(7.39)$

$R_{4}=1800\Omega$
$R_3=13000\Omega+200\Omega$  $(7.33)$

The one above looks very good but will the $200\Omega$ survive the current?
$R_4=1800\Omega$ 
$R_3=11000\Omega+2200\Omega$  $(7.33)$ is better. (This became $R_3$ and $R_7$)


## Resistor Options for 5V (Buck-Boost Converter):

$R_1=R_2\times(\frac{V_{OUT}}{V_{FB}}-1)$
$\frac{R_1}{R_2}=(\frac{V_{OUT}}{V_{FB}}-1)$
$V_{FB}=0.5V$
$V_{OUT}=5V$
$\frac{R_1}{R_2}=\frac{5}{0.5}-1$
$\frac{R_1}{R_2}=9$
$R_1=(4.3\times10^{x})+(4.7\times10^{x})$
$R_2=1.0\times10^{x}$

The current through the resistive divider should be about 100 times greater than the
current into the FB pin.

The typical current into the FB pin is 0.01μA and the voltage across the resistor between
FB and GND, R2, is typically 500 mV. Based on these two values, the recommended value for R2 should be lower than 500kΩ (Because $500k\Omega=\frac{500mV}{0.01μA\times100}$).

Therefore, we can choose:
$R_2=100k$
and $R_1=430k\Omega+470k\Omega$

## Choosing an inductor for the 5V Buck-Boost converter

The larger the inductor value, the smaller the inductor ripple current and the lower the conduction losses of the converter. Conversely, larger inductor values cause a slower load transient response

The datasheet tells me what to choose.

0.63