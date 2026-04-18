

## 4/17/2026

I was at the airport today to drop my dad off, and I noticed how airplanes have these LEDS(Strobe lights) On the front, wing, and tail of the plane. I noticed how they would all blink one after another and this gave me inspiration of the project I am making today.

First I started off with finding a reference image to how I wanted to shape my PCB, and where i wanted to keep my LEDS on the PCB 
<img width="611" height="624" alt="image" src="https://github.com/user-attachments/assets/6a383323-1b41-4565-ab53-a1205fc9f132" />

The numbers in the circles correspond to what order i want the LEDS to light up in. So essentially it would all light up sequentially in order. And I'm still debating on whether i should make all of the LEDS light up at the end and then reset, or just reset once its done with the cycle.
_______________________________________________________________________________

So, while thinking of how this entire circuit would work, I landed on using 2 IC's that I've previously used before: The NE555, and the CD4017B. The NE555 would be in astable mode giving pulses to the CD4017 which will cycle through the LEDS.

Looking at the IC's datasheets, it helped me out with the schematic of creating the astable function for the NE555.

<img width="269" height="402" alt="image" src="https://github.com/user-attachments/assets/c980a789-a33a-4197-bf25-1c28156477e1" />


I want the LEDs to flash relatively quick, so I made it to where it would do a full cycle in around 1 second. It took me a while to understand how the calculations actually worked, but when looking online I found this amazing website that helps you out(https://www.digikey.com/en/resources/conversion-calculators/conversion-calculator-555-timer?utm_source=online&utm_medium=vanity&utm_campaign=555timer). This is the full NE555 circuit, and now we must connect it to the CD4017 circuit. 

<img width="628" height="547" alt="image" src="https://github.com/user-attachments/assets/05f46664-e397-4916-b382-babf91dcc5da" />


This is the full cd4017 circuit. We want it to reset once it fully cycles so its important to set pin 9 to reset, so once the cycle reaches output 8 it goes back to output 1.

<img width="1168" height="715" alt="image" src="https://github.com/user-attachments/assets/1e8d67de-2cde-416c-957f-7c016cce7dc1" />


And this is the full schematic connected. I used a USB - A as a powersource for this. I changed my mind with making all the LEDS light up at the end because I felt it might be too extra, and I didn't really feel like doing all the attaching. But if anyone else wants to do it all they would have to do is move the reset connection to Q9, and on Q8, you want to connect a wire to each of the the outputs.
<img width="1172" height="611" alt="image" src="https://github.com/user-attachments/assets/64987977-6b0b-4a56-9747-5a9e47f15ad8" />


It would basically look like this. 

_______________________________________________________________________________
Now that the schematic is done, its time to move onto the actual PCB.
My first step is to draw the Airplane layout for the PCB.
<img width="590" height="593" alt="image" src="https://github.com/user-attachments/assets/0c385e5f-a055-479b-80b8-94c79a6fd30e" />

From here onwards, the placement should be pretty simple, as its just aligning where the LEDS go, and after that the wiring will be pretty rough as it always is for me I'm assuming.
<img width="681" height="676" alt="image" src="https://github.com/user-attachments/assets/42869a1f-d827-4b65-bfef-9d6be97862d6" />



This is the completed Placement. The hardest thing about this was trying to keep every component reasonably placed so that it would be easy while soldering etc.

Top wirings:
<img width="690" height="683" alt="PCBfronttt" src="https://github.com/user-attachments/assets/a1611e39-8789-4247-8c54-6949ec102b4e" />


Bottom Wirings:
<img width="693" height="676" alt="PCBbackk" src="https://github.com/user-attachments/assets/262696f1-5e9f-422f-8b68-7fced165f5f9" />


The Wiring was very tedious to do, as when I tried to do it all on one layer it wasn't working out there was just going to be overlapping. I decided to use the top layer to mostly route the LEDS To the resistors and the CD4017,and the Capacitors to the NE555. I decided to use the back layer to wire the resistors to the CD4017 and the NE555 and any resistors that I was unable to wire on the bottom I just wired on top.
_______________________________________________________________________________
3d render
<img width="1088" height="925" alt="3ddd" src="https://github.com/user-attachments/assets/937aede0-1b5c-4056-b0e8-b22076db3227" />


## Time taken for schematic: ~90 minutes 

## time for pcb: 120 minutes (2hours)

# total time: 3 hours 30minutes

