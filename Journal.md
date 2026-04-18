

## 4/17/2026

I was at the airport today to drop my dad off, and I noticed how airplanes have these LEDS(Strobe lights) On the front, wing, and tail of the plane. I noticed how they would all blink one after another and this gave me inspiration of the project I am making today.

First I started off with finding a reference image to how I wanted to shape my PCB, and where i wanted to keep my LEDS on the PCB 
![[Pasted image 20260417155138.png]]
The numbers in the circles correspond to what order i want the LEDS to light up in. So essentially it would all light up sequentially in order. And I'm still debating on whether i should make all of the LEDS light up at the end and then reset, or just reset once its done with the cycle.
_______________________________________________________________________________

So, while thinking of how this entire circuit would work, I landed on using 2 IC's that I've previously used before: The NE555, and the CD4017B. The NE555 would be in astable mode giving pulses to the CD4017 which will cycle through the LEDS.

Looking at the IC's datasheets, it helped me out with the schematic of creating the astable function for the NE555.

![[Pasted image 20260417174432.png]]
I want the LEDs to flash relatively quick, so I made it to where it would do a full cycle in around 1 second. It took me a while to understand how the calculations actually worked, but when looking online I found this amazing website that helps you out(https://www.digikey.com/en/resources/conversion-calculators/conversion-calculator-555-timer?utm_source=online&utm_medium=vanity&utm_campaign=555timer). This is the full NE555 circuit, and now we must connect it to the CD4017 circuit. 

![[Pasted image 20260417174537.png]]
This is the full cd4017 circuit. We want it to reset once it fully cycles so its important to set pin 9 to reset, so once the cycle reaches output 8 it goes back to output 1.

![[Pasted image 20260417174638.png]]
And this is the full schematic connected. I used a USB - A as a powersource for this. I changed my mind with making all the LEDS light up at the end because I felt it might be too extra, and I didn't really feel like doing all the attaching. But if anyone else wants to do it all they would have to do is move the reset connection to Q9, and on Q8, you want to connect a wire to each of the the outputs. ![[Pasted image 20260417181940.png]]
It would basically look like this. 
# Time taken for schematic: ~90 minutes 

Now that the schematic is done, its time to move onto the actual PCB.
My first step is to draw the Airplane layout for the PCB.
![[Pasted image 20260417181347.png]]
From here onwards, the placement should be pretty simple, as its just aligning where the LEDS go, and after that the wiring will be pretty rough as it always is for me I'm assuming.

![[Pasted image 20260417185338.png]]
This is the completed Placement. The hardest thing about this was trying to keep every component reasonably placed so that it would be easy while soldering etc.

Top wirings:
![[Pasted image 20260417185705.png]]
Bottom Wirings: ![[Pasted image 20260417185718.png]]
The Wiring was very tedious to do, as when I tried to do it all on one layer it wasn't working out there was just going to be overlapping. I decided to use the top layer to mostly route the LEDS To the resistors and the CD4017,and the Capacitors to the NE555. I decided to use the back layer to wire the resistors to the CD4017 and the NE555 and any resistors that I was unable to wire on the bottom I just wired on top.

3d render