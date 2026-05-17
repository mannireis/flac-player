---
## Name: 
### Flac Player
---
---
Template:

# May 4th, 2026: Got the screen to work!

[your actual journal entry!]

[A picture or two of what you did!]

**Total time spent: 2h**
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

**Total time spent: 0.5h**
