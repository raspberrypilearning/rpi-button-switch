## Using buttons to get input

--- task ---

Connect a button to a GND pin and GPIO pin 2, like this:

![Diagram showing a red push button connected on a breadboard, with two wires—one blue and one black—connecting the button to a Raspberry Pi GPIO header.](images/button.png)

--- /task ---

--- task ---

Create a new file by clicking **New**.

--- /task ---

--- task ---

Save the new file by clicking **Save**. Save the file as `gpio_button.py`.

--- /task ---

--- task ---

Import the `Button` class, and tell it that the button is on pin 2. Write the following code in your new file:

```python
from gpiozero import Button
button = Button(2)
```

--- /task ---

--- task ---

Now you can get your program to do something when the button is pushed. Add these lines:

```python
button.wait_for_press()
print('You pushed me')
```

--- /task ---

--- task ---

Save and run the code.

--- /task ---

--- task ---

Press the button and your text will appear.

--- /task ---







