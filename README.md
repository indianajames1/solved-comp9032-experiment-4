Download Link: https://assignmentchef.com/product/solved-comp9032-experiment-4
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">1.  Objectives</span>




In this lab, you will gain more practical experience on microcontroller interfacing.

Specifically, your tasks in this lab are

<ul>

 <li>studying Dot Matrix LCD and programming LCD to display output data, and</li>

 <li>studying the DC motor and programming to detect and control the motor speed.</li>

</ul>







<h1>2.  Preparation</h1>




Before coming to the laboratory, you should:

<ul>

 <li>read through the document available at www.cse.unsw.edu.au/~cs9032/references/Documents/LCD_Manual.pdf for general description of Dot Matrix LCD,</li>

 <li>read the Atmega2560 data sheet on how to use Timer 0 to generate Phase Correct PWM signals,</li>

 <li>read through the task description of this experiment, and write your programs at home in order to finish the experiment on time.</li>

</ul>







<h1>3.     Introduction to the DMC LCD and the DC Motor</h1>




3.1       DMC LCD




The AVR Microcontroller Board comes with a 2 × 16 character Liquid Crystal Display (LCD) module. This module can be controlled via an ATmega2560 port.




In order to read/write from/to the LCD, here is the list of things you must perform:

<ul>

 <li>Initializing LCD,</li>

 <li>Checking the busy flag of LCD,</li>

 <li>Determining which register (instruction register or data register) in the LCD controller to write to or read from,</li>

 <li>Writing/reading data or instruction to/from the LCD.</li>

</ul>




The pin descriptions, timing constraints and detailed instruction specifications can be found in the LCD User’s Manual.




3.2       DC Motor




The motor on the AVR Microcontroller Board is DC voltage driven. It takes the input electrical energy and converts it to rotating motion. The motor is attached to a disc. The disc has four holes.




The speed of the motor is measured in revolutions per second (rps).

To determine the motor speed, we use the shaft encoder. The encoder uses the infrared light emitter and detector that are each placed on the different side of the disc. When a hole of the disc lies between the emitter and the detector, the light can pass through the hole and turn on the detector. When the opaque section of the disc lies between the emitter and the detector, the light is blocked and the detector is off.




Examine the motor and shaft encoder on the AVR Microcontroller Board. Can you identify the emitter and the detector? The emitter is active high (i.e OpE=1) and the detector is active low (namely, OpO will go low when it can see the light). For the further circuit information, please refer to the “I/O Connection Diagram” available on the References page of the course website.




Power up the AVR Microcontroller board and connect the pin named as POT to the MOT pin on the lab board. As you turn the POT (potentiometer), the speed of the motor changes accordingly.




You can measure the motor speed by counting the number of holes the shaft encoder detects per second and the motor speed is the value divided by 4.










<h1>4.  Tasks</h1>







4.1       Task 1 (6 marks, for week 9, due week 10)




Write an assembly program that displays characters inputted from the keypad on the LCD. When the first line is full, the display goes to the second line. When the two lines are all full, the display is cleared and ready to display a new set of characters.







Assemble your program using AVR Studio, and run it on the AVR Microcontroller Board. Demonstrate your working program to the laboratory tutor.













4.2      Task 2 (6 marks, for week 9, due week 10)




Write an assembly program to control the motor operations. When a button is pressed, the motor spins at its full speed. When the button is pressed again, the motor stops.




Assemble your program using AVR Studio, and run it on the AVR Microcontroller Board. Demonstrate your working program to the laboratory tutor.










4.2.1 Task 3 (7 marks, for week 9, due week 11)







Write an AVR assembly language program that measures the speed of the motor (based on the number of holes that are detected by the shaft encoder) and displays the speed on LCD. The motor speed can be adjusted by the POT (potentiometer).







Assemble your program using AVR Studio, and run it on the AVR Microcontroller Board. Demonstrate your working program to the laboratory tutor.