starting off with a 22V source, and a resistor.
ran .op got V(n001) w 22
and I(V1): -2.2

-just click on the wire in order to probe it.

step 2:
- replace resistor with another 5.37 resistor as well as a 20 mH inductor to simulate the electromagnet
- we're using 20 mH because we don't have a measured value. it's a decent approximate and the actual value isn't super important at this current stage.
- ran .tran 10m startup and got a nice curve/

step 3: 
- remove the wire connecting to negative
- press P to search for an nmos

- place the end of the inductor to the source on the mosfet
- the drain will go to ground

- we make a new pulsing voltage source that we connect to the gate with values of :
Vinitial = 0
Von = 10
Tdelay = 1m
Trise = 1u
Tfall = 1u
Ton = 5m
Period = 10m

-then run the simulation probing:
current through inductor
Gate voltage
Drain voltage

for some reason everything stopped working so I restarted
- started using grounds instead and switched to a non ideal mosfet

step 4: 
- now we create a flyback diode to solve the large voltage spike
- the line (cathode positive) connects to the voltage source and the anode (negative) connects to the drain.

step 5: 
-we add a gate resistor
-LTspice has ideal wires so it won't make much difference but in practice I limits instantaneous current required to charge the mosfet gate capacitance which damps ringing
-Much less oscillation of the current going through the mosfet gate.

step 6:
gate driver. 
- need to import but can't figure out how to do that yet so will continue using ideal voltage.
- d
