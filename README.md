# AirplaneStrobeLights


<img width="866" height="586" alt="image" src="https://github.com/user-attachments/assets/eff87671-6c38-4231-becd-d49229314a3d" />


### This project is designed to replicate the strobe lights seen on flights. The lights flash on the sides of the wings and the top and back of the plane for better visibility.
I got inspiration for this when I went to the airport and saw the planes with these flashing lights, and I wanted to replicate it. 

## Schematic-
<img width="1205" height="710" alt="schem" src="https://github.com/user-attachments/assets/6664f1c7-2568-47fb-aefc-1a8f94d4bdc8" />

## PCB-

<img width="670" height="617" alt="PCBFRONTT" src="https://github.com/user-attachments/assets/73790cd5-ce06-4392-a4d5-733b99e34d33" />
<img width="635" height="615" alt="PCBBACKK" src="https://github.com/user-attachments/assets/dd004efa-e1ca-4752-b961-f14c3a8562a6" />

## Assembly- 

Its important that you place the LEDS as 2 on the sides, 1 in the middle, and 3 in the back as it is how it is in real life.
I made it so every component can be placed on the top of the PCB, I tried to design it to where it still had a decent look once all components were placed. 

As soon as you connect the plane to a USB A port(5v), it should automatically turn on and the leds will start to flash very quick.

## Components-

This is made up of 10 resistors, **Its very important to know that resistor #1 is 8.2k, and resistor #2 is 1k** All the rest are 220, be very careful. Also **Capacitor 1 is .1u, and Capacitor 2 is 10u**. When placing said resistors and capacitors capacitor 2 goes on the left of the NE555, and Capacitor 1 goes to the right. Resistor 1 goes to the top of capcitor 2, and resistor 2 goes to the top of capacitor 1. its VERY important you place them in the correct spots as seen below.
<img width="358" height="177" alt="image" src="https://github.com/user-attachments/assets/8e32fc50-4246-42d8-b0ad-7ef73a2d9c97" />


The entire BOM can be seen in the production files. But in short the pcb is made up of 8LEDS, 10 Resistors(1 8.2k, 1 1k, 8 220), 2 capacitors(1 .1u, 1 10u), a USB a connection as the power source, a NE555, and a CD4017.

# I hope you enjoy building this!
