Programming the Raspberry Pi
===========================

The Raspberry Pi is very small computer that you can use to build projects that light up, move, sense and respond to people, animals, plants and the rest of the world. We are going to use the Raspberry Pi with LEDs and photo resistors. You may want to watch [this 5 minute video](https://www.youtube.com/watch?v=5jA8wYqQLBU&t=34s) for a quick overview of the Raspberry Pi. You may also find the [Raspberry Pi PowerPoint slides](https://drive.google.com/open?id=0Bz2ZkT6qWPYTQk85WklyVml2M00) helpful. In this assignment, you and a partner will build and program a series of projects. There is nothing to turn in for this assignment. When you get one of the following projects working, call your instructor over to show them, and then start working on the next

Blinking LED
---------------
Our first project will be to create a circuit with a single LED. First, create a test circuit like the one shown on slides 12 and 13 to check that your breadboard is powered. Then move the jumper from the + power rail so that it connects to pin 4. Open Processing and find the SimpleOutput program in *File | Examples | Libraries | Hardware I/O*. Show your instructor when you have your blinking LED working. If you have extra time, try connecting the jumper to pin 17 and rewriting the program to work from that pin. 

Multiple LEDs that blink in a random pattern
---------------
You will create a circuit with at least 4 LEDs. Any pin marked with green on slide 11 can be used for output (e.g. 17, 18, 22, 24, 27). Your working program should store the 4 output pin numbers in an array. In `setup()` set the pin mode of each of the pins you choose to output. In `draw()`, randomly choose a pin using `Math.random()`. See slides 20 - 21 for a sample circuit and program. When you have your program working, call your instructor over to show him.

LEDs that are controlled by buttons
------------------
You will create a circuit with at least 2 LEDs and 2 buttons. You will then write a program that allows a user to turn the LEDs on and off with the buttons. First, just connect one button. Connect the button to pin 4 and -. To test the circuit, run the SimpleInput program. Pressing the button should change the fill of the ellipse. Now add an LED that connects to - through a 220 Ohm resistor. The + lead on the LED should connect to a different pin like 17. Add code so that if `GPIO.digitalRead(4)` is High, then set `GPIO.digitalWrite(17,GPIO.HIGH)`. Add another button, LED and resistor. Call your instructor over to see the working circuit.

Move a circle by casting a shadow on a photo resistor
------------------
You will create a circuit with photo resistor and a capacitor. The capacitor connects from - power rail to one lead of the photoresitor. That same lead of the photoresistor will also connect to pin 4. The other lead of the photoresitor connects to 3.3V + on the power rail. The photoresistor senses the amount of light that reaches it. The capacitor charges like a battery. We’ll measure how long it takes to charge the capacitor and that will tell us how much light is reaching the photoresistor. You can find some sample code on slide 30 of the PowerPoint. Call your instructor over to see the working circuit.
