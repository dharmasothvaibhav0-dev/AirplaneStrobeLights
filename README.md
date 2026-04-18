# AirplaneStrobeLights


<img width="866" height="586" alt="image" src="https://github.com/user-attachments/assets/eff87671-6c38-4231-becd-d49229314a3d" />


### This project is designed to replicate the strobe lights seen on flights. The lights flash on the sides of the wings and the top and back of the plane for better visibility.
I got inspiration for this when I went to the airport and saw the planes with these flashing lights, and I wanted to replicate it. 

## Schematic-
<img width="1126" height="680" alt="schem" src="https://github.com/user-attachments/assets/b7f1d9d3-383e-4d48-b6d4-fd15b18f5fab" />


## PCB-

<img width="690" height="683" alt="PCBfronttt" src="https://github.com/user-attachments/assets/b63ddfeb-6bc6-4ebe-916b-2601529d8c20" />
<img width="693" height="676" alt="PCBbackk" src="https://github.com/user-attachments/assets/902f825f-b0d1-4f20-b4d3-935af1284bbb" />


## Assembly- 

Its important that you place the LEDS as 2 on the sides, 1 in the middle, and 3 in the back as it is how it is in real life.
I made it so every component can be placed on the top of the PCB, I tried to design it to where it still had a decent look once all components were placed. 

As soon as you connect the plane to a USB A port(5v), it should automatically turn on and the leds will start to flash very quick.

## Components-

This is made up of 10 resistors, **Its very important to know that resistor #1 is 8.2k, and resistor #2 is 1k** All the rest are 220, be very careful. Also **Capacitor 1 is .01u, and Capacitor 2 is 10u**. When placing said resistors and capacitors capacitor 2 goes on the left of the NE555, and Capacitor 1 goes to the right. Resistor 1 goes to the top of capcitor 2, and resistor 2 goes to the top of capacitor 1. its VERY important you place them in the correct spots as seen below.
<img width="1381" height="642" alt="image" src="https://github.com/user-attachments/assets/0ff0c12b-2ca9-4f76-a7f8-9b844fda407f" />

## Bill of Materials (BOM)

| Id                               | Footprint                                         | Quantity | Value   |
|----------------------------------|---------------------------------------------------|----------|---------|
| C1                               | C_Disc_D8.0mm_W5.0mm_P5.00mm                      | 1        | 0.01uF  |
| C2                               | C_Disc_D8.0mm_W5.0mm_P5.00mm                      | 1        | 10uF    |
| D1, D2, D3, D4, D5, D6, D7, D8   | LED_D5.0mm                                        | 8        | LED     |
| J1                               | USB_A_Molex_67643_Horizontal                      | 1        | USB_A   |
| R1                               | R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal  | 1        | 8.2kΩ   |
| R2                               | R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal  | 1        | 1kΩ     |
| R4, R5, R6, R7, R8, R9, R10, R11 | R_Axial_DIN0204_L3.6mm_D1.6mm_P7.62mm_Horizontal  | 8        | 220Ω    |
| U1                               | DIP-8_W7.62mm                                     | 1        | NE555P  |
| U2                               | DIP-16_W7.62mm                                    | 1        | CD4017  |

# I hope you enjoy building this!
