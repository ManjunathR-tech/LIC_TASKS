# EXPERIMENT - 06 {CURRENT MIRROR CIRCUIT}  
## Current Mirror 
A current mirror circuit is a fundamental building block in analog electronics used to replicate a reference current with high accuracy.It amplifies the difference between two input signals while rejecting common-mode noise, making it ideal for high-precision circuits, including operational amplifiers.  

## Classification based on type of moseft used in current mirror circits  
NMOS Currnet Mirroring  
   - Used: N-channel MOSFETs  
   - One NMOS transistor is diode-connected  to set the reference current.  
   - Ensures stable and precise current mirroring.  

![images](https://github.com/user-attachments/assets/af301326-3b42-4a14-84d0-20c50c3e3bb4)  

PMOS current Mirroring
   - Used: P-channel MOSFETs
   - The reference current is set using a diode-connected PMOS transistor, with another PMOS mirroring it.

![image](https://github.com/user-attachments/assets/1a870006-1e99-448a-b5e7-c4ddd99f8417)

### OBJECTIVE
  To design and analyze a current mirror circuit as an active load in a common-source amplifier.  

  ![image](https://github.com/user-attachments/assets/d78da15e-9d51-4c8b-b3c1-73b958d48fff)  

  
  - **Gain(Av)** > -10V/V
  - **Power supply(Vdd)** = 1.8V
  - **Power(P)** <= 1mW
  - **It=P/Vdd.**
  - **It=Iref+Ix.**

## DC Analysis:[for mirror ratio 1:1]  

We know that already Itotal=Iref+Ix  
For 1:1 ratio Iref=Ix  
So,Iref=Itotal/2  
Itotal=P/Vdd  
Itotal=1mW/1.8V  
Itotal=0.555mA.  
Therefore,Iref=Ix= 0.2778mA  

![Screenshot 2025-03-23 221756](https://github.com/user-attachments/assets/21d81de3-4186-430e-95d5-fb614443a823)  

### Analyzing the current mirroring circuit by changing the w and L but with the same ratio.  

**L=500nm.**

We know (w/L) ratio which is 16.667.

Therefore for L=500nm the w=8.334um.

|  Mosfet   |      Id       |  
|-----------|---------------|
|  M1       |   0.000281241 |             
|  M2       |   0.000281241 |             
|  M3       |   0.0002778   |       

## Transient Analysis:  

![Screenshot 2025-03-23 221946](https://github.com/user-attachments/assets/be56f207-c1fc-464a-acc8-6445a1199073)  
The obtained gain from the transient analysis is -10.2V/V.  

## AC Analysis:

![Screenshot 2025-03-23 222148](https://github.com/user-attachments/assets/696c6eed-7d79-48c3-8b3b-5e54bd74f039)  
The Expected gain in db of the circuit is 20db.But the obtained gain from the AC analysis(frequency response) is 22.16db.  

**3db Bandwidth:**  
The obatined 3db B.W=2.267GHz.  


![Screenshot 2025-03-22 155941](https://github.com/user-attachments/assets/f162d225-40dd-4f49-b466-eae9243c31a6)  


## DC Analysis:[for mirror ratio 1:2]  

We know that already Itotal=Iref+Ix    
For 1:2 ratio 2*Iref=Ix  
So,Iref=Itotal/3  
Itotal=P/Vdd  
Itotal=1mW/1.8V  
Itotal=0.555mA    
Therefore,Iref=0.185mA  

![Screenshot 2025-03-23 222519](https://github.com/user-attachments/assets/4c45186d-81c5-4add-8565-c94b756087ce)  

## Transient Analysis:  

![Screenshot 2025-03-23 222816](https://github.com/user-attachments/assets/e4a79bdb-80de-40c9-9d7c-265384f2e129)  
The Expected gain of the circuit is -10V/V.But the obtained gain from the transient analysis is -11.68V/V.  

## AC Analysis:  

![Screenshot 2025-03-23 222944](https://github.com/user-attachments/assets/10d5cd69-e8bf-4f04-8c55-aabb55e1ec70)  
The obtained gain from the AC analysis(frequency response) is 24.6db.  


**3db Bandwidth:**

The obatined 3db B.W=1.175GHz.  

### **Comparison Table:**
| **Parameter** | **Mirror Ratio 1:1** (Theory) | **Mirror Ratio 1:1** (Practical) | **Mirror Ratio 1:2** (Theory) | **Mirror Ratio 1:2** (Practical) |
|---------------|-------------------------------|----------------------------------|-------------------------------|----------------------------------|
| Av (in dB)    |         20 dB                 |       22.16 dB                   |          21.34 dB             |           24.6 dB                |
| Av (in V/V)   |          -10                  |        -10.2                     |           -10                 |           -11.68                 |
| 3 dB Bandwidth|           -                   |       2.267 GHz                  |             -                 |           1.175 GHz              |  


### Inference:  

The PMOS current mirror circuit accurately replicates the reference current with minimal deviation, ensuring reliable current mirroring across different W/L 
ratios.  
As the mirror ratio increases, the drain current (Id) scales proportionally, confirming the circuit's effectiveness in current duplication.  
Increasing the mirror ratio for 1:1 to 1:2 results in higher gain but also reduces bandwidth, affecting the circuit's frequency response.  
AC analysis shows the circuit has a high gain and wide frequency range, making it good for high-speed applications.  
The simulation results closely match theoretical expectations, validating the circuit's performance and its suitability for analog applications.  



# PART-B  

### Design the differential amplifier with 2 Differencial pair with current source.  

## CIRCUIT DIAGRAM:

![Screenshot 2025-03-25 001233](https://github.com/user-attachments/assets/94fa6fc3-1b2d-4b55-8f7f-fd8cc10ad206)  

## DC ANALYSIS:  

The circuit consists of six MOSFETs (M1 to M6),each with different width-to-length (W/L) ratios.To ensure accurate analysis,all transistors must operate in the   saturation region.  
DC analysis focuses on identifying the voltage and current levels at various nodes in the circuit. Based on the previous experiment, the following conditions must be met Current Matching & Voltage Stability.  

![Screenshot 2025-03-25 000619](https://github.com/user-attachments/assets/1ffb6b82-b0fe-4bd4-a872-2d7a999899ac)  

## Transient Analysis:  

![Screenshot 2025-03-25 232303](https://github.com/user-attachments/assets/ec35d4f0-e80c-4240-bb2b-5d0c47f9160f)  

## AC Analysis: 

![image](https://github.com/user-attachments/assets/9db4f418-0185-4105-a534-2aed9265adc3)




















    






  


