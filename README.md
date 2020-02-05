# Color-Sensor
Color sensor using LDR, RGB LED and Arduino
To make reliable color sensor using a microcontroller (Arduino), an RGB LED (WS2812B), a LDR and a  resistor. The sensor can pick up colors from a surface and detected color value or code.
Important points:
The LDR should only be exposed to the reflected light from the surface which was emitted by the RGB LED.
Light from the RGB LED should not directly goes to the LDR and light from the surrounding should be eliminated.

Proper calibration of sensor should be done.
We need to have black and white color material.If the sensor is going to be used to detect colors from a clothe, when calibrating the sensor, it needs to be calibrated using black and white color papers. If the sensor was calibrated to one material it tries to detect color from surrounding, which is not accurate.

Basic Idea:
LDR can be used to measure the intensity of light. The resistance between the two pins of an LDR will change depending on the intensity of the light. In this case the an RGB LED is used for illuminating the target surface with red, green and blue colors.While reflected light intensity was measured by an LDR.
The targeted surface is illuminated only by the RGB LED. Depending on the surface texture and the color the reflected intensity was reduced. Since a white surface will reflect every wavelength, intensity readings from a white surface is the highest reading among any other color on that particular surface and, lowest on a black colored surface.
During the calibration process the microcontroller will store the light intensity readings from the LDR for red, green and blue colors which is reflected from white and black color. These values are the highest and lowest values for that surface. Any readings taken should be in between these values.
When an RGB color reading was obtained from a surface the program will compare that values with the white and black values which was stored during the calibration and decides the color.
 
 For this sensor you will need:
a breadboard (not required, but it is how I will walk you through it.)
an RGB LED (alternatively you could use 3 LEDs)
A 220 ohm resistors
An Arduino
I have included both images of the breadboard arrangment, and a small diagram to show you how to wire up the sensor to the Arduino.
The circuit is really simple. First we will look at the RGB LED half of the sensor. It is simply a common cathode RGB LED connected to pins 2,3, and 4 of the Arduino with a 220 ohm resistor going out to ground. This will allow us to turn each of the LEDs within the package on and off individually when we need to.    
  This sensor works great on a breadboard, but it works even better if you put it into a more permanent enclosure to minimilize ambient light.
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
