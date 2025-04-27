## Experiment -6 
## Current Mirror

**Aim : Design a current mirror circuit which has a gain of AV = -10V/V, power supply of Vdd = 1.8V, and power of P <= 1mW. Find reference current (Iref), output current (Id), and total current (Itotal). Perform DC and AC analysis for mirror ratio 1:1, 1:2. Vary length from 180nm -> 500nm -> 1µm and do the analysis.** <br>

**Introduction to Current Mirror**<br>

 <p> The current mirror circuits are simple current sources which gives constant current. The current mirror circuits are based on the principle that, if the gate to source voltage of two identical MOSFETs are equal then the drain current flowing through them is equal. The basic current mirror circuit is shown in Figure below.</p>

 ![Image](https://github.com/user-attachments/assets/a7293d41-62b4-46a2-8ce7-5bcd00543125)

 <ins>Observed Table</ins> <br>
For I<sub>ref</sub> = 100u <br>

  <table> 
<tr>
 <th><b>I<sub>out(expected)</sub>(A)</b></th>
 <th><b>I<sub>out(appeared)</sub>(A)</b></th>
 <th><b>(W/L)<sub>2</sub>(m)</b></th>
 <th><b>(W/L)<sub>1</sub>(m)</b></th>
 <th><b>V<sub>x</sub>(V)</b></th>
 <th><b>V<sub>out</sub>(V)</b></th>
</tr>
<tr>
    <td>100µ</td>
    <td>103.5µ</td>
    <td>(180n/180n)</td>
    <td>(180n/180n)</td>
    <td>1.275V</td>
    <td>1.715V</td>
</tr>
<tr>
    <td>100µ</td>
    <td>100.715µ</td>
    <td>(500n/500n)</td>
    <td>(500n/500n)</td>
    <td>1.4375V</td>
    <td>1.717V</td>
</tr>
<tr>
    <td>100µ</td>
    <td>100.648µ</td>
    <td>(1µ/1µ)</td>
    <td>(1µ/1µ)</td>
    <td>1.3972V</td>
    <td>1.71747V</td>
</tr>
<tr>
    <td>200µ</td>
    <td>197.637µ</td>
    <td>(1µ/1µ)</td>
    <td>(1µ/2µ)</td>
    <td>1.397V</td>
    <td>1.637V</td>
</tr>
    <tr>
      <td>50µ</td>
    <td>52.13µ</td>
    <td>(1µ/1µ)</td>
    <td>(1µ/0.5µ)</td>
    <td>1.3972V</td>
    <td>1.75725V</td>
    </tr>
    <tr>
      <td>100µ</td>
    <td>101.539µ</td>
    <td>(1µ/2µ)</td>
    <td>(1µ/2µ)</td>
    <td>1.08762V</td>
    <td>1.71674V</td>
    </tr>
     <tr>
      <td>100µ</td>
    <td>102.131µ</td>
    <td>(1µ/3µ)</td>
    <td>(1µ/3µ)</td>
    <td>0.95619V</td>
    <td>1.71625V</td>
    </tr>
</table> 
<br>

**Part - A**

## Case-1
**180nm**<br>
*1:1 aspect ratio**<br>
## DC analysis

<p> Vdd=1.8v</p><br>
<p> P <= 1mw</p><br>
<p> I = P/V = 1/1.8 = 0.55mA</p><br>
<p>ID1=ID2= 0.277mA</p><br>
<p> For MOSFET 1 the circuit is diode connected hence, it is working in saturation region. MOSFET 2 has Vsd = 0.8327V, Vsg = 0.8327V, and Vth = 0.496V. It satisfies the P-MOS saturation condition Vds > Vgs - Vth. For MOSFET 3 it has Vds = 0.8327V, Vgs = 0.5697V, hence satisfies the N-MOS saturation condition.</p><br>


![Image](https://github.com/user-attachments/assets/ab20f49b-39cb-4204-8bd2-152356b42753)

![1000049942](https://github.com/user-attachments/assets/eab24b2a-c22c-4478-9642-2f0a06f7310c)




 <table> 
<tr>
 <th><b>Parameters</b></th>
 <th><b>MOSFET1</b></th>
 <th><b>MOSFET2</b></th>
 <th><b>MOSFET3</b></th>
</tr>
<tr>
    <td>Model</td>
    <td>CMOSP</td>
    <td>CMOSP</td>
    <td>CMOSN</td>
</tr>
<tr>
    <td>Mosfet Length</td>
    <td>180nm</td>
    <td>180nm</td>
    <td>180nm</td>
</tr>
<tr>
    <td>Mosfet Width</td>
    <td>10µm</td>
    <td>10µm</td>
    <td>32.025µm</td>
</tr>

   <tr>
      <td>Current(I)</td>
      <td> I<sub>ref</sub> = 0.227mA </td>
      <td> I<sub>d</sub> = 0.227mA </td>
      <td> I<sub>d</sub> = 0.227mA </td>
    </tr>
    <tr>
      <td>Supply Voltage</td>
      <td> 1.8V</td>
      <td> 1.8V</td>
      <td> --- </td>
    </tr>
     <tr>
      <td>Biased Voltage</td>
      <td> --- </td>
      <td> --- </td>
      <td> 0.500V</td>
    </tr>
</table>
<br>

## Transient Analysis 

![Image](https://github.com/user-attachments/assets/46f5edb0-195b-464b-9643-add5942b5480)
<p> The input voltage given for N-MOS has DC-offset of 0.500V and amplitude of 10mV with frequency of 1kHz.
Can observe the output voltage which is 12.43V.</p>

## AC Analysis 


![Image](https://github.com/user-attachments/assets/50211f45-5747-4146-aa33-0e229c8c92a9)


<p>The obtained gain from the simulation is 29.88dB.
29.88 - 3 = 26.88dB
The frequency for this particular dB is 547.86MHz, the bandwidth can be calculated as fH - fL.
= 564.84M - 0
= 564.84MHz</p><br>

---
**for 1:2 aspect ratio**<br>
**180nm**<br>
<p>As total current is 0.55mA, it is divided into 3 parts, where 1/3 of current is its reference current I<sub>ref</sub> and remaining is the output current I<sub>d</sub>. <br>
i.e 0.55m / 3 = 0.183mA. <br>
Hence, I<sub>ref</sub> = 0.183mA and I<sub>d</sub> = 0.3667mA </p><br>

![1000049945](https://github.com/user-attachments/assets/0e1e6d3c-d91c-441e-a107-f0e35e8f1a21)


 <table> 
<tr>
 <th><b>Parameters</b></th>
 <th><b>MOSFET1</b></th>
 <th><b>MOSFET2</b></th>
 <th><b>MOSFET3</b></th>
</tr>
<tr>
    <td>Model</td>
    <td>CMOSP</td>
    <td>CMOSP</td>
    <td>CMOSN</td>
</tr>
<tr>
    <td>Mosfet Length</td>
    <td>180nm</td>
    <td>180nm</td>
    <td>180nm</td>
</tr>
<tr>
    <td>Mosfet Width</td>
    <td>10µm</td>
    <td>20µm</td>
    <td>48.69µm</td>
</tr>

   
   <tr>
      <td>Current(I)</td>
      <td> I<sub>ref</sub> = 0.1833mA </td>
      <td> I<sub>d</sub> = 0.3666mA </td>
      <td> I<sub>d</sub> = 0.3666mA </td>
    </tr>
    <tr>
      <td>Supply Voltage</td>
      <td> 1.8V</td>
      <td> 1.8V</td>
      <td> --- </td>
    </tr>
     <tr>
      <td>Biased Voltage</td>
      <td> --- </td>
      <td> --- </td>
      <td> 0.500V</td>
    </tr>
</table>

## Transient Analysis

![Image](https://github.com/user-attachments/assets/4363f5ad-b178-408a-a1a8-a1c9ba38e478)

## AC Analysis

![Image](https://github.com/user-attachments/assets/c20df57d-482b-4d57-adc3-4ac812ccfe95)

<p>The obtained gain from the simulation is 29.88dB.
29.88 - 3 = 26.88dB
The frequency for this particular dB is 547.86MHz, the bandwidth can be calculated as fH - fL.
= 564.84M - 0
= 564.84MHz</p><br>
<p> There is no increase or decrease in gain in both 1:1 and 1:2 aspect ratio.</p><br>

**Comparision table for 180nm**

<table>
  <tr>
    <th> Parameters</th>
    <th> 1:1 </th>
    <th> 1:2 </th>
  </tr>
  <tr>
    <td> V<sub>out</sub></td>
    <td> 0.967276V</td>
    <td> 1.03471V</td>
  </tr>
  <tr> 
    <td> V<sub>x</sub></td>
    <td>0.967276v</td>
    <td> 0.998633V</td>
  </tr>
</table>

## Case-2 - 500nm Length
**1:1 aspect ratio**

## DC Analysis 

![1000049955](https://github.com/user-attachments/assets/8e490a39-778c-454d-a6dd-fdded74bcdcc)



 <table> 
<tr>
 <th><b>Parameters</b></th>
 <th><b>MOSFET1</b></th>
 <th><b>MOSFET2</b></th>
 <th><b>MOSFET3</b></th>
</tr>
<tr>
    <td>Model</td>
    <td>CMOSP</td>
    <td>CMOSP</td>
    <td>CMOSN</td>
</tr>
<tr>
    <td>Mosfet Length</td>
    <td>500nm</td>
    <td>500nm</td>
    <td>500nm</td>
</tr>
<tr>
    <td>Mosfet Width</td>
    <td>10µm</td>
    <td>10µm</td>
    <td>33.179µm</td>
</tr>

   <tr>
      <td>Current(I)</td>
      <td> I<sub>ref</sub> = 0.227mA </td>
      <td> I<sub>d</sub> = 0.227mA </td>
      <td> I<sub>d</sub> = 0.227mA </td>
    </tr>
    <tr>
      <td>Supply Voltage</td>
      <td> 1.8V</td>
      <td> 1.8V</td>
      <td> --- </td>
    </tr>
     <tr>
      <td>Biased Voltage</td>
      <td> --- </td>
      <td> --- </td>
      <td> 0.500V</td>
    </tr>
</table>
<br>

## Transient Analysis

![Image](https://github.com/user-attachments/assets/f8e06c9e-f9dc-4c85-bfe5-07c0e13b16ae)

## AC Analysis

![Image](https://github.com/user-attachments/assets/76382502-a1fe-4a94-a814-b4914aa96c4b)

The obtained gain from the simulation is 39.85dB.
39.85 - 3 = 36.85B
The frequency for this particular dB is 140.45MHz, the bandwidth can be calculated as fH - fL.
= 140.45M - 0
= 140.45MHz

**1:2 aspect ratio**

## DC Analysis

![1000049956](https://github.com/user-attachments/assets/a3d17bdf-a260-42a9-9c7b-d1ca6671ce62)

<p> here the width is 60.456um.</p>
## Transient Analysis

![Image](https://github.com/user-attachments/assets/0c21dfcf-06e8-4afb-823e-bf5fd1f33f3d)

## AC Analysis

![Image](https://github.com/user-attachments/assets/ac1b6071-004c-4d91-a5e4-3f060feaade7)

<p>The obtained gain from the simulation is 41.952Db.
41.952 - 3 = 38.952dB
The frequency for this particular dB is 547.86MHz, the bandwidth can be calculated as fH - fL.
= 159.896kHz - 0
= 159.896kHz</p><br>
<p> There is no increase or decrease in gain in both 1:1 and 1:2 aspect ratio.</p><br>

**comparision table**

<table>
  <tr>
    <th> Parameters</th>
    <th> 1:1 </th>
    <th> 1:2 </th>
  </tr>
  <tr>
    <td> V<sub>out</sub></td>
    <td>0.644704V</td>
    <td>0.79317V</td>
  </tr>
  <tr> 
    <td> V<sub>x</sub></td>
    <td>0.644704V</td>
    <td>0.778596V</td>
  </tr>
</table>

# case-3 1µm 
**1:1 aspect ratio**

 <table> 
<tr>
 <th><b>Parameters</b></th>
 <th><b>MOSFET1</b></th>
 <th><b>MOSFET2</b></th>
 <th><b>MOSFET3</b></th>
</tr>
<tr>
    <td>Model</td>
    <td>CMOSP</td>
    <td>CMOSP</td>
    <td>CMOSN</td>
</tr>
<tr>
    <td>Mosfet Length</td>
    <td>1µm</td>
    <td>1µm</td>
    <td>1µm</td>
</tr>
<tr>
    <td>Mosfet Width</td>
    <td>10µm</td>
    <td>10µm</td>
    <td>91.541125µm</td>
</tr>

   <tr>
      <td>Current(I)</td>
      <td> I<sub>ref</sub> = 0.277mA </td>
      <td> I<sub>d</sub> = 0.277mA </td>
      <td> I<sub>d</sub> = 0.277mA </td>
    </tr>
    <tr>
      <td>Supply Voltage</td>
      <td> 1.8V</td>
      <td> 1.8V</td>
      <td> --- </td>
    </tr>
     <tr>
      <td>Biased Voltage</td>
      <td> --- </td>
      <td> --- </td>
      <td> 0.500V</td>
    </tr>
</table>
<br>

## DC Analysis

![1000049957](https://github.com/user-attachments/assets/23da6fd5-39cd-4af9-a909-38b34cd60938)

<p> From dc analysis:
Vout = 0.293177v, which is equal to Vx
Iref = Id = 277µA</p><br>

## Taansient Analysis

![Image](https://github.com/user-attachments/assets/9781a5e0-848e-4b71-acc7-7d73aac8b5fb)

## AC Analysis

![Image](https://github.com/user-attachments/assets/210cdbeb-abbc-4198-ab3a-9a804e1284b9)

<p>The obtained gain from the simulation is 39.946Db.
39.964- 3 = 36.964dB
The frequency for this particular dB is 31.798kHz, the bandwidth can be calculated as fH - fL.
=31.798kHz - 0
= 31.798kHz</p><br>

**1:2 aspect ratio**

## DC Analysis 

![Image](https://github.com/user-attachments/assets/8f116501-d8e9-4b6c-a239-879b42858317)
 <table> 
<tr>
 <th><b>Parameters</b></th>
 <th><b>MOSFET1</b></th>
 <th><b>MOSFET2</b></th>
 <th><b>MOSFET3</b></th>
</tr>
<tr>
    <td>Model</td>
    <td>CMOSP</td>
    <td>CMOSP</td>
    <td>CMOSN</td>
</tr>
<tr>
    <td>Mosfet Length</td>
    <td>1um</td>
    <td>1um</td>
    <td>1um</td>
</tr>
<tr>
    <td>Mosfet Width</td>
    <td>10µm</td>
    <td>20µm</td>
    <td>100.88µm</td>
</tr>

   
   <tr>
      <td>Current(I)</td>
      <td> I<sub>ref</sub> = 0.183mA </td>
      <td> I<sub>d</sub> = 0.3667mA </td>
      <td> I<sub>d</sub> = 0.3667mA </td>
    </tr>
    <tr>
      <td>Supply Voltage</td>
      <td> 1.8V</td>
      <td> 1.8V</td>
      <td> --- </td>
    </tr>
     <tr>
      <td>Biased Voltage</td>
      <td> --- </td>
      <td> --- </td>
      <td> 0.500V</td>
    </tr>
</table>

## Transient analysis
![Image](https://github.com/user-attachments/assets/d7603a63-d484-4f7e-a5bd-878df21120c5)

## AC Analysis
![Image](https://github.com/user-attachments/assets/a03a8752-f5c3-452f-a43f-294aad084bfa)

<p>The obtained gain from the simulation is 40.313Db.
40.313- 3 =37.313 dB
The frequency for this particular dB is 10.656MHz, the bandwidth can be calculated as fH - fL.
=10.656MHz - 0
= 10.656MHz</p><br>
<table>
  <tr>
    <th> Parameters</th>
    <th> 1:1 </th>
    <th> 1:2 </th>
  </tr>
  <tr>
    <td> V<sub>out</sub></td>
    <td> 0.29317V</td>
    <td> 0.472227V</td>
  </tr>
  <tr> 
    <td> V<sub>x</sub></td>
    <td>0.293177v</td>
    <td> 0.51519V</td>
  </tr>
</table>

## PART - B 

<p> Design the differential amplifier using the same design specification as experiment 3(differential amplifier). Perform DC, Transient, AC analysis for this.
</p><br>
<p> Here M1 and M2 are in 1:1 ratio and M5 and M6 are in 1:2 ratio .</p><br>
<p> For this circuit biased voltage is replaced by current mirror circuit, with Vdd = 3.3vV</p><br>

![Image](https://github.com/user-attachments/assets/29e5b266-47d9-4eeb-96cd-35964d9fb533)


## DC Analysis

![Image](https://github.com/user-attachments/assets/ebf0500c-c22a-4400-aa82-f74022dd2965)
<p> here the width is = 1.69991u</p><br>

## Transient Analysis

![Image](https://github.com/user-attachments/assets/3765d6f4-b1a1-40c4-8f40-7b399a65508d)
<p> Output voltage is 2.70v</p><br>

## AC Analysis

![Image](https://github.com/user-attachments/assets/ba221a2d-1d48-407a-bee6-5328fd916c62)

<p> gain is 21.760dB.</p><br>
