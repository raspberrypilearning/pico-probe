## Wire the Sensor Circuit

Connect the metal screws to the pins on the Pico so you can measure the resistance of the soil.

--- task ---
 
Set the Raspberry Pi Pico securely on a breadboard or workspace so you can easily access all pins for wiring.
![](images/probe1.png)

--- /task ---

--- task ---
 
Join a wire from **Probe A** to one end of a **10 kΩ resistor**; with a **terminal block** in the breadboard.
![](images/screws_probe_00.png){:width="300px"}

--- /task ---

--- task ---
 
Attach the free end of the resistor to **Pin 26 (ADC0)** on the Pico. This pin reads the changing voltage from the probe.
![](images/screws_probe_0.png){:width="300px"}

--- /task ---

--- task ---

Attach a jumper wire from **Probe B** to one of the **GND** pins on the Pico to complete the ground connection.
![](images/screws_probe_1.png){:width="300px"}

--- /task ---

--- task ---

**Test:** Make sure there are no short circuits or broken connections:  
- Confirm that **Probe A** and **Probe B** are not touching or connected through any conductive path.
- Gently move each jumper and connection to check there is a firm connection between the pins and breadboard.
- Double-check that the probe assembly and screws don't contact the Pico board or any metal parts of your workspace.

--- /task ---
