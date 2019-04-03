# Practical-Pi  /  Jack Pender, David White, Jake Halley

## Practical NO.1
The first of the practicals for the Raspberry Pi dealt with a simple program printing out "Hello World!". Here is the output of the program once it had been run: 
![56547427_1830440127057889_7401713167799156736_n](https://user-images.githubusercontent.com/44526174/55517407-378bb100-5668-11e9-8976-bc87c0199d8a.jpg)

Here is what the code looked like: 

- #!/usr/bin/python
- #Print Hello world
- print "Hello World!"

## Practical NO.2
The second of the practicals focussed on turning on and off a set of LEDs. Here is the code used to do that:

- #!usr/bin/python
- **import** RPi.GPIO **as** GPIO
-
- GPIO.setmode(GPIO.BCM)
-
- GPIO.setup(17, GPIO, OUT)
- GPIO.setup(27, GPIO, OUT)
- **print** "Lights on"
-
- GPIO.output(17, GPIO, HIGH)
- GPIO.output(27, GPIO, HIGH)

In order to turn the light off the last four lines of code were changed to: 

- **print** "lights off"
-
- GPIO.output(17, GPIO, LOW)
- GPIO.output(27, GPIO, LOW)

Here is the GPIO setup:
insert pic

## Practical NO.3
In this practical the Raspberry Pi was used to make a set of lights blink. The code was as follows:

- #!usr/bin/python
-
- **from** time **import** sleep
- **import** RPi.GPIO **as** GPIO
-
- GPIO.setmode(GPIO.BCM)
-
- GPIO.setup(17, GPIO, OUT)
- GPIO.setup(27, GPIO, OUT)
-
- **while** True:
-- **print** "lights on"
-- GPIO.output(17, GPIO, HIGH)
-- GPIO.output(27, GPIO, HIGH)
--
-- sleep(1)
--
-- **print** "lights off"
-- GPIO.output(17, GPIO, LOW)
-- GPIO.output(27, GPIO, LOW
--
-- sleep(1)

This is how the GPIO setup looked:
insert image

## Practical NO.4
The final of the Raspberry Pi practicals involved 1)a push button for physical input and 2)a buzzer. The code used for the button looked like this:

- #!usr/bin/python
- **import** os
- **from** time **import** sleep
- **import** RPi.GPIO **as** GPIO
-
- GPIO.setmode(GPIO.BCM)
-
- GPIO.setup(10, GPIO.IN, pull_up_down=GPIO.PUD_UP)
-
- **while** True:
-- **if**( GPIO.input(10) == False ):
-- print("Button Pressed")
-- os.system('date)
-- **print** GPIO.input(10)
-- sleep(5)
--
-- **else**:
-- os.system('clear')
-- print("Waiting for you to press a button")
-- sleep(0.1)

And this is what the GPIO setup looked like:
insert image

For the buzzer part, this was the code used:

- #!usr/bin/python
-
- **import** os
- **from** time **import** sleep
- **import** RPi.GPIO **as** GPIO
-
- GPIO.setmode(GPIO.BCM)
- GPIO.setup(22, GPIO, OUT)
-
- **loop_count** = 0
-
- **def** morsecode ():
--
-- GPIO.output(22, GPIO, HIGH)
-- sleep(0.1)
-- GPIO.output(22, GPIO, LOW)
-- sleep(0.1)
--
- os.system('clear')
- **print** "Morse Code"
-
- **loop_count** = input("How many times would you like SOS to loop?: ")
- **while** **loop_count** > 0:
- **loop_count** = **loop_count**-1
- morsecode()

This was the setup of the GPIO:
insert image

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ginge2000/Practical-Pi/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.p
