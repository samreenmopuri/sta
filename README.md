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



