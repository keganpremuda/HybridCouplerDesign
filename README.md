<h1>Broadband 90-degree Hybrid Coupler Design</h1>

 <!--### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)-->

<h2>Description</h2>
This project consists of the design of a broadband 90-degree hybrid coupler using the double-box branch-line topology. The design was created and tested using Keysight Advanced Design System electronic design automation software, and calculations were made using MATLAB. The coupler design meets the specific requirements for an input reflection coefficient of -20dB, an output power split balance of less than 0.5dB, an output phase difference of 90 degrees plus or minus a degree, isolation of less than -25dB, transmission line width greater than 6 mils, the frequency range of 3.4 to 4.2 GHz, and substrate realization using Rogers RO4003 substrate. The coupler was first optimized using ideal transmission lines, reconfigured and reoptimized using microstrip transmission lines and Rogers RO4003 substrate, and then used as a module and reoptimized in a 2 port test circuit to confirm requirements were met. 
<br />


<h2>Languages Used</h2>

- <b>MATLAB</b> 

<h2>Environments Used </h2>

- <b>Keysight ADS</b>
- <b>MATLAB</b>

<h2>Project walk-through:</h2>

<p align="center">
 <br/>
<b>Ideal Transmission Line Schematic and S-Parameter Simulation:</b><br><br/>
<img src="https://i.imgur.com/PbqD9Vi.png" height="80%" width="80%" alt="TLIN Schematic"/></p>
<p align="left">
A double-box branch-line topology was studied using the article https://www.microwaves101.com/encyclopedias/two-section-branchline-coupler, and an optimized impedance structure was implemented on a Keysight ADS schematic using ideal transmission lines.</p>
<br />
<br />
<img src="https://i.imgur.com/mlpT7kB.png" height="80%" width="80%" alt="TLIN S-Parameter Simulation"/></p>
<p align="left">
An S-parameter simulation was run to obtain S-parameter plots to ensure specification requirements have been met.</p>
<br />
<br />
<br />
<p align="center">
<b>Microstrip Transmission Line Schematic and S-Parameter Simulation:</b><br><br/>
<img src="https://i.imgur.com/FJ2rrmI.png" height="80%" width="80%" alt="MLIN Schematic"/></p>
<p align="left">
The ideal transmission line modules were replaced with microstrip line modules. The LineCalc tool was used along with Rogers RO4003 substrate information to obtain the necessary lengths and widths of microstrip lines. 50 Ohm terminals were used and microstrip step modules were added for discontinuities between microstrip sections.</p>
<br />
<br />
<img src="https://i.imgur.com/K9Vepy7.png" height="80%" width="80%" alt="MLIN S-Parameter Simulation"/></p>
<p align="left">
An S-parameter simulation was run to obtain S-parameter plots to ensure specification requirements have been met. To meet the line width requirement, W2 was kept just above 6 mils, L1 and W1 were kept at LineCalc determined values and L2 and W3 were tuned until specifications were met.</p>
<br />
<br />
<p align="center">
<b>Layout and EM Model:</b><br><br/>
<img src="https://i.imgur.com/BDJCZ8Q.png" height="80%" width="80%" alt="Layout"/></p>
<p align="left">
The layout was generated using optimized microstrip line parameters.</p>
</br>
<br/>
<img src="https://i.imgur.com/Bnrko2u.png" height="80%" width="80%" alt="Substrate"/></p>
<br/>
<img src="https://i.imgur.com/he9CyTT.png" height="80%" width="80%" alt="Simulation"/></p>
In the layout interface, the substrate, frequency plan, ports, and simulation setup were implemented in the simulation settings. Parameters were added to the coupler for L1, L2, W1, W2, and W3 for future re-optimization, and an EM model and symbol were created for co-simulation.</p>
<br />
<br />
<br />
<p align="center">
<b>Coupler Cosimulation Circuit:</b> <br><br/>
<img src="https://i.imgur.com/wGJiIlY.png" height="80%" width="80%" alt="Final Circuit"/></p>
<p align="left">
A circuit was built using the optimized microstrip coupler for co-simulation. Goals were set up for running the optimization module to meet coupler specifications.</p>
<br/>
<br/>
<img src="https://i.imgur.com/SO58oO4.png" height="80%" width="80%" alt="Optimization"/></p>
<p align="left">
The optimization module and S-parameter simulation were run to obtain optimized L1, L2, W1, W2, and W3 for the coupler.</p>
<br/>
<br/>
<img src="https://i.imgur.com/j4jM1MT.png" height="80%" width="80%" alt="Final Results"/></p>
<p align="left">The final S-parameter results were obtained and confirmed to meet the required specifications.</p>
<br/>
<br/>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
# HybridCouplerDesign
