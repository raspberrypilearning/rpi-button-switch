## Light an LED with a Button

Control an LED using the button.

--- task ---

Connect the long leg of an LED to pin 17 and the short leg to a GND pin.

--- /task ---

--- task ---

Create a new file by clicking **New**.

--- /task ---

--- task ---

Save the new file by clicking **Save**. Save the file as `gpio_control.py`.

--- /task ---

--- task ---

Now write the following code:

    ```python
    from gpiozero import LED, Button
    from time import sleep

    led = LED(17)
    button = Button(2)

    button.wait_for_press()
    led.on()
    sleep(3)
    led.off()
    ```

--- /task ---

--- task ---

Save and run your program. When you push the button the LED should come on for three seconds.

--- /task ---




