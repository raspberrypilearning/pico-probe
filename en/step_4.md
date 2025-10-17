## Program the sensor

--- task ---

Add the libraries needed to access the Pico’s analogue input and timing functions.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1-2
---

from machine import Pin, ADC  
from time import sleep
--- /code ---

--- /task ---

--- task ---

Set up the Pico to read the analogue signal from **Pin 26**, which is connected to the soil moisture probe.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 4
---
from machine import Pin, ADC  
from time import sleep

sensor = ADC(26)  # Soil probe input
--- /code ---

--- /task ---

--- task ---

Continuously take readings from the soil probe, print them to the Shell, and pause briefly before the next reading.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 6-9
---
from machine import Pin, ADC  
from time import sleep

sensor = ADC(26)  # Soil probe input

while True:  
    reading = sensor.read_u16()  
    print("Soil moisture:", reading)  
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Click **Run** and watch the changing moisture readings as you touch or insert the probes into soil.

--- /task ---

--- task ---

Test the probe behaviour:  
- Touch the two screws together with some metal — the reading should drop (low resistance).  
- Separate them — the reading should rise (high resistance).  
- Insert into wet soil — readings should decrease.  
- Insert into dry soil — readings should increase.
- Insert into damp soil — readings should be somewhere in the middle.

--- /task ---

--- task ---

Note down the typical readings for “wet,” “damp,” and “dry” soil to prepare for the next step, where you’ll add an LED alert to tell you if it's too dry.

--- /task ---
