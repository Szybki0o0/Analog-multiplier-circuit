# Analog Multiplier circuit

## Overview
The multiplier circuit presented in the schematic is an electronic system composed of several functional blocks working together to perform mathematical operations on input signals.

![mult](https://github.com/user-attachments/assets/2a41cb6e-7fd3-4901-ae9d-5d6ee5dde25d)

## Main Functional Blocks
The schematic consists of the following key sections:

1. **Power Supply (V+ and V-)**  
   - Voltage stabilization for the circuit.
   - Uses **MIC5207** for V+ regulation and **LT1054** as a charge pump for V-.

2. **Charge Pump**  
   - Responsible for generating the negative voltage required for some components.  
   - Utilizes **MCP6002** as an operational amplifier.
   - Utilizes **ADG779** as a CMOS switch.

3. **Voltage-Frequency Converter (VCF)**  
   - Based on **LM331N** operational amplifier, responsible for controlling the input signal through filtering.  
   - Includes adjustment via **RV1** potentiometer.

4. **Adding Offset**  
   - Allows adding a frequency shift to the input signal to allow correct operation with 0V.  
   - Implemented using **MCP6002**.

5. **Subtracting Offset**  
   - Compensates voltage by subtracting an offset value.  
   - Uses **MCP6002** and **RV2** potentiometer.

## How It Works
The circuit receives an input signal, which can be filtered and modified by adding or subtracting an offset. The processed signal is then transmitted to other circuit blocks where it can be used for further operations.

## Problems
VCF isn't working properly due to wrong choice of resistors and not enough current is flowing into integrated circuit.

## PCB
Physical implementation of a circuit:

![image](https://github.com/user-attachments/assets/b2ab5f1f-f99b-4c22-9b39-64033af195a4)

## Author
Jakub Konior
Jakub Wiącek
Arkadiusz Kowalczyk

## Design Software
Designed using **KiCad EDA 8.0.2**.
