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

### The trail ratios of W/L:

![1000036742](https://github.com/user-attachments/assets/5f0e45f9-fa6c-45e8-899b-3446235fe36a)

![1000036743](https://github.com/user-attachments/assets/651877c0-964e-4da0-a8cc-f84151d68cbd)

![1000036745](https://github.com/user-attachments/assets/426170aa-608c-49f8-90a4-0105ed707bf2)

![1000036744](https://github.com/user-attachments/assets/f1a3af9f-fd9c-44dd-952d-e36cc72ca7b3)

![1000036746](https://github.com/user-attachments/assets/609481c8-3331-4823-9547-5fcf0df862ba)

![1000036747](https://github.com/user-attachments/assets/a64e3ad0-98bf-4032-8c4a-6544ded56662)

###  From Analysis 
 we got out voltage 1.77v
 and current Id 27.73×10^-6A
 as we expected in our Calculation
 for the power dissipation 50u w.
 and as we calculated and verified in our calculation this DC Operating point confirms that NMOS
 Operates in saturation region. 
 
 ## 2.AC Analysis 

Output 
![1000036750](https://github.com/user-attachments/assets/0f7df383-24da-49b0-9aa5-e33826fb278b)

In AC analysis, we test how a circuit behaves at different frequencies to see where it works well as an amplifier.

We do this by gradually increasing the frequency in steps of 10 times (decade sweep), starting from 0.1 Hz and going up to 1 THz.

## 3.Transient Analysis 

 Vout 

 ![1000036749](https://github.com/user-attachments/assets/9efcc9c7-51bb-4a5a-a08d-f1ac0b95350a)

 Vin

 ![1000036748](https://github.com/user-attachments/assets/fa21d3aa-5719-4981-9d4e-411de5a72357)

![1000036751](https://github.com/user-attachments/assets/f8290d9f-2d08-4197-8e6e-f22ef829bcda)

 In this analysis we determine the gain of the circuit. for input give sinusoidal voltage signal where the DC offset is 0.9v ,Frequency is 1kHz and Ac amplitude is 50m.select the stop time to 1ms.

Gain = Vin/Vout
Av= (1.777-1.767)v/(950m-850m)v= 0.1
This matches the theoritical value which is calculated by Av = gmRd.
where gm= KnVov
From the graph we can observe that there is 180 degree phase shift which is exhibited by Common Source Amplifier.

# Experiment-01
# DC ,AC,Transient Analysis of Common Source Amplifier Circuit-2
 
![1000036781](https://github.com/user-attachments/assets/529763a2-620b-40b8-ae98-af67c71a45e3)

In this circuit the resistor is replaced by pmos transistor.

This circuit consist of TSMC 180nm NMOS and PMOS transistor (CMOSN) , drain resistor and voltage sources (V1 & V2) .
Threshold voltage : 0.36v,
Supply voltage : 1.8v , input voltage :0.9v
Amplitude : 50mv , Frequency : 1KHz. vb=?

## Calculation

![1000036797](https://github.com/user-attachments/assets/b90a2333-fbeb-4b76-828b-312f99b4ac0c)

## 1.DC Analysis 

![1000036782](https://github.com/user-attachments/assets/88924fed-456f-4bea-bab8-1d102d8de096)

## 2.AC Analysis 

![1000036783](https://github.com/user-attachments/assets/1e00d3cd-741f-4eff-b62d-55e3f9308d1a)

## 3.Transient analysis

Vout

![1000036784](https://github.com/user-attachments/assets/62a82ed9-acbf-466e-ac56-9f3ce5dbd46e)

Vin

![1000036785](https://github.com/user-attachments/assets/0326be38-5b4a-44db-87e7-541a9e9d0dbe)


 # Inference 

In this experiment, we analyzed a Common Source Amplifier using DC, AC, and Transient analysis to understand its behavior.

1. DC Analysis

The biasing conditions were determined, ensuring that the NMOS transistor operates in the saturation region.

The operating point (Q-point) was verified with expected values of Id = 27.73 µA and Vd = 1.77V, confirming the correctness of theoretical calculations.

The W/L ratio was adjusted experimentally in LTSpice to achieve the desired drain current, showing how transistor sizing affects circuit performance.

2. AC Analysis

The amplifier's frequency response was examined using a decade sweep from 0.1 Hz to 1 THz to understand gain variations across different frequencies.

The gain (Av) was theoretically calculated using gmRd, and the measured gain matched expectations, validating the small-signal model approach.

3. Transient Analysis

A sinusoidal input with DC offset = 0.9V, amplitude = 50mV, and frequency = 1kHz was applied.

The amplifier exhibited a 180-degree phase shift, confirming the inverting nature of the Common Source Amplifier.

The measured gain of 0.1 matched theoretical predictions, proving the circuit's correct operation.

4. Comparison of Resistor Load vs. PMOS Load

The second circuit replaces the drain resistor with a PMOS transistor, forming an active load.

This likely improves gain and output swing, as PMOS active loads provide higher resistance compared to a simple resistor.

The bias voltage Vb for PMOS must be chosen properly to maintain it in the saturation region, ensuring proper amplification.

## Conclusion:
Our analysis confirmed that the amplifier works as expected, with proper biasing, frequency response, and signal amplification.









