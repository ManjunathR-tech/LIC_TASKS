## *Experiment - 03* {Analysis of MOS Differential pair Amplifier}  
**Differential Amplifier** is a circuit that amplify the difference between two input signals while rejecting common-mode signals (noise present in both inputs). They are commonly used in operational amplifiers,   comparators, and signal processing applications.  

***There are four types differential amplifier:***   
 Resistively Loaded Differential Amplifier:- The resistively loaded MOSFET differential amplifier is the simplest type of differential amplifier. It consists of two MOSFETs (M1 & M2) operating in saturation mode, Rss resistor, and also two resistors as load resistances at the drain terminals.  
 
 Differential Pair with Current Source:- Replacing the source resistor (𝑅ss) with a current source improves the gain, stability, and common-mode rejection ratio (CMRR) of the amplifier.  

 Differential Pair with Single MOSFET as Current Source:- A single MOSFET acts as a current source instead of using a current source.This simplifies the design while still improving gain.  

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

- Operating point (1.10V , 0.438mA) is obtained at length=180nm and width=2.536uum for both the MOSFETs.
  caluculate vincm(min), Vincm(max), Vout(min), Vout(max).  
Vincm(min)= Vth + Vp =0.36 + 0.6 = 0.96  
Vincm(max) = Vdd - (Id*Rd) + Vth = 2.2V  
Vout(min) = Vov1 + Vov3 = 1.04V
Vout(max) = Vdd-(Id*Rd) = 1.738V  

Perform Transient Analysis :    
Replace DC input with an AC signal.  
Use SINE(dc_offset, Amplitude, Frequency).  
Go to "Simulate" > "Edit Simulation Cmd" > "Transient".  
Set Stop Time: 5ms.  
Run the simulation.  

 ![Screenshot 2025-03-04 210733](https://github.com/user-attachments/assets/a67474b3-9ab0-4f96-a407-d85b36247270)

  Maximum Input swing can be obtain using equation  
    Vds>=Vov+x  
    Vds=Vgs-Vth+x  
    Vd-Vs=Vg-Vs-Vth+x  
    Vo-Vp=Vin-Vp-Vth+x  
    1.7-0.6=1.6-0.6-0.489+x  
    1.1=0.511+x  
    x=0.589V

### AC Analysis :  

 ![Screenshot 2025-03-04 212951](https://github.com/user-attachments/assets/d277b655-0195-4459-b00a-c86808a76b91)
    
 - Gain obtained is 10.5dB  

## CIRCUIT 2 : Current Source-Loaded Differential Pair:  


![Screenshot 2025-03-05 014414](https://github.com/user-attachments/assets/0ffb09e3-ae0d-47cc-a789-e7da553c70b6)  

### DC analysis :  

![current dc](https://github.com/user-attachments/assets/93b7f3c9-d289-4b60-b051-e39028d19a5d)  

### Transient Analysis :  

![current trans](https://github.com/user-attachments/assets/94cbff78-75eb-4e24-a69c-69d2878484f2)  

### AC Analysis :  

![current ac](https://github.com/user-attachments/assets/fc497957-f5fe-418e-8a45-fef233d9f220)  


## CIRCUIT 3 : Differential Pair with Single MOSFET as Current Source  

### DC analysis :  

![mosfet current dc](https://github.com/user-attachments/assets/cc531f54-5f44-44c3-abe7-4c5e761e8d24)

### Transient Analysis :  

![Screenshot 2025-03-05 021743](https://github.com/user-attachments/assets/ad8ad54c-187d-4666-82dd-73c0cd1bc344)  

### AC Analysis :  

![image](https://github.com/user-attachments/assets/9ff5dbff-2ba0-45de-851f-f32ac91d568f)


















   












 

 
 
 

