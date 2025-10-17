## Wire the Sensor Circuit

Connect the metal screws to the pins on the Pico so you can measure the resistance of the soil.

--- task ---
 
Set the Raspberry Pi Pico securely on a breadboard or workspace so you can easily access all pins for wiring.
![](images/probe1.png)

--- /task ---

--- task ---
 
Join a wire from **Probe A** to one end of a **10 kΩ resistor**; this resistor limits current and enables voltage measurement. In this diagram we have used a **terminal block** to join the trailing wires that connect to the sensor.
![](images/screw_probe0.png)

--- /task ---

--- task ---
 
Attach the free end of the resistor to **Pin 26 (ADC0)** on the Pico; this pin reads the analogue voltage from the probe.
![](images/screw_probe1.png)

--- /task ---

--- task ---

Attach a jumper wire from **Probe B** (one of the screws) to one of the **GND** pins on the Pico to complete the ground connection.
![](images/screw_probe2.png)

--- /task ---

--- task ---

**Test:** Make sure there are no short circuits or broken connections:  
- Confirm that **Probe A** and **Probe B** are not touching or connected through any conductive path.
- Gently wiggle each jumper and resistor lead to ensure solid connections to the pins and breadboard.
- Double-check that the probe assembly and screws don't contact the Pico board or any metal parts of your workspace.

--- /task ---
