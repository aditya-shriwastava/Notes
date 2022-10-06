# Tesla AI Day

**Battery Pack:**
* cells + integrated electronics

**Bot Brain:**
* SoC + WiFi + LTE + Audio + Security & Safety

* 4 bar linkage at knee.

* 6 diff actuator in entire tesla bot.
  * 3 rotary actuator
    + Mechanical clutch on high speed side
    + [Strain wave gearing i.e. harmonic gearing](https://en.wikipedia.org/wiki/Strain_wave_gearing)
    + Sensors:<br>
      [Input] --> [motor] --> [Gear reduction] --> [Output]
      + Input position sensor
      + Output position sensor
      + non-contacttorque sensor
  * 3 linear actuator

**Visual Odometry:**
- NN to identify high hz features (i.e. keypoints) within the bots camera stream and track then access frames over time as the bot navigates.

**Walking:**
* Physical self-awareness.
* Energy-Efficient Gait.
  + **Gate:** Pattern of limb movement made during locomotion.


[Desired Path] --> [Locomotion Planes] --> [References Tragectory]

```mermaid
flowchart LR
	se[State Estimation]
	mc[Motion Control]
	rb[Real Behavior]
	r[Reality]

	se --> mc --> rb
	rb --> r --> se
```
