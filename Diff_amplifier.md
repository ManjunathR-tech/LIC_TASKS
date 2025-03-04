## *Experiment - 03* {Analysis of MOS Differential pair Amplifier}  
**Differential Amplifier** is a circuit that amplify the difference between two input signals while rejecting common-mode signals (noise present in both inputs). They are commonly used in operational amplifiers,   comparators, and signal processing applications.  

***There are four types differential amplifier:***   
 Resistively Loaded Differential Amplifier:- The resistively loaded MOSFET differential amplifier is the simplest type of differential amplifier. It consists of two MOSFETs (M1 & M2) operating in saturation mode, Rss resistor, and also two resistors as load resistances at the drain terminals.  
 
 Differential Pair with Current Source:- Replacing the source resistor (𝑅ss) with a current source improves the gain, stability, and common-mode rejection ratio (CMRR) of the amplifier.  

 Differential Pair with Single MOSFET Current Source:- A single MOSFET acts as a current source instead of using a current source.This simplifies the design while still improving gain.  

Active Load Differential Pair (MOSFET as Load):- Both Iss and Rd are replaced with a mosfet.Gain is very high.  

### *Aim*
  Perform  DC, Transient and AC analysis of differential amplifier with the following specifications using LT Spice simulation software.     

- *Vdd* = 3.2V
- *Vincm* = 1.6V 
- *Power budget* <= 2.8mW 
- *Vocm* = 1.7V 
- *Vp* = 0.6V

With above specifications also extract the following parameters:
- DC operating point
- Input and output maximum swing
- Gain

  ![WhatsApp Image 2025-03-05 at 00 07 17_b075c03f](https://github.com/user-attachments/assets/24521ea2-13f6-4d45-a674-a3725ff690dd)

  ### Circuit 1: Differential Amplifier with a Resistive Load
  ![IMG_20250303_074814.jpg](https://github.com/user-attachments/assets/cfc32586-fcce-4aa7-b1e8-74ae135d6dd4)

Above circuit depecits the two NMOSFET having same Vdd connected to a single resistor Rss(Ron3) this constitutes differential amplifier with resistive load.  

### Procedure:
 
- Circuit

![ckt](https://github.com/user-attachments/assets/6d7fa9c5-12ba-43ba-a8b6-218cfa17a1da)


* Perform DC analysis to obtain operating point(.op) by adjusting width and length of both MOSFETS and Set the Rd and Rss values such that the transistors will operate in saturation region.
* Vary W/L to get the required Voutcm.  
* Vary Rd to set exact Voutcm.  
* Go to "Simulate" > "Edit Simulation Cmd" > "DC op pnt".
  
  ![Screenshot 2025-03-04 203942](https://github.com/user-attachments/assets/32f4794a-a87d-4656-864b-6d1f14ee01de)

- Operating point (1.7V , 0.43mA) is obtained at length=180nm and width=2.536uum for both the MOSFETs.

- ![Screenshot 2025-03-04 210733](https://github.com/user-attachments/assets/a67474b3-9ab0-4f96-a407-d85b36247270)












 

 
 
 

