# **Expermient-1-**  
## **DC,Transient and AC Analysis of Common Source Amplifier Using LTspice**  
## **AIM**:  
To Analyse the DC,Transient and AC Analysis of Common Source Amplifier Using LTspice.  
## **COMPONENTS**:  
Resistor, n-mosfet,Voltage source(Power Supply),AC ground,Wires.  
## **CIRCUIT DIAGRAM**:  
![Image](https://github.com/user-attachments/assets/b532a953-89db-425d-b885-72963173c5eb)  
## **PROCEDURE**:  
1.Design the common source amplfier circuit as per the circuit diagram using LTspice.  
2.Right click on power supply and set gate vtg 0.9V,VDD as 1.8V and Resistor value as 1k.  
3.Download the library file.  
4.Import the library file to LTspice using spice directive called(.op).
5.Find the cuurent value for the given power rating P=100µW.  
6.Now by doing trial and error method we can find L and W value. Where is L=1u and W=6.85u.  
## **DC Analysis**:  
1.In edit simulation option or command,we have to select the dc output print(DC op pnt) and Run the Simulation.    

![Dc analysis task 1](https://github.com/user-attachments/assets/c520c0aa-e6c6-475f-b606-191508b36fa8)  
## **Transient Analyis**:  
1.In edit simulation option,change from dc offset to transient.Set the DC offset as 0.9V,Amplitude 50mV,Frequency 1KHz.  
Set stop time for 1ms and Run the Simulation.  

![op trans](https://github.com/user-attachments/assets/f2e7e996-c8a4-4140-b884-0325cdff738f)  
## **AC Analysis**:  
1.In edit simulation option or command,change from transient to Ac anlysis.Set type of sweep as Decade,number of points per decade as 20,start and stop frequency as 0.1Hz and 1THz and Run the Simulation.  

![ac analysis](https://github.com/user-attachments/assets/81496881-1f19-446b-a245-d8659533b46f)
















