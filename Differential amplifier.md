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

Applying KVL for the loop

Vdd - (Id1×Rd) - Vocm1=0

Rd=(Vdd-Vocm)/I1

Rd=(3.2-1.7)/0.4375x10^-3

Rd=3.428kohm

Rss=Vp/Iss 
= 0.6/0.875m

Rss=0.6857kohm


# Case 1  with Rss


![1000039896](https://github.com/user-attachments/assets/e358409b-44a5-4e67-b3e2-c2a059c9af55)

# DC Analysis

Now we set DC Operating Point of the circuit



![1000040002](https://github.com/user-attachments/assets/6c1601eb-ee81-43cc-87e6-ffd6c1921760)

But for the exact output voltage of 1.7 v we get little more current where it exceeds our power budget .Hence by varying w and l we have to set Operating point under our power budget .

![1000039975](https://github.com/user-attachments/assets/de853bf4-8931-4a67-acaa-efdd59690cee)

![1000039977](https://github.com/user-attachments/assets/887b6a46-aee2-4fa8-9cca-5e375b7bd470)

Now this Operating point is under our power budget .

In the data sheet of ltspice the treshold voltage mentioned as 0.366v
but while doing dc analysis the treshold voltage is changed to 0.489v thi is due to body effect.

The give Vicm is 1.6 v let change it by increasing 1v and let observe the changes 

![1000039985](https://github.com/user-attachments/assets/81bbf5d4-b481-4a21-96ee-4965a1fcad2e)

As we can observe that the  current  is greater than o.4375mA
which is out of our power power budget hence its not useful for our design .A we can see Vp is also increased .






