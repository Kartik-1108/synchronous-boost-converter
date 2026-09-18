# Experimental Results

## Recorded Operating Point

| Quantity | Experimental value |
|---|---:|
| Input voltage | 6 V |
| Output voltage | ≈ 11 V |
| Load | 20 Ω |
| Duty ratio | 0.5 |
| Switching frequency | ≈ 50.0002 kHz |
| Inductor | 33 µH |
| Input current | ≈ 1 A, observed from bench supply |

## Derived Quantities

From the 20 Ω load:

\[
I_o\approx0.55A
\]

\[
P_o\approx6.05W
\]

## Efficiency

Efficiency is intentionally **not reported** because the input current was only
observed approximately from the supply display and was not recorded with enough
precision to produce a defensible power-balance measurement.

A future test should simultaneously record:

\[
V_{in}, I_{in}, V_o, I_o
\]

and calculate:

\[
\eta=\frac{V_oI_o}{V_{in}I_{in}}\times100\%
\]

## Available Measurements

See the `measurements/` directory for the retained oscilloscope and supply
photographs.
