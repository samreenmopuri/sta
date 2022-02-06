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

DAY 3
Timing Arcs 
      cell arcs
      net arcs
Combinational Arcs
Sequential Arcs
Timing Sense 
    Positive Unate:output signaldirection will be same as input direction
    negative unate:output signal direction will be opposite to input direction
    Non Unate:It is not possible to predict whether output follows input direction
Cell Delay is  a function of input transition ,output load/capacitance
SETUP CHECK:
STA finds the most restrictive setup by expanding the clock into a common base period and finding the most restrictive launch and capture.
If the peroid of one clock cycle is Tperiod, setup time Tsetup, delay due to combinational logic Tcomb, clock skew Tskew, setup uncertainty Su due to jitter in clock
The equation for setup check : Tcomb + Tsetup <= Tperiod + Tskew - Su
<img width="534" alt="Screen Shot 2022-02-05 at 12 44 57" src="https://user-images.githubusercontent.com/99019822/152693103-afdaa4bf-e991-4c4f-aae8-b7a173855925.png">
<img width="936" alt="Screen Shot 2022-02-05 at 16 33 03" src="https://user-images.githubusercontent.com/99019822/152693161-56007de1-0d73-4c13-8933-2c0e431b2dfb.png">
<img width="1440" alt="Screen Shot 2022-02-05 at 16 34 52" src="https://user-images.githubusercontent.com/99019822/152693191-63f4bf3c-5f8f-4976-8d54-e4ddb54b0178.png">

DAY4
CLOCK GATING CHECKS
<img width="829" alt="Screen Shot 2022-02-05 at 23 11 38" src="https://user-images.githubusercontent.com/99019822/152693755-07ef12ad-cd7a-4456-9a5a-cb595e05b825.png">
COMPLEX CELL:Timing tool cant figure out to check
Checks on Asynchronous Pin:Asserion is an asynchronous event & no relation with clock
                           Deassertion causes flop to become depenent on clock
                           
  <img width="1440" alt="Screen Shot 2022-02-05 at 23 03 43" src="https://user-images.githubusercontent.com/99019822/152693972-ff365941-148d-4380-b54f-2497cecf96d4.png">
  <img width="1440" alt="Screen Shot 2022-02-05 at 23 08 14" src="https://user-images.githubusercontent.com/99019822/152694068-b85b0980-6071-46d5-aa92-605e1d98a5f9.png">
  <img width="1440" alt="Screen Shot 2022-02-05 at 23 09 52" src="https://user-images.githubusercontent.com/99019822/152694141-0e2c8c99-203b-45bd-8fdb-f07f9e44c16a.png">











