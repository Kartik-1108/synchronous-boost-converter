# Design Calculations

## Given

- \(V_{in}=6V\)
- \(V_o\approx11V\)
- \(D=0.5\)
- \(f_s\approx50kHz\)
- \(L=33\mu H\)
- \(R=20\Omega\)

## Ideal Boost Conversion

\[
V_o=\frac{V_{in}}{1-D}
\]

\[
V_o=\frac{6}{0.5}=12V
\]

Measured:

\[
V_o\approx11V
\]

## Switching Period

\[
T_s=\frac{1}{f_s}
=\frac{1}{50\times10^3}
=20\mu s
\]

## Inductor Ripple

\[
\Delta I_L=\frac{V_{in}D}{Lf_s}
\]

\[
\Delta I_L\approx1.82A
\]

## Output Current

\[
I_o=\frac{V_o}{R}
=\frac{11}{20}
=0.55A
\]

## Output Power

\[
P_o=\frac{V_o^2}{R}
=\frac{121}{20}
=6.05W
\]

## Critical Inductance

\[
L_{crit}=
\frac{D(1-D)^2R}{2f_s}
\]

\[
L_{crit}=25\mu H
\]

Since \(33\mu H>25\mu H\), CCM is predicted by the idealized model.

## Important Note

The input-current observation of approximately 1 A is too coarse to use for a
credible efficiency claim. With 6 V and 1 A, the estimated input power is
approximately 6 W, which is lower than the estimated 6.05 W output power.
This is a measurement-accuracy issue, not evidence of >100% efficiency.
