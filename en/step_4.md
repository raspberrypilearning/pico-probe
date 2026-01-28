## Program the sensor

If you need help getting ready to program your Raspberry Pi Pico, check out our ['Getting started with Raspberry Pi Pico' guide](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/2){:target="_blank"} for support.

--- task ---

Open a **new script** in your code editor.

--- /task ---

--- task ---

Add the `picozero` and `time` classes you need to access the Raspberry Pi Pico's input and timing functions.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1-2
---

from picozero import Pot
from time import sleep
--- /code ---

--- /task ---

--- task ---

Set up the Raspberry Pi Pico to read the analogue signal from **GP26**, which is connected to **Probe A**.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 4
---
from picozero import Pot
from time import sleep

sensor = Pot(26)  # moisture probe input
--- /code ---

--- /task ---

--- task ---

Add code to continuously take readings from the moisture probe, print them to the Shell, and pause briefly before the next reading.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6-9
---
from picozero import Pot
from time import sleep

sensor = Pot(26)  # moisture probe input

while True:  
    reading = sensor.value  
    print("Soil moisture:", round(reading, 2))  
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Click on **Run** and watch the moisture readings change as you touch the probe to different items or insert the probe into soil.

--- /task ---

--- task ---

Test the probe's behaviour:  
- Use some metal to touch the two screws together — the readings should decrease (low resistance) 
- Separate the screws — the readings should increase (high resistance)
- Insert the probe into wet soil — the readings should decrease
- Insert the probe into dry soil — the readings should increase
- Insert the probe into damp soil — the readings should be somewhere in the middle

--- /task ---

--- task ---

Write down the typical readings for 'wet', 'damp', and 'dry' soil to prepare for the next step, where you will add an LED warning light to alert you if the soil is too dry.

--- /task ---
