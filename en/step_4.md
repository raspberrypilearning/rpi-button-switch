## Making a switch with a button

With a switch, a single press and release on the button would turn the LED on, and another press and release would turn it off again.

--- task ---

Modify your code so that it looks like this:

```python
from gpiozero import LED, Button
from time import sleep

led = LED(17)
button = Button(2)

while True:
    button.wait_for_press()
    led.toggle()
    sleep(0.5)
```

--- /task ---

`led.toggle()` switches the state of the LED from on to off, or off to on. Since this happens in a loop the LED will turn on and off each time the button is pressed.

--- task ---

It would be great if you could make the LED switch on only when the button is being held down. With GPIO Zero, that's easy. There are two methods of the `Button` class called `when_pressed` and `when_released`. These don't block the flow of the program, so if they are placed in a loop, the program will continue to cycle indefinitely.

--- /task ---

--- task ---

Modify your code to look like this:

```python
from gpiozero import LED, Button
from signal import pause

led = LED(17)
button = Button(2)

button.when_pressed = led.on
button.when_released = led.off

pause()
```

--- /task ---

--- collapse ---
---
title: Running as a script
---

In this code, `pause()` keeps the program running so the button can control the LED. Without `pause()`, the script would end right after setting up, and the button wouldn't work. It essentially tells the program to "wait here" so that it can continue responding to the button events, allowing the LED to turn on or off when the button is pressed or released. While you are working in Thonny, this isn't so important. 

--- /collapse ---

--- task ---

Save and run the program. Now when the button is pressed, the LED will light up. It will turn off again when the button is released.

--- /task ---