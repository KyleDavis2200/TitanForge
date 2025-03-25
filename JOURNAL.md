Made by: @KyleDavis2200
Repository link: https://github.com/KyleDavis2200/TitanForge
Total hours so far: 29

- [x] I have a 3D printer or will be getting one before March 21st

### 3/23/2025
15 Hours

# Researched components:

I started off by establishing my goals for this project and created an ordered list of features that I would like to have, but would be willing to cut to save price. My main goal was to create a printer capable of printing filled Nylons and quickly printing TPU, the two most common filaments in combat robotics, my main hobby. TPU is a flexible filament that, for 99% of uses outside of combat robotics, is moreorless indestructable. The key to printing TPU is a direct drive extruder, which made that one of my necessities. Nylon is generally a lot more fragile than TPU, however its heat resistance makes it ideal for smooth pulleys that act as clutches in the robots' weapon systems. Some of the features that I wanted, but was willing to forgo, were CoreXY kinematics, Klipper, ABL, 300mm width, dual material, touch screen, and 250mm depth. Due to the budget constraints, I quickly gave up most of these features, and instead focused on getting a functional printer within the budget.

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/research.png" width="550">

I began my parts research by looking at off the shelf toolheads that featured direct drive extruders, and eventually settled on the Neptune 4 Max's toolhead. However, since there was no CAD model and buying an off the shelf toolhead felt out of the spirit of Infil, I opted to design my own toolhead. Even on my Elegoo Neptune 2, by no means a fancy or fast printer, I find myself flow rate limited (particularly on larger nozzles) due to the plastic not being able to melt in time. I wanted a hotend that avoided the limited meltzone of the Mk8 nozzle. This led to me switching to a Volcano hotend, and I paired it with an HGX Lite extruder.

# Began Bill of Materials:

As I picked parts out and added them to the CAD model, I added them to by BOM. At this point my list was very imcomplete, but so was my printer design. 

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day1%20bom.png" width="550">

# Began CAD Model:

I had initially started my CAD model based off of 3030 extrusion, as I expected 2020 extrusion to not be strong enough for a printer of this scale. However, when I looked at the Voron 2.4 for inspiration, I found that it got away with using 2020 extrusions even at the 350mm scale. This led to me switching to 2020 rails to save a little bit of cost, as I knew I would be cutting it close on my budget for this project. Taking inspiration from the Voron would turn into a running theme throughout this project, as I moreorless ended up trying to make a budget Voron 2.4. Another instance of this is the bed mounting system. I knew that a triple Z lead screw system like the Voron Trident uses would be too expensive and complex for my project, and I wanted to avoid using bed springs, which led to me using a fixed bed and a PCB klicky probe to run automatic bed leveling on the flying gantry. This ended up being the cheapest and simplest path, with the added advantage of automatic bed leveling, which was something I wanted but a very low priority. 

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day%201%20cad.png" width="550">

### 3/24/2025
14 Hours

Day 2 started off well, with me getting most of the printer's motion system inserted into the model in the first 5 hours. I was able to find cheap sources for all of the belts and pulleys, and everything fit more or less as I wanted it to. After I got the motion system modelled, all that was left to do was to sort out my electronics, model the mounting for all of the components, and insert the part cooling fan and model the ducts. I started off researching boards, and settled on the BTT Manta M5P because it provided a seperate driver for each stepper motor and came with a cheap and easy way to integrate Klipper into the printer without needing to buy a Raspberry Pi, which can be expensive. After this, I began researching power supplies, which is when I realized I made a mistake earlier. The bed I had selected would draw about 250W by itself, meaning I would need approximately a 400W power supply for the rest of the printer. Many recent 3D printers avoid this by using a 110V bed and connecting it straight to the power grid, bypassing the power supply. However, I ended up choosing to stick with the 24V bed because it allowed me to avoid directly connecting to 110V mains, which could be a safety hazard if done incorrectly, and it allowed me to avoid a major redesign.

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day%202%20cad%201.png" width="550">

After this, I began working on mounting the rest of the components. I had first modeled out the general frame and motion system, which allowed me to make sure that I had the right size of everything. Now, I needed to create 3D printed mounting brackets for each of the rails/extrusions. These would be printed out of PLA initially, and would later be swapped to Nylon or ABS if I enclosed the printer. At this point, I had temporarily given up on enclosing the printer, as the mounting brackets intersected where I had planned to put the chamber walls. I will still be able to enclose the printer in the future by mounting the chamber walls into 3D printed brackets mounted to the frame, but for the sake of time I had chosen to forgo that for now. One of the more questionable choices in this build is the mounting of the idler pulleys. Instead of using a screw or a shaft to mount the pulleys, I integrated the shaft into the 3D printed mounting bracket. To save time I had mirrored the mounting brackets across, which led to the upper pulley being cantilevered a decent distance on a 5mm PLA shaft. I plan to either reduce the cantilever effect by creating a tapered shaft for the upper pulley or by replacing the PLA shaft with a screw, but for now, since the deadline is approaching, I have chosen to keep the PLA shaft. After the mounting brackets were all added, I inserted the part cooling fan CAD model. I did not have time to mount the fan or make the fan ducts today, but I was able to figure out what I would do with my PCB. Like many things on this printer, I took inspiration from the Voron 2.4 with the LEDs around the nozzle on the StealthChanger. I plan to make a simple PCB to mount LEDs near my nozzle to light it up. This will be difficult to squeeze in as I will have cooling ducts and a Z probe mount nearby (and obviously the hotend as well), but I think a custom PCB will give me the best chance of fitting it in. 

As it sits writing this, the printer is currently 95% done, just needing the part cooling ducts, fan mount, and LED board added. My BOM is also about 90% done, still missing the LED board and most of the screws and heatset inserts, along with a few larger T slot nuts. 

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day%202%20cad%202.png" width="550">

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day%202%20bom.png" width="550">

This CAD model shows a few glitches I ran into in Solidworks. I have the brackets set to mirror across the frame, yet one of them isn't mirroring properly. They are all set to the same mirror setting, but it isn't working properly even after rebuilding.  
