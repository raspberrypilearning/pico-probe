## Wire the sensor circuit

Connect the probe to the pins on the Raspberry Pi Pico so that you can measure the resistance of the soil.


--- task ---
 
Set your Raspberry Pi Pico securely on a breadboard or workspace so that you can easily access all the pins for wiring.
![A Raspberry Pi Pico H mounted into a breadboard, aligned with the top row.](images/probe1.png){:width="300px"} 

--- /task ---

--- collapse ---

---

title: I have a moisture probe component — I don't want to use screws!

---

The moisture probe component will require a power supply to work. Follow these instructions to use a moisture probe component instead of a probe that you have built with screws:

--- task ---

Connect the **VCC** pin on the moisture sensor to the **3V3 (OUT)** pin on the Raspberry Pi Pico (pin **36**). This will provide the sensor with a 3.3V power supply. 
![The VCC pin on a soil moisture sensor has been connected to the 3V3 pin on the Raspberry Pi Pico with a jumper wire.](images/probe_probe_3.png){:width="300px"} 

--- /task ---

--- task ---

Connect the **GND** pin on the moisture sensor to one of the **GND** pins on the Raspberry Pi Pico (pin **38**). This will complete the power circuit.  
![The GND pin on the soil moisture sensor has been connected to a GND pin on the Raspberry Pi Pico with a jumper wire.](images/probe_probe_2.png){:width="300px"}

--- /task ---

--- task ---

Attach a jumper wire from the **SIG** (signal) pin on the moisture sensor to pin **31 (GP26/ADC0)** on the Raspberry Pi Pico. This will allow the Raspberry Pi Pico to read the analogue signal that represents the soil moisture level. 
![The SIG pin on the soil moisture sensor has been connected to GP26 on the Raspberry Pi Pico with a jumper wire.](images/probe_probe_1.png){:width="300px"} 

--- /task ---

--- task ---

**Test:** Make sure that there are no short circuits or loose connections:
- Gently move each jumper wire at each connection point to check that there is a firm connection between the pins on the sensor and the breadboard
- Double-check that the probe does not come into contact with the Raspberry Pi Pico or any metal parts of your workspace

--- /task ---

--- task ---

Now, move on to the [next step](https://projects.raspberrypi.org/en/projects/pico-probe/3){:target="_blank"} to continue the project!

--- /task ---

--- /collapse ---

--- task ---
 
Connect the jumper wire attached to **Probe A** to one end of a **10kΩ resistor** with a **terminal block** in the breadboard.
![The jumper wire attached to Probe A has been connected to one end of a resistor via a terminal block.](images/screws_probe_00.png){:width="300px"}

--- /task ---

--- task ---
 
Connect the other end of the resistor to pin **31 (GP26/ADC0)** on the Raspberry Pi Pico. This pin will read the changing voltage from the probe.
![A jumper wire has been connected from the other end of the resistor to GP26 on the Raspberry Pi Pico.](images/screws_probe_0.png){:width="300px"}

--- /task ---

--- task ---

Connect the jumper wire attached to **Probe B** to one of the **GND** pins on the Raspberry Pi Pico to complete the ground connection.
![The jumper wire attached to Probe B has been connected to a GND pin on the Raspberry Pi Pico via the terminal block.](images/screws_probe_1.png){:width="300px"}

--- /task ---

--- task ---

**Test:** Make sure that there are no short circuits or loose connections:  
- Check that **Probe A** and **Probe B** are not touching or connected through any conductive path
- Gently move each jumper wire at each connection point to check that the components are connected securely
- Double-check that the probe assembly and screws do not come into contact with the Raspberry Pico or any metal parts of your workspace

--- /task ---
