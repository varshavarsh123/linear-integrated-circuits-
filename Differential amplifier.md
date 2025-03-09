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

Also we have to verify that the transistor is working in saturation region, this can be done by checking that whether VGD is greater than or lesser that Vt

For VGD=VG-VD=1.6-1.70

VGD = -0.10 , but Vt=0.489V

Hence VGD<Vt; therefore mosfets are in saturation region.

The give Vicm is 1.6 v let change it by increasing 1v and let observe the changes 

![1000039985](https://github.com/user-attachments/assets/81bbf5d4-b481-4a21-96ee-4965a1fcad2e)

As we can observe that the  current  is greater than o.4375mA
which is out of our power power budget hence its not useful for our design .A we can see Vp is also increased .

##Calculate maximum input swing and output swing

VICMmin = VT + VP (We are observing the condition of cut-off)

VT = 0.489 V , VP = 0.6 V
VICMmin = 1.089 V

VICMmax = VOCM + VT (We are observing the condition of MOSFET getting out of saturation region)

VT = 0.489V , VOCM = 1.7 V
VICMmax = 2.189V

Any inputs that makes the gate voltage less than this value will give clipped output.

# Transient Analysis  

Now we are ready for transient analysis, we take an input of 50mV (Amplitude) and 1.6 of dc offset  

## Input 

![1000039973](https://github.com/user-attachments/assets/cf1fb8e0-1f9c-4737-a786-295f158e558b)

## Output

![1000040010](https://github.com/user-attachments/assets/ee5893e7-9b58-41ad-a71e-12502166dffd)

## Both

![1000040011](https://github.com/user-attachments/assets/63a73331-2677-439b-b6c9-244ca8817932)


We can now calculate gain 
Av= - vout/vin
Av=(1.6484-1.5516)/(1.7678-1.6335)
Av= -1.389 V/V

nagetive sing inticates 180 degree phase shift  

# AC Analysis

![1000040012](https://github.com/user-attachments/assets/9410f990-335f-4faa-8040-4e4a465d6c3c)


From the graph the gain in db scale is 11.183db-3db= 8.183db

# Case 2 replace Rss with current source 


![1000040014](https://github.com/user-attachments/assets/2c4d5a2d-9496-48c9-a9d2-6c9d1a9b1e5b)


When you swap out resistor R3 for a current source , the circuit becomes a fully differential pair with an active current source. This change boosts the circuit's gain and improves its ability to block common signals that both inputs receive (CMRR). The current source ensures a steady bias current, making the circuit more stable even if component values change. Without R, the transconductance gm increases, resulting in a higher differential gain.

# DC Analysis 

![1000039957](https://github.com/user-attachments/assets/1669687d-de77-48c8-8059-dae5942f3407)

for mosfet M1 & M2:

Vocm = 1.70025v

ViCM = 1.6V

Id= 0.4375 mA

Vtn = 0.489v

VGS = 1.6 - 0.593613 = 1.01V

VDD = IdRd + VDS +Vp

VDS = 1.11

The Q-point of both the mosfets are (1.1V, 0.4375mA).

# Transient Analysis 

![1000039955](https://github.com/user-attachments/assets/47221451-e754-494f-ae41-8fc71d6b514f)

From the above observation

Gain Av=Vout(peak)/Vin(peak)
Av=1.863/1.65=1.129V/V

# AC Analysis

![1000039983](https://github.com/user-attachments/assets/5f981235-1611-4535-8fc4-7c97cd2c85c2)

From the graph , the gain in dB scale is 10.457dB - 3dB =7.457db


# Case 3 replace Rs by MOSFET

![1000039991](https://github.com/user-attachments/assets/4a02a69d-7fce-4e36-8fce-dbdf575afad5)

The value for Vb is given by Vb=Vtn+Vp=0.489+0.6=1.089V



