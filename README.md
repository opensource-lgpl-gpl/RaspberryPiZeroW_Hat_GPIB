# RaspberryPiZeroW_Hat_GPIB
## A $25.66 Dongle 
### Alternative to GPIB National Instrument's USB-GPIB-HS (MSRP: $1,476) and Prologix GPIB-LAN (MSRP: $189.99): 
This is used to standardize old Lab Instruments (Ammeters and Voltage Sources) like the Kiethley Picoammeter and Voltage Source so that a computer can connect wired via USB-A or wirelessly via bluetooth to a Raspberry Pi Zero with Wifi capabilities. 

This contraption RaspberryPiZeroW_Hat_GPIB can deliver results wirelessly via bluetooth or wired via USB-A (Plug) to USB (Plug) so that results can be delivered wirelessly in order to support work-from-home pandemic initiatives. 

This allows the older lab instruments to have the same capabilities as newer more expensive lab instruments that can cost thousands of dollars. 

This side-project used free and open-source tools to show: 
- Free software like KiCAD can completely replace Altium and intra-convertibility between Altium-to-KiCAD. 
- Free software auto-routing tool FreeRoute can replace most of manual PCB design routing. 
- Free software FreeCAD can completely replace SolidWorks, AutoCAD, et cetera (all costly "CAD" software). 

## Why was this created? 
During my time at NASA, I was tasked with getting a Prologix-LAN (MSRP $189.99) to talk to an old lab instrument: 

I was having a hard time connecting to a Prologix GPIB-Lan that was talking to a Kiethley instrument because when I sent the Prologix controller a command to go into "recieve"/"listen" mode, the logic was inverted; what resulted was the Prologix controller started to spew out a lot of data. Then when I wanted the Prologix controller to give me data or in other words, to "talk," the Prologix controller was silenced and went into "recieve"/"listen" mode. 

So I said to myself: "Why would I want to use a GPIB controller that does the exact opposite of what you want it to? Wouldn't that unpredictability potentially compromise valuable results someday when something invariably goes wrong, and you are trying to look for a root-cause?"

To me, this was not rocket science; I scoured the internet and found Thomas Klima's work on Raspberry Pi Model 3's USB-GPIB. 

Link to thesis paper (I studied German at University of Freie-Universitat, Berlin, Germany in 2013): http://elektronomikon.org//Bakkarbeit%20RasPi-GPIB%20Thomas%20Klima.pdf

I worked on this project about 6-8 hours total; most of the time was spent on tool setup and getting used to KiCAD, FreeCAD, and FreeRoute on a Mac machine.

This $25 dongle RaspberryPiZeroW_Hat_GPIB would be placed on every old lab instrument to modernize/"upgrade" it. 

## Bill of Materials from Digikey and OshPark and Raspberry Pi 
### (Total Cost of Materials)
| Part                               | Unit price  | Quantity | Digikey Part No.    | Price    |
| ---------------------------------- | ----------- | -------- | ------------------- | -------- |
| IC TRANSCEIVER HALF 8/8 20DIP      | 3.69        | 1        | SN75160BN           | $3.69    |
| IC TRANSCEIVER HALF 8/8 20SOIC     | 2.74        | 1        | SN75161BDWR         | $2.74    |
| RES ARRAY 5 RES 3.3K OHM 10SIP     | 0.63        | 2        | 4610X-102-332LF     | $1.26    |
| RES ARRAY 9 RES 6.8K OHM 10SIP     | 0.63        | 2        | 4610X-101-682LF     | $1.26    |
| CAP CER 0805 220NF 100V X7R 5%     | 0.31        | 1        | C0805C224J1REC7800  | $0.31    |
| RES 100 OHM 1% 1/4W 0805           | 0.07        | 20       | RNCP0805FTD100R     | $1.40    |
| Oshpark PCB Fab                    | $5.00       | 1        | N/A                 | $5.00    |
| Raspberry Pi   Zero W              | $10.00      | 1        | N/A                 | $10.00   |
|                                    |             |          | **Total:**          | $25.66   |

## PCB design and schematics. 
### Tool used: KiCAD
#### Cost of Tool used: Free, Open-source
KiCAD is a free alternative to more expensive software suites like Altium. 
![Screen Shot 2022-03-06 at 1 16 15 PM](https://user-images.githubusercontent.com/33333047/156943624-be5df4e3-5151-464e-b0a2-2ec082021ff7.png)

## FreeRouting Tool to auto-route the PCB
### Tool used: FreeRouting
#### Cost of Tool used: Free, Open-source
I used the open-source and free tool called FreeRouting (https://freerouting.org) to route the PCB and ensure that a mounting bracket would fit. 

The PCB was designed using Free Routing to prevent cross-talk of wires as well as support a FreeCAD-designed mounting bracket. 

What is shown is the schematics taken from KiCAD. 

![Screen Shot 2022-03-06 at 1 11 00 PM](https://user-images.githubusercontent.com/33333047/156940672-710920b7-4bf7-457b-bb29-0b7c213f05d1.png)

## Right Angle Mounting Bracket between the Raspberry Pi Zero W and GPIB Rpi Hat. 
### Tool used: FreeCAD
#### Cost of Tool used: Free, Open-source
This is the mounting bracket that was to be 3D printed using my personal 3D Printer from Monoprice. 
![image](https://user-images.githubusercontent.com/33333047/156943819-1d9079e8-981c-4ec2-b3c8-1b3783266e13.png)




