# Design Calculations

## Given

| Parameter | Value |
|---|---:|
| Input voltage, Vin | 6 V |
| Output voltage, Vo | ≈ 11 V |
| Duty ratio, D | 0.5 |
| Switching frequency, fs | ≈ 50 kHz |
| Inductor, L | 33 µH |
| Load resistance, R | 20 Ω |

---

## Ideal Boost Conversion

For an ideal boost converter operating in CCM:

$$
V_o = \frac{V_{in}}{1-D}
$$

For \(V_{in}=6\,V\) and \(D=0.5\):

$$
V_o = \frac{6}{1-0.5}
$$

$$
\boxed{V_o = 12\,V}
$$

The experimentally observed output voltage was approximately:

$$
\boxed{V_o \approx 11\,V}
$$

The difference between the ideal and experimental values can be attributed
to practical non-idealities such as MOSFET voltage drops, inductor resistance,
switching losses, dead time, wiring resistance, and parasitic elements.

---

## Switching Period

The switching period is:

$$
T_s = \frac{1}{f_s}
$$

For \(f_s \approx 50\,kHz\):

$$
T_s =
\frac{1}{50\times10^3}
$$

$$
\boxed{T_s = 20\,\mu s}
$$

---

## Inductor Ripple Current

For a boost converter operating in CCM, the inductor ripple current is:

$$
\Delta I_L =
\frac{V_{in}D}{Lf_s}
$$

Substituting the design values:

$$
\Delta I_L =
\frac{6(0.5)}
{(33\times10^{-6})(50\times10^3)}
$$

Therefore:

$$
\boxed{\Delta I_L \approx 1.82\,A}
$$

The relatively large ripple current is an important consideration when
selecting the inductor and evaluating conduction losses.

---

## Output Current

With a resistive load of:

$$
R = 20\,\Omega
$$

and measured output voltage of approximately:

$$
V_o \approx 11\,V
$$

the output current is:

$$
I_o = \frac{V_o}{R}
$$

$$
I_o = \frac{11}{20}
$$

$$
\boxed{I_o \approx 0.55\,A}
$$

---

## Output Power

The output power delivered to the resistive load is:

$$
P_o = \frac{V_o^2}{R}
$$

Substituting \(V_o \approx 11\,V\) and \(R=20\,\Omega\):

$$
P_o = \frac{11^2}{20}
$$

$$
P_o = \frac{121}{20}
$$

$$
\boxed{P_o \approx 6.05\,W}
$$

---

## Critical Inductance

For an ideal boost converter, the critical inductance separating CCM and DCM
can be calculated as:

$$
L_{crit} =
\frac{D(1-D)^2R}{2f_s}
$$

Using:

- \(D=0.5\)
- \(R=20\,\Omega\)
- \(f_s=50\,kHz\)

$$
L_{crit} =
\frac{0.5(1-0.5)^2(20)}
{2(50\times10^3)}
$$

Therefore:

$$
\boxed{L_{crit}=25\,\mu H}
$$

The selected inductance is:

$$
L = 33\,\mu H
$$

Since:

$$
33\,\mu H > 25\,\mu H
$$

the operating point is **predicted to be in CCM under the idealized model**.

Actual CCM operation should be verified experimentally using the inductor-current
waveform.

---

## Input Power and Efficiency

The bench power supply indicated an input current of approximately:

$$
I_{in} \approx 1\,A
$$

However, this value was only observed approximately from the supply display and
was not recorded as a precise measurement.

Using the approximate value:

$$
P_{in} \approx V_{in}I_{in}
$$

$$
P_{in} \approx 6\times1
$$

$$
\boxed{P_{in}\approx6\,W}
$$

The estimated output power is approximately:

$$
P_o\approx6.05\,W
$$

These approximate values would imply an apparent efficiency slightly above
100%, which is physically impossible for a real converter.

Therefore, **no measured efficiency is claimed in this project**.

The apparent discrepancy is attributed to the limited precision of the
retrospectively observed input-current value and the fact that the input and
output quantities were not measured simultaneously.

For a proper efficiency measurement, the following quantities should be
measured under the same operating condition:

$$
V_{in},\quad I_{in},\quad V_o,\quad I_o
$$

The converter efficiency can then be calculated as:

$$
\boxed{
\eta =
\frac{V_o I_o}
{V_{in} I_{in}}
\times100\%
}
$$

---

## Summary of Calculated Parameters

| Parameter | Value |
|---|---:|
| Input voltage | 6 V |
| Duty ratio | 0.5 |
| Switching frequency | ≈ 50 kHz |
| Switching period | 20 µs |
| Inductor | 33 µH |
| Inductor ripple current | ≈ 1.82 A |
| Load resistance | 20 Ω |
| Output voltage | ≈ 11 V |
| Output current | ≈ 0.55 A |
| Output power | ≈ 6.05 W |
| Critical inductance | 25 µH |
| Predicted operating mode | CCM |

> **Note:** The CCM classification is based on the idealized critical-inductance
> calculation. Experimental verification requires the actual inductor-current
> waveform.
