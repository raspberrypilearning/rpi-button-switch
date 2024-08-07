## Using buttons to get input

+ Connect a button to a GND pin and GPIO pin 2, like this:

    ![](images/button.png)

+ Create a new file by clicking **New**.

+ Save the new file by clicking **Save**. Save the file as `gpio_button.py`.

+ Import the `Button` class, and tell it that the button is on pin 2. Write the following code in your new file:

    ```python
    from gpiozero import Button
    button = Button(2)
    ```

+ Now you can get your program to do something when the button is pushed. Add these lines:

    ```python
    button.wait_for_press()
    print('You pushed me')
    ```

+ Save and run the code.

+ Press the button and your text will appear.
