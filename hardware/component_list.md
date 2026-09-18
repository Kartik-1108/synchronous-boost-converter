# Hardware / Component List

| Section | Component | Value / Part |
|---|---|---|
| Gate driver | High/low-side driver | IR2110 |
| Power stage | MOSFET | IRF520 / IRF540* |
| Inductor | Power inductor | 33 µH |
| Gate resistor | Series | 27 Ω |
| Gate pull-down | Gate-source | 560 Ω |
| Bootstrap capacitor | Cboot | 10 µF |
| Bootstrap diode | Dboot | 1N4148 |
| Output capacitor | Electrolytic bank | 330 µF × 4 (as shown on prototype) |
| Level shifter | NPN transistor | BC547 |
| Load | Resistive | 20 Ω |

\* The hand-drawn prototype schematic is marked “IRF 520/540”; verify the exact
fitted MOSFET part number if the hardware becomes available again.
