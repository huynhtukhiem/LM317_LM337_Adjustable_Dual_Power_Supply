# Desription
This project was developed as the final assignment for the PCB Design course at Industrial University of Ho Chi Minh City (IUH). It also represents my first complete PCB project.

## Project Requirements
Design of a dual-polarity rectifier and linear voltage regulator circuit that generates adjustable positive and negative DC output voltages.

| Parameter | Requirement |
|-----------|-------------|
| PCB Design Software | Altium Designer 26 |
| PCB Layers | 1 Layers |
| Size | 70 x 70 mm |
| Input Voltage | 12V AC |
| Output Voltage | Adjustable positive and negative 5V DC |
| Maximum Output Current | Up to 1.5 A (with big heatsink) |
| IC Regulators | LM317 and LM337 |

## Schematic

## 3D view

## Calculations

1. Ouptut Voltage:

The output voltage of the LM317 and LM337 is determined by two resistors according to the following equation:

\[
V_{OUT}=V_{REF}\left(1+\frac{R_2}{R_1}\right)
\]

where:

- \(V_{REF}=1.25V\)
- \(R_1=240\Omega\)

For a target output voltage of **5V**:

\[
R_2
=
R_1\left(\frac{V_{OUT}}{V_{REF}}-1\right)
\]

Substituting the values:

\[
R_2
=
240
\left(
\frac{5}{1.25}-1
\right)
=
720\Omega
\]

Therefore, the recommended resistor values are:

| Component | Value |
|----------|-------|
| R1 | 240 Ω |
| R2 | 720 Ω |

The same calculation is applied to both the **LM317** (positive regulator) and **LM337** (negative regulator), resulting in regulated **+5V** and **−5V** outputs.
