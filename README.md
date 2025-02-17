# Experiment-01
# DC ,AC,Transient Analysis of Common Source Amplifier Circuit-1
![1000036739](https://github.com/user-attachments/assets/18b4ee75-4916-4e6e-9390-801c31fce430)

## Abstract :
In this experiment, we study a Common Source Amplifier in three ways. First, we do DC analysis to check how the circuit behaves with a steady DC voltage and determine its biasing conditions. Next, we perform AC analysis to see how the amplifier responds to different frequencies. Finally, we conduct transient analysis to observe how the amplifier amplifies signals over time and measure its gain and output.

## Introduction:
A Common Source (CS) amplifier is a popular MOSFET-based amplifier. In DC analysis, we find the operating point (Q point) by calculating voltages and current (Vgs, ID, and Vds) to ensure the MOSFET works in the right mode. AC analysis helps us understand how the amplifier responds to small signals, including its gain and impedance. Transient analysis checks how the amplifier reacts to changes in the input signal over time.
 
## Components 
This circuit consist of TSMC 180nm NMOS transistor (CMOSN) , drain resistor and voltage sources (V1 & V2) .
Threshold voltage : 0.36v
Resistor : 1k,Supply voltage : 1.8v  input voltage :0.9v
Amplitude : 50mv , Frequency : 1KHz.

# Analysis

## 1.DC Analysis 

### Circuit 

![1000036739](https://github.com/user-attachments/assets/08fd5218-df5f-4a79-99fe-b476d23aa114)

### Calculation :

![1000036774](https://github.com/user-attachments/assets/0b5c1a82-cd67-4cd4-8890-81f5dad878d2)

As per the Calculation the the required id is 27.78×10^-6 A
and output voltage Vd 1.77v 
with W/L ratio more are less 1.22
in ltspice by varying ratio by trail and error method we can find desired current value .

## DC Analysis Output 

![1000036740](https://github.com/user-attachments/assets/31d04ead-a9d4-4b29-b400-0126cc039683)

![1000036741](https://github.com/user-attachments/assets/88a03f49-e208-4333-a357-6cc5e642e1c5)

### The tried ratios of W/L

![1000036742](https://github.com/user-attachments/assets/5f0e45f9-fa6c-45e8-899b-3446235fe36a)

![1000036743](https://github.com/user-attachments/assets/651877c0-964e-4da0-a8cc-f84151d68cbd)

![1000036745](https://github.com/user-attachments/assets/426170aa-608c-49f8-90a4-0105ed707bf2)

![1000036744](https://github.com/user-attachments/assets/f1a3af9f-fd9c-44dd-952d-e36cc72ca7b3)




