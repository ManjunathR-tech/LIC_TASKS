![task 2 ckt](https://github.com/user-attachments/assets/a80607ac-c4d2-40a1-8520-cbb915165141)# **Expermient-1-**  
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

# **Calculations**:  
Given the power as 100uW ,we know that Vdd is 1.8V  
from the formula P=VI  
Id=P/V = 100u/1.8 = 55.5uA  
Now,  
from the loop equation : Vdd=IdRd + Vout  
(where Id=55.5uA,Rd=1kohm,Vdd=1.8V)  
Therefore,  
Vout=1.745V  
Hence the Q point = (Vout,Id) = (1.745V,55.5uA)  

## TABULAR COLUMN:  
For DC Analysis,to get thr calculated value of Id,you need to vary the width check for the corresponding Vout.  
|  Width   |  Current |   Vout   |
|----------|----------|----------|
|    1um   |  152.7uA |   1.64V  |
|   0.8um  |  78.37uA |   1.67V  |
|   0.4um  |  78.37uA |   1.72V  |
|   0.2um  |  55.2uA  |   1.74V  |
|  0.203um |  55.5uA  |   1.74V  |  
## Result:  
Dc Analysis:  

![Dc analysis task 1](https://github.com/user-attachments/assets/c520c0aa-e6c6-475f-b606-191508b36fa8)  

As seen above,We got Id=55.5uA for width 0.203um and Vout=1.745V.  
Therefore the Dc operating point is(1.745V,55.5uA).  

Transient Analysis:  

![op trans](https://github.com/user-attachments/assets/f2e7e996-c8a4-4140-b884-0325cdff738f)  

We got Vout=1.745V for width=0.203um and phase shift of 180 degree.

Ac Analysis:

![ac analysis](https://github.com/user-attachments/assets/81496881-1f19-446b-a245-d8659533b46f)  

We got Frequency=210,4GHz.  
Gain(db)=-9.104db  


## INFERENCE:  
1.Width is directly proportional to drain current.  
2.There is 180 degree phase shift between input and output in Transient Analysis. 


#  **CIRCUIT DIAGRAM 2:**  

![task 2 ckt](https://github.com/user-attachments/assets/b0aca44b-578e-4a65-aef9-20dcb6aa0721)  

##  **COMPONENTS:**  
PMOSFET(180nm technology),NMOSFET(180nm technology),Voltage supply,AC ground.  

## **PROCEDURE:**  
1.Build the above Circuit using LTspice software.  
2.Download and save the library file and LT splice file to a folder.  
3.Import the library file to LTspice file using spice directive (.op).  
4.Design a diode connected PMOSFET such that it always operates in saturation region.  
5.Set the gate voltage of NMOSFET to 0.7V and maintain the supply voltage as 1.8V only.  
6.Set the length and width of both the transistor as 180nm and 1um.  
7.The given power rating is 100 micro watt. So find the current for this power rating.  
8.Firstly conduct the DC Analysis of the circuit. For this vary the width of CMOSN to get the calculated value as the result of the simulation as drain current is directly proportional to width of the transistor.  
9.For Transient Analysis set the dc offset as 0.9V, amplitude 50mV, and frequency as 1kHz and keep the stop time for 3ms and run.  
10.For AC Analysis set the sweep as decade , number of points per decade as 20, start frequency as 0.1Hz and stop frequency as 1T(Tera)Hz.  

## **TABULAR COLOUMN:**  
For the DC Analysis, to get the calculated value of Id , you need to vary the width and check for the corresponding Vout.  
|  Width   |  Current |   Vout   |
|----------|----------|----------|
|    1um   |   27uA   |   1V     |
|   1.2um  |  32.6uA  |   1V     |
|   1.4um  |  38.1uA  |   1V     |
|   1.6um  |  43.5uA  |   1V     |
|    2um   |  54.5uA  |   1V     |  
## Result:  
1.DC Analysis:  
Given the power as 100uW ,we know that Vdd is 1.8V  
from the formula P=VI  
Id=P/V = 100u/1.8 = 55.5uA  
We got Id=55.5uA for width=2.02um and Vout=1.1V.  
Vds=Vout=1.1V  
Vov = Vgs-Vth = Vin-Vth = 0.7-0.36= 0.36V  
where Vds>Vov. Mosfet lies in saturation region.  
Therefore the dc operting point is(1.1V,55.5uA)  

2. Transient Analysis:
 ![tans](https://github.com/user-attachments/assets/6d023064-09e0-49b6-bae2-3593bb77d1f4)
 













      



















