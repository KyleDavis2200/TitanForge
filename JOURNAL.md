Made by: @KyleDavis2200
Repository link: https://github.com/KyleDavis2200/TitanForge
Total hours so far: 15

- [x] I have a 3D printer or will be getting one before March 21st

### 3/23/2025
15 Hours
Researched components:

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/research.png" width="550">

Began Bill of Materials:

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day1%20bom.png" width="550">

Began CAD Model:

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day%201%20cad.png" width="550">

### 3/24/2025

Day 2 started off well, with me getting most of the printer's motion system inserted into the model in the first 5 hours. I was able to find cheap sources for all of the belts and pulleys, and everything fit more or less as I wanted it to. After I got the motion system modelled, all that was left to do was to sort out my electronics, model the mounting for all of the components, and insert the part cooling fan and model the ducts. I started off researching boards, and settled on the BTT Manta M5P because it provided a seperate driver for each stepper motor and came with a cheap and easy way to integrate Klipper into the printer without needing to buy a Raspberry Pi, which can be expensive. After this, I began researching power supplies, which is when I realized I made a mistake earlier. The bed I had selected would draw about 250W by itself, meaning I would need approximately a 400W power supply for the rest of the printer. Many recent 3D printers avoid this by using a 110V bed and connecting it straight to the power grid, bypassing the power supply. However, I ended up choosing to stick with the 24V bed because it allowed me to avoid directly connecting to 110V mains, which could be a safety hazard if done incorrectly, and it allowed me to avoid a major redesign.

<img src="https://github.com/KyleDavis2200/TitanForge/blob/main/day%202%20cad%201.png" width="550">
