# Home-Automation-System-with-IOT

## AIM:

To interface an LED with a Raspberry Pi Pico and write a MicroPython program to blink the LED at regular time intervals using the Wokwi online simulator.

## COMPONENTS REQUIRED:
PC/Laptop with Internet connection
Wokwi Online Simulator
Raspberry Pi Pico
LED
220 Ω Resistor
Jumper Wires
MicroPython Programming Environment

## THEORY:

The Raspberry Pi Pico is a low-cost microcontroller development board based on the RP2040 microcontroller. It provides several General-Purpose Input/Output (GPIO) pins that can be configured as either input or output.

An LED (Light Emitting Diode) is an electronic component that produces light when current flows through it in the forward direction. Since excessive current can damage an LED, a current-limiting resistor is connected in series with the LED.

In this experiment, the LED is connected to one of the GPIO pins of the Raspberry Pi Pico. The GPIO pin is configured as an output using MicroPython. When the GPIO pin is set to HIGH, voltage is applied to the LED and it turns ON. When the GPIO pin is set to LOW, the LED turns OFF.

The Pin class from the machine module is used to configure and control the GPIO pin. The sleep() function from the utime module introduces a delay between the ON and OFF states. By continuously switching the GPIO pin between HIGH and LOW, the LED blinks at a regular interval.

Wokwi is an online electronics simulator that allows microcontroller circuits and programs to be designed and tested virtually without requiring physical hardware. It can simulate Raspberry Pi Pico, LEDs, sensors and other electronic components.

## PROCEDURE:

1. Open the Wokwi online simulator and create a new Raspberry Pi Pico project.

2. Place a Raspberry Pi Pico, LED, and 220 Ω resistor in the simulation workspace.

3. Connect the GPIO pin GP5 of the Raspberry Pi Pico to the anode (positive terminal) of the LED through the 220 Ω resistor.

4. Connect the cathode (negative terminal) of the LED to the GND pin of the Raspberry Pi Pico.

5. Select MicroPython as the programming language.

6. Write the MicroPython program to configure GP5 as an output pin.

7. Use the `toggle()` function to alternately switch the LED between ON and OFF states.

8. Use the `sleep()` function to provide a delay of 0.5 seconds between each state.

9. Start the simulation using the Run button.

10. Observe that the LED continuously turns ON and OFF at regular intervals.

11. Verify that the LED blinks continuously as long as the simulation is running.
# CIRCUIT DIAGRAM:

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/57082b36-7da7-4308-a0f5-63bd17287491" />


 
# PROGRAM:
```
from machine import Pin
from utime import sleep

sleep(0.01)  # Wait for USB to connect
print("Hello, Pi Pico!")

led = Pin(5, Pin.OUT)

while True:
    led.toggle()
    sleep(0.5)
 ```
# Output:

<img width="1906" height="871" alt="image" src="https://github.com/user-attachments/assets/c3edfe91-d9df-425b-b539-1b2d3959c5ac" />



## Result:
The Raspberry Pi Pico LED blinking experiment was successfully implemented and simulated using Wokwi.






