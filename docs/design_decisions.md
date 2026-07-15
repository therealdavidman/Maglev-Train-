## DD-000

### Decsion
-
### Reason
-
### Tradeoffs

#### Pros:
-

#### Cons:
-


## DD-001

### Decision
selected:
**Active Repulsive Electromagnetic Suspension (AREMS)** over **Active Attractive Electromagnetic Suspension(EMS)**

### Reason
The primary design objective is to create a train that visibly levitatesabove a flat guideway whilst all active levitation components reamin on the vehicle. 
Compared to EMS, AREMS provides a cleaner visual apppearance and more closely matches the original project vision of a train that appears to "float" above the track.


### Tradeoffs

#### Pros:
- Flat, visually clean guidway.
- More impressive visual demonstration.
- Levitation components remain entirely onboard.
- Capable of levitation from rest.
- Unique architecture with interestin control-system challenges.

#### Cons:
- requires permanant magnets (or equivelant magnetic structure) on the track.
- Hall effect sensors are likey unsuitable due to the complex magnetic enviroment.
- Requires seperate lateral guidance (mechanical rails or magnetic guidance).
- more complex magnetic interactions than EMS.
- More difficult to scale to a full-size transportation system.

## DD-002

### Decsion
selected:
Optical gap sensors over hall effect sensors for levitation feedback.

### Reason
Due to choosing AREMS over EMS, The levitation system contains multiple strong magnetic fields from the onboard electromagnets, permanent guideway magnets, and linear motor. Optical sensors measure the air gap and are largely unaffected by these magnetic fields.

### Tradeoffs

#### Pros:
- directly measures the air gap
- immune to magnet interference
- Easier to calibrate because the output corresponds to physical distance.
- compatible with the planned IMU sensor fusion.

#### Cons:
- Requires a clear line of sight to the track.
- Performance will depend on reflectivity of the track surface.
- can be affected by dirt, dust or debris.
- Requires careful alignment during assembly.
- Generally more expensive than simple hall-effect sensors.
- 

