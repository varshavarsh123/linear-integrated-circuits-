# Experiment:03
# Analysis of differential amplifier 

## AIM:Design a differential amplifier for the following specifications using ltspice

## Specifications 
+ Vdd =3.2 volts 
+ power <=2.8mW
+ Vicm=1.6V
+ Vocm=1.7V
+ Vp=0.6V  

perform DC Analysis, Transient Analysis, Frequency Response and find out required parameters.

# Overview 
A differential amplifier **amplifies the difference between two input signals** while ignoring any signals that are common to both inputs. It's like focusing on what makes two signals different and ignoring what makes them the same.
It's useful in reducing noise and is commonly used in devices like op-amps and communication systems. 

# Circuit diagram 

![1000039886](https://github.com/user-attachments/assets/01eaaf94-55dd-41bd-9024-965bf245c438)


### Working Principle

**Differential Input**: The circuit amplifies the difference between the two input voltages (Vin1 - Vin2)

**Current Source Biasing**: The total bias current (I bias) is constant, ensuring stable operation.

**Output Voltages**: The amplified signals appear at Vout1 and Vout2.

**Key Components**: The sum of the two drain currents Id1 and Id2 must equal I_bias . In this idealized analysis, both halves of the circuit are identical, meaning the two drain currents are equal.

### Currents

Let's assume for the moment that the transistors are in saturation. The equation for saturation-mode drain current is:



Given that the drain current is already established by the current source and the gates are tied to the ground node, the source voltage will settle on whatever value creates a gate-to-source voltage V_gs corresponding to a drain current of I_bias/2





