# Experimental Results

## Recorded Operating Point

| Quantity | Experimental Value |
|---|---:|
| Input voltage | 6 V |
| Output voltage | ≈ 11 V |
| Load resistance | 20 Ω |
| Duty ratio | 0.5 |
| Switching frequency | ≈ 50.0002 kHz |
| Inductor | 33 µH |
| Input current | ≈ 1 A* |

\* The input current was approximately observed from the laboratory power
supply display and was not recorded as a precise measurement.

---

## Derived Quantities

### Output Current

Using the measured output voltage and the 20 Ω resistive load:

$$
I_o = \frac{V_o}{R}
$$

$$
I_o = \frac{11}{20}
$$

$$
\boxed{I_o \approx 0.55\,A}
$$

### Output Power

The estimated output power is:

$$
P_o = \frac{V_o^2}{R}
$$

$$
P_o = \frac{11^2}{20}
$$

$$
\boxed{P_o \approx 6.05\,W}
$$

---

## Input Power and Efficiency

The laboratory power supply indicated an input current of approximately
1 A.

Using this approximate value:

$$
P_{in} \approx V_{in}I_{in}
$$

$$
P_{in} \approx 6\times1
$$

$$
P_{in} \approx 6\,W
$$

However, the input current was only observed approximately from the supply
display. It was not measured with sufficient precision or simultaneously
with the output quantities.

The estimated output power is approximately:

$$
P_o \approx 6.05\,W
$$

Using these approximate values would result in an apparent efficiency slightly
above 100%, which is physically impossible for a real converter.

Therefore, **no measured efficiency is claimed for this experiment**.

This discrepancy is attributed to the limited precision of the retrospectively
observed input-current value and the lack of simultaneous input and output
power measurements.

---

## Recommended Efficiency Measurement

For a future experimental session, the following quantities should be measured
under the same operating condition:

$$
V_{in},\quad I_{in},\quad V_o,\quad I_o
$$

The converter efficiency can then be calculated as:

$$
\eta =
\frac{V_o I_o}
{V_{in} I_{in}}
\times 100\%
$$

This will provide a reliable experimental efficiency measurement.

---

## Available Measurements

The repository contains the experimental photographs and oscilloscope
measurements retained from the original laboratory session.

### Switching Waveform

The oscilloscope measurement indicates a switching frequency of approximately:

$$
\boxed{f_s \approx 50.0002\,kHz}
$$

See:

`measurements/Switch_waveform.jpg`

### Input Supply

The laboratory power-supply measurement showing the approximately 6 V input
and approximately 1 A input-current observation is available in:

`measurements/input_supply.jpg`

### Hardware

Photographs of the assembled converter and laboratory setup are available in
the `photos/` directory.

---

## Experimental Limitations

The following measurements were not retained from the original experiment:

- High-side MOSFET \(V_{GS}\)
- Low-side MOSFET \(V_{GS}\)
- Switching-node voltage \(V_{SW}\)
- Dead-time measurement
- Inductor-current waveform
- Precise input current
- Precise output current
- Measured converter efficiency
- Switching transient and ringing characterization

These measurements are listed as future characterization work rather than
being estimated or reconstructed from unavailable data.
