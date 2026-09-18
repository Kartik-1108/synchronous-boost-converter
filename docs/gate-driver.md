# Gate Driver Design

## IR2110

The prototype uses an IR2110 high/low-side gate driver to drive the
synchronous MOSFET pair.

The driver provides:

- High-side gate output (HO)
- Low-side gate output (LO)
- Bootstrap-based high-side supply
- Separate gate-drive paths

## Bootstrap Network

The prototype uses:

- 10 µF bootstrap capacitor
- 1N4148 bootstrap diode

The bootstrap network supplies the floating high-side driver during operation.

## Gate Network

Each MOSFET gate includes:

- 27 Ω series gate resistor
- 560 Ω gate-to-source pull-down

The series resistor controls gate charging/discharging current and switching
speed while helping manage ringing. The pull-down provides a defined OFF-state
gate voltage.

## Level Shifting

BC547 transistor stages were used to interface the PWM/control signals with
the gate-driver input stage.

## Future Characterization

The following measurements should be captured in a future hardware session:

1. High-side \(V_{GS}\)
2. Low-side \(V_{GS}\)
3. Dead time
4. Switching-node voltage
5. Gate ringing
6. Rise/fall times
7. Bootstrap-voltage behavior
