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

### Output voltage

```text
VOUT = VREF × (1 + R2/R1)
```

According to datasheet:

- **VREF** = 1.25 V
- **R1** = 240 Ω

To obtain an output voltage of **5 V**:

```text
R2 = R1 × (VOUT / VREF − 1)

R2 = 240 × (5 / 1.25 − 1)

R2 = 240 × (4 − 1)

R2 = 720 Ω
```

==> Selected Resistor Values:R1 = 240 Ω and R2 = 720 v.
==> choose Variable Resistor = 1k Ω

The same resistor values are used for both the **LM317** and **LM337** to obtain regulated **+5 V** and **−5 V** outputs.

### LED Current Limiting Resistor

The LED current limiting resistor is calculated using Ohm's law:

```text
R = (VS - VF) / IF
```

Where:

- Supply Voltage (VS) = 5 V
- LED Forward Voltage (VF) ≈ 2.0 V
- LED Forward Current (IF) = 10 mA

Calculation:

```text
R = (5 - 2) / 0.01

R = 300 Ω
```

