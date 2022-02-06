# sta
sta
Day 1 

STA method of computing the expected timing of digtal circuit  without requiring an exhaustive dynamic simulation of full circuit Static timing analysis (STA) is a method of validating the timing performance of a design by checking all possible paths for timing violations. STA breaks a design down into timing paths, calculates the signal propagation delay along each path, and checks for violations of timing constraints inside the design and at the input/output interface. This process does not verify logic of a design and works only for synchronous clock types.
INPUTS TO THE STA:
    gate level netlist
    SDC or constraint file
STA breaks down the design at ports,sequential elements
Timing paths are either from port to sequential
Timing Path Elements
               Start Point ,End Point,Combinational Logic
Setup Pin:data should be available at sequential device before clock edge that captures the data .This Enforces Max delay on the path
HoldPin:Data should be stable at the input of sequential device for some time after clock Edge that capture the data .this enforces Min delay on the path
Day 1 lab
opening Simple.v file
<img width="1440" alt="Screen Shot 2022-02-04 at 17 06 29" src="https://user-images.githubusercontent.com/99019822/152687496-a874474c-362b-44a5-b2af-3ef0a39cc0bd.png">
<img width="1436" alt="Screen Shot 2022-02-04 at 13 04 47" src="https://user-images.githubusercontent.com/99019822/152687534-938fff15-111d-4f62-b742-fd3f674fd6bf.png">
running and Opening of Liberty File
<img width="1414" alt="Screen Shot 2022-02-04 at 13 02 29" src="https://user-images.githubusercontent.com/99019822/152687620-67fb69b6-032a-4425-a810-ffdc18df24c7.png">
Day 2
Design Rule Check
Slew or Transition Analysis
   Time taken for signal to raise from 30% Vdd to 70%vdd {rise from 0 to 1}
   Time taken for signal to fall from 70%vdd to 30% Vdd {fall from 1 to 0}
Load Analysis:STA checks Load analysis {min and Max Capacitance on Ports and Nets}
              Fanout Load on Ports and Output Pins
Clock skew Analysiis
Pulse width analysis
Latch based design is preferred compared to flop design as latch is transparent
opening Simple_Early.lib File
<img width="1440" alt="Screen Shot 2022-02-04 at 19 07 10" src="https://user-images.githubusercontent.com/99019822/152688283-b0f923c2-3d1b-4fe8-ad4f-5b7488f8bdb4.png">
opening Simple_Late.lib File
<img width="1440" alt="Screen Shot 2022-02-04 at 19 09 07" src="https://user-images.githubusercontent.com/99019822/152688344-0d4f4c21-245b-478d-bf3f-15852ac9fce8.png">





