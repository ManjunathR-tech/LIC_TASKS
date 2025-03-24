## EXPERIMENT - 06 {CURRENT MIRROR CIRCUIT}  
# Current Mirror 
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
Itotal=0.555mA.
Therefore,Iref=0.185mA












    






  


