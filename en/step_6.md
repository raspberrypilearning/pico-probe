## Program the LED indicator

Edit your existing program so that the LED lights up when the soil is too dry.  

--- task ---

Edit the first line so that it imports both the `Pot` and `LED` classes from `picozero`.

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

sensor = Pot(26)  # moisture probe input

while True:
    reading = sensor.value
    print("Soil moisture:", round(reading, 2))
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Below your line that defines the soil moisture sensor, add a new line to define the LED. This will tell the Raspberry Pi Pico that there is an LED connected to **GP15** (the pin you wired it to).

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

sensor = Pot(26)       # moisture probe input
led = LED(15)          # LED output pin

while True:
    reading = sensor.value
    print("Soil moisture:", round(reading, 2))
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Above your loop, add a new line to define the dryness threshold. Compare your readings against this value to decide when the LED should turn on.

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

sensor = Pot(26)       # moisture probe input
led = LED(15)          # LED output pin

dry_limit = 0.6        # adjust this number after testing

while True:
    reading = sensor.value
    print("Soil moisture:", round(reading, 2))
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Inside the `while True:` loop, add an `if` statement to compare the reading to your dryness threshold. **If** the soil is too dry, the LED will turn on. **Else**, it will stay off.

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

sensor = Pot(26)       # moisture probe input
led = LED(15)          # LED output pin

dry_limit = 0.6        # adjust this number after testing

while True:
    reading = sensor.value
    print("Soil moisture:", round(reading, 2))

    if reading > dry_limit:     # soil is too dry
        led.on()
    else:                        # soil is fine
        led.off()
    sleep(1)
--- /code ---

--- /task ---

--- task ---

Click on **Run** to test your code. When the probe is in dry soil, the LED should light up. When the soil is damp or wet, the LED should stay off.

If you need to, adjust the `dry_limit` number so that the LED changes state at the right point.

--- /task ---
