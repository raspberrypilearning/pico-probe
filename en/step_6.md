## Code the LED indicator

Edit your existing program so that an LED lights up when the soil is too dry.  

--- task ---

Edit the first line so it imports both the **Pot** and **LED** classes from picozero.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 1
---

from picozero import Pot, LED
from time import sleep

sensor = Pot(26)  # Soil probe input

while True:
    reading = sensor.value()
    print("Soil moisture:", round(reading, 2))
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Below your existing line that defines the soil sensor, add a new line to define the LED.  
This tells the Pico that there’s an LED connected to **Pin 14** (the pin you wired it to).

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 5
---

from picozero import Pot, LED
from time import sleep

sensor = Pot(26)       # Soil probe input
led = LED(14)          # LED output pin

while True:
    reading = sensor.value()
    print("Soil moisture:", round(reading, 2))
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Above your loop, add a new line to define the dryness threshold.  
Compare your readings against this value to decide when the LED should turn on.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 7
---

from picozero import Pot, LED
from time import sleep

sensor = Pot(26)       # Soil probe input
led = LED(14)          # LED output pin

dry_limit = 0.6        # Adjust this number after testing

while True:
    reading = sensor.value
    print("Soil moisture:", round(reading, 2))
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Inside the `while True:` loop, add an `if` statement to compare the reading to your dryness limit.  
**If** the soil is too dry, the LED turns on. **Otherwise**, it stays off.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 13-16
---

from picozero import Pot, LED
from time import sleep

sensor = Pot(26)       # Soil probe input
led = LED(14)          # LED output pin

dry_limit = 0.6        # Adjust this number after testing

while True:
    reading = sensor.value
    print("Soil moisture:", round(moisture, 2))

    if reading > dry_limit:     # Soil is too dry
        led.on()
    else:                        # Soil is fine
        led.off()
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Click **Run** to test your code.  
When the probe is in dry soil, the LED should light up.  
When the soil is damp or wet, the LED should stay off.  
Adjust the `dry_limit` number if needed so the LED changes state at the right point.

--- /task ---
