# Electronics Design

This document is a summary of some practical electronic circuit design
considerations that may not have shined through in ECE110L/BME354L.

## Pull-up/down resistors
* We do not want floating inputs!
* Toggle digital input with switch.

## Detecting button press with MCU
* Interrupts!  Not dependent on `loop()` execution time.
* High priority; must execute quickly.
* Typically toggle Boolean state variable.
* Generic approach for any event detection.

## Pulse Width Modulation (PWM) 
* Modulate the "on" time of a digital output signal.
* Can be LPF to create analog output.

## LED
* Must use in series resistor to handle extra voltage drop from digital output.
* Can modulate brightness with PWM.
* Can also module brightness with current modulation (requires more components).

## Voltage Regulators
* Produce a constant output voltage for input voltage higher than desired output.
* Handles power fluctuations / discharging sources.
* Dissipates appreciable energy (commonly equipped with a heat sink).

## Voltage Protection (Voltage Clippers / Limiters)
* Use of diodes to prevent voltage spikes from causing component damage.
* Protection is related to diode threshold voltage and DC offset.

## Bypass Capacitors
* Stabalize "constant" voltage sources.
* Act as LPF.
* Should be as close to source pin as possible.
* Usually tenths of a uF.

## Example Arduino Code
* https://github.com/mlp6/ADPL/tree/master/software/ADPL_electron
* Software flowchart

## Electronic Design Automation (EDA)
* Utilize information about part footprints to layout PCBs.
* Simulate circuit behavior.
* [EDA Overview](EDA.md)
