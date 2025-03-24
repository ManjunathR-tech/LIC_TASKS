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
So,Iref=It/2  
Itotal=P/Vdd  
Itotal=1mW/1.8V  
Itotal=0.555mA.  
Therefore,Iref=Ix= 0.2778mA  

![Screenshot 2025-03-23 221756](https://github.com/user-attachments/assets/21d81de3-4186-430e-95d5-fb614443a823)


    






  


