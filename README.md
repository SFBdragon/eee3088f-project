# EEE3088F Project

> Power board for a micro-mouse [(Veritasium video)](https://www.youtube.com/watch?v=ZMQbHMgK2rw) designed for EEE3088F Design Principles @ UCT

#### Team #69

- Shaun Beautement
- Adedamola Yusuff

### Project Description

The board aims to meet the following requirements:
- Operate up to 4 motors bidirectionally 
    - Controls 2x brushed DC motors which could each draw 200mA @ 4.2V
    - Controls 2x motors at 500mA each.
- Monitor the battery using an INA219
- Charge the battery from USB supply
- Two charging modes the battery: IBAT = 200mA, or 600mA ±100mA
- Integrate USB C and get 9V out of the USB Host
- Provide 2x high-side external load switching with 5V regulated supply, drawing at most 1A each
- Provide a 3V3 5% accuracy (300mA max) and 5V Out 5% accuracy (1.5A max)
- Provide an ON/OFF switch.
    - OFF state: battery draw <30uA.
    - ON state: can provide your robot peak current of 2A.

The board is designed to be printable with PCBA for most components for under $70 with JLCPCB. (As-is, the design costs about $50, not including the JST and 2x16 connector, which was provided to us.)

The board is shaped to fit to and interface with
- [Justin Pead](https://ebe.uct.ac.za/department-electrical-engineering/contacts/justin-pead)'s micro-mouse (2025 version)
- a [1s1p LiPo battery](https://www.robotics.org.za/802540)
- a USB C cable (USB v2 and v3 should work) for charging

### Software

The schematic and PCB design is drafted in [KiCAD](https://www.kicad.org/).

Our working notes are included under `notes/` and are best viewed in [Obsidian](https://obsidian.md/). (Even better, not viewed at all ^-^)

### License 

CERN Open Hardware Licence Version 2 - Permissive

See [LICENSE.md](./LICENSE.md)
