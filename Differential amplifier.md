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

![17415142999093036009038723477340](https://github.com/user-attachments/assets/9c6d118e-2a50-40a6-adb4-bd2360cf2526)




Given that the drain current is already established by the current source and the gates are tied to the ground node, the source voltage will settle on whatever value creates a gate-to-source voltage V_gs corresponding to a drain current of I_bias/2

# Design

Given p=2.8mW

since p=VddxIss

Iss = p/Vdd = 2.8m/3.2 = 0.875mA

Id1=Id2=Iss/2 = 0.4375mA

Applying KVL along the loop

Vdd-Id1×Rd-Vocm1=0

Rd=(Vdd-Vocm)/I1

Rd=(3.2-1.7)/0.4375x10^-3

Rd=3428ohm

Rss=Vp/Iss 
= 0.6/0.875m

Rss=685.7ohm

![1000039896](https://github.com/user-attachments/assets/e358409b-44a5-4e67-b3e2-c2a059c9af55)




