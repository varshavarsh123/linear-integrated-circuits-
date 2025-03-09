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

**Differential Input**: The circuit amplifies the difference between the two input voltages \((V_{IN1} - V_{IN2})\).

**Current Source Biasing**: The total bias current \((I_{BIAS})\) is constant, ensuring stable operation.

**Output Voltages**: The amplified signals appear at \(V_{OUT1}\) and \(V_{OUT2}\).

**Key Components**: The sum of the two drain currents \(I_D1\) and \(I_D2\) must equal \(I_{BIAS}\). In this idealized analysis, both halves of the circuit are identical, meaning the two drain currents are equal.

### Currents

Let's assume for the moment that the transistors are in saturation. The equation for saturation-mode drain current is:

\[ I_{D} = \frac{1}{2} \mu_n C_{ox} \frac{W}{L} (V_{GS} - V_{TH})^2 \]

Given that the drain current is already established by the current source and the gates are tied to the ground node, the source voltage will settle on whatever value creates a gate-to-source voltage \((V_{GS})\) corresponding to a drain current of \(\frac{I_{BIAS}}{2}\).





