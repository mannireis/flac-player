---
## Name: 
### Flac Player
## Total time spent:
### 
---

# May 13, 2026: Researched and started making the schematic!

So, I started by researching MCUs and ended up deciding on the ESP32-S3 because it has the processing power, BLE, and Wi-Fi, since my plan is to make a web app and use that for uploading music and changing settings.

Then, I researched more about power. I want to make this really good, so I’m going to use a MAX17048X with a DW01A for battery protection. I worked a bit on the schematic to start making it, and I have the power and USB done.

[img1](https://cdn.hackclub.com/019e22cf-306f-7707-bd91-6919ce4c12cb/image.png)

**Total time spent: 2.5h**


# May 14, 2026: Audio!

I spent a really long time on this because I want it to be really high quality. I was originally going to use the Cirrus Logic CS43131, but it was a bit overkill and a bit complex since I’ve never used a DAC before. Then, I did a bunch of research on which DAC I should use and ended up choosing the TAD5242 and the TPA6132 amp.

After that, I worked on the schematic. It’s already finished, as you can see in the image. It was a bit hard since datasheets are a mess, but I made it work (I think?). Next, I need to decide on the battery charger and then work on the display.

[img2](https://cdn.hackclub.com/019e26cc-dba3-7548-8492-b05fbbf438ce/Screenshot_20260514_150330.png)

**Total time spent: 3.5h**


# May 16, 2026: Battery Charger.

This is a bit of a small journal because it was pretty short, but what I did during this time was add a battery charger. I decided on the MCP73831 because it’s good, and it was hot on LCSC :pf:

I did the schematic. It’s quite simple; I just followed the datasheet. I still need to calculate the PROG resistor once I decide what battery to use.

[img2](https://cdn.hackclub.com/019e3544-f91c-7525-824a-1e7172dda40d/image.png)

**Total time spent: 1.5h**

# May 26, 2026: SD Card and cleaning stuff.

I forgot to journal a few times, so this actually covers a few days of work.

First, I spent about an hour trying to clean up the schematic. It’s pretty clean now.

[before](https://cdn.hackclub.com/019e3544-f91c-7525-824a-1e7172dda40d/image.png)
(before)

[after](https://cdn.hackclub.com/019e6441-ba3d-7dfe-95d2-cebad5ec0622/image.png)
(after)

Then, I spent around 1.4 hours fixing a few things @cyao said were wrong, like some issues in the power section and the display. They should be correct now. I really hope they are.

[Power](https://cdn.hackclub.com/019e6445-0301-7cf0-acbb-1ee00ad5b43b/image.png)
[Display](https://cdn.hackclub.com/019e6445-7c39-7a2a-9da8-4fd0e1351dec/image.png)

After that, I spent another 1.7 hours adding the SD card. I think it’s correct, but I’m not fully sure yet, so I’m going to ask a few people.

[SD Card](https://cdn.hackclub.com/019e6444-b869-7161-a898-baa041f2ace9/image.png)

**Total time spent: 4.2h**

# May 29, 2026: Clean up schematic and change stuff based on feedback.
This is a bit of a shorter one since I mostly changed the capacitors and resistors to make things cleaner. Now it looks better, I think. I was a bit careless with how I organized it before, and it’s improved now.

I also looked into buck-boost converters because I think I might need one. I’m not sure though, so let me know if you think I do.

[Schem now // P1](https://cdn.hackclub.com/019e7375-796a-7bd2-8087-80ab6b6e0862/image.png)
[Schem now // P2](https://cdn.hackclub.com/019e7375-7c94-7d39-a187-ef37a2e61f08/image.png)

As you can see, I’ve changed those horrendous values inside the components.

**Total time spent: 1.4h**

# May 31, 2026: Fix stuff based on feedback.

I feel like I’ve been under-journaling my time, but now I added feedback based on what @cyao said, and I also fixed some stuff Redditors told me to. Now I’m missing a power latch, and then I can move over to the PCB!

I also worked a bit on researching parts. I already decided on these parts:

- SD card holder: Hirose DM3AT
- USB-C: HCTL HC TYPE C 16P 01A
- 0603 capacitors and resistors

The hardest part of this was fixing the stuff because I’m really dumb :pensive-wobble:

[Fixed schematic](https://cdn.hackclub.com/019e7f13-158c-77f1-a420-a455153c5a0e/image.png)

**Total time spent: 2.5h**

# May 31, 2026: Make a Press ON - Hold OFF latching circuit

This was really cool.  
I did a lot of research because this was a bit too complex, but I’m happy with how it ended and I think it’s working.

This was really hard, but I learned quite a lot from it. I also originally went with different latch systems, but I ended up on this one and it’s really good :3

## Latching Circuit

[Latching Circuit](https://cdn.hackclub.com/019e7f13-158c-77f1-a420-a455153c5a0e/image.png)

Thank you [Mosaic Industries](http://www.mosaic-industries.com/embedded-systems/microcontroller-projects/electronic-circuits/push-button-switch-turn-on/latching-toggle-power-switch)! You saved me <3

**Total time spent: 1.2h**

# June 10 to June 11, 2026: Restart making everything!

- Remade all off the MP3 player because the old schematic was really messy and pretty bad.

[Full Schematic](https://user-cdn.hackclub-assets.com/019eb7c4-259b-7b8a-ac0a-f55e3072166a/image.png)

- Decide to use a STM32 instead of the ESP32 because I think power efficiency is more inportant than wireless since I won't use wireless since wired headphones are better I'm using the STM32H753.

[STM32](https://user-cdn.hackclub-assets.com/019eb7c4-2339-79e8-b939-5ae69eb19fce/image.png)
[Decoupling Capacitors](https://user-cdn.hackclub-assets.com/019eb7c4-2110-7cd0-9484-cc088802a43f/image.png)

- Remake the DAC and AMP I decided on using the same as I was before But this time I actually made it good and clean:

[DAC and AMP](https://user-cdn.hackclub-assets.com/019eb7c4-1d44-7f8c-a4b1-e0296b198cbc/image.png)

- Add the LDO decided on the LDO from mitxela since I was seeing the projects he made and in one of their projects he used the one I'm using and said it was good so I researched it and it seemed good for what I needed.

[Power thingys](https://user-cdn.hackclub-assets.com/019eb7c4-0db2-74eb-aee0-09cdac440e2b/image.png)

- Added the USB-C and ESD Protection using the ST guidlines for the STM32's.

[USB](https://user-cdn.hackclub-assets.com/019eb7c4-1b1b-78c5-99b6-940c993fcaf2/image.png)


The hardest part of this was researching what chips and IC's to use but this helped me get started for more projects since now I know many more IC's and Chips that I can use in other projects!

(I hope this journal is good)
**Total time spent: 4.2h**

# June 16, 2026: Add a 6 axis accelerometer + research and thinking.

I added a accelerometer yay. I searched a bit (very little) on what accelerometer to use and decided on the MPU-6050 since it has a gyroscope and a accelerometer built in and is pretty useful then I read the datasheet to see what decoupling capacitors to use since it had an application segment and then I added the capacitors.

[Finished MPU-6050](https://cdn.hackclub.com/019ed05a-5f1c-7c71-a7e2-e0fa20b77c47/image.png)

I also did a bit of research and thinking on how to make the shape and stuff but I'm still not sure how I want it to be.

**Total time spent: 1.3h**
