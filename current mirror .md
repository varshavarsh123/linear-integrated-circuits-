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
