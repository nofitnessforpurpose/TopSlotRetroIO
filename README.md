# TopSlotRetroIO
PSION Organiser II - Top Slot Retro Component 8 Bit I/O

This repository holds files supporting creation of a Top Slot 8 bit Input Ouput (I/O) adapter for the Psion Organiser 2 series of devices.
  
<div align="center">
  <div style="display: flex; align-items: flex-start;">
    
  <img src="https://github.com/nofitnessforpurpose/TopSlotRetroIO/blob/main/images/TSRIO-01.png?raw=true" width="400px" alt="PSION Organiser II Top Slot Retro IO Case. Image copyright (c) 01 November 2024 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

[![Organiser](https://img.shields.io/badge/gadget-Organiser_II-blueviolet.svg?%3D&style=flat-square)]([https://en.wikipedia.org/wiki/Psion_Organiser])
[![GitHub License](https://img.shields.io/github/license/nofitnessforpurpose/TopSlotRetroIO?style=flat-square)](https://github.com/nofitnessforpurpose/TopSlotRetroIO/blob/main/LICENSE) 
[![Maintenance](https://img.shields.io/badge/maintained%3F-yes-green.svg?style=flat-square)](https://github.com/nofitnessforpurpose/TopSlotDataPack/graphs/commit-activity)
![GitHub repo size](https://img.shields.io/github/repo-size/nofitnessforpurpose/TopSlotRetroIO?style=flat-square)
[![Static Badge](https://img.shields.io/badge/format-STEP%20Solid%20Model-blue?style=flat-square)](https://en.wikipedia.org/wiki/ISO_10303)
[![Static Badge](https://img.shields.io/badge/format-GERBER%20PCB-blue?style=flat-square)](https://en.wikipedia.org/wiki/Gerber_format)
<br>  
  All the files are required.  <br>
  The default repository format for 3D files is STEP (<a target="_blank" rel="noopener noreferrer" href="https://en.wikipedia.org/wiki/ISO_10303"> ISO 10303</a> ) due to its high fidelity.  { STL files are surface geometry as opposed to solid model representations, often containing export processing artifacts }. 
<br>  
  The default repository format for PCB files is <a targer="_blank" rel="noopener noreferrer" href="https://en.wikipedia.org/wiki/Gerber_format">GERBER</a> .
<br>

<br>  
<a target="_blank" rel="noopener noreferrer" href="https://www.freecad.org/" > FreeCAD </a> may prove suitable for viewing, handling and, if desired modifying STEP files.
<br>
<a target="_blank" rel="noopener noreferrer" href="https://www.kicad.org/" >KiCad </a> may prove suitable for viewing GERBER files.
<br>

## Use Case
General purpose 5 Volt, low current hardware interface.  

## Hardware Design
The hardware is largely compatible with a previously published project, <a target="_blank" rel="noopener noreferrer" href="https://www.strickling.net/orginter.htm" > here </a>, which I recommend reading. This arises as there are limited combinations of hardware port management via the slots. Though differences exist in the expression of the design presented here, principally this embodiment presents a single 8 bit output port. Never the less this embodiment exhibits a good degree of compatability, arising from the design complying with reference slot hardware implementation and reference designs.  

## Software Attribution Credit  
The <a target="_blank" rel="noopener noreferrer" href="https://www.strickling.net/orginter.htm" > author</a> has kindly granted permission for a copy of his software to be reproduced here and forks of the software under an MIT licence (November 2024). I would like to thank the author <a target="_blank" rel="noopener noreferrer" href="https://www.strickling.net/orginter.htm" >Dr. Wolfgang Strickling</a> for permission, as the software is documented and tested. Copyright to <a target="_blank" rel="noopener noreferrer" href="https://github.com/nofitnessforpurpose/TopSlotRetroIO/tree/main/Reference%20Software">that software</a> remains with the author.  

## Discussion
Whilst it would be desirable to have code available with the hardware, as presented for example via the classic Serial Comms. interface. The additional space claim and complexity within the desired space claim, would demand surface mount technology restricting potential implementation. A physically compatible surface mount variant is planned with supporting on board code storage.  

Fabrication of the Retro I/O implementation is more straight forward. It may be found desirable to utilise IC sockets, though space claim should be accounted for when considering compatability with any enclosure.

- TI (Texas Instruments) devices were selected for the integrated circuits.  
- The board is implemented as a 4 layer variant to obtain a ground plane for improved EMC performance.  
- I/O devices, in particular the output channel can consume considerable current. This will discharge any battery rapidly where high current drains are employed. Facility exists to provide for an external power source via the Vb connection and associated power diode.  
- A compatible hardware expansion board is available to permit connection of additional hardware. This board supports interconnection headers to the I/O board for reliable interconnection.  
- The pitch of all connectors is compatible with breadboard pitch. Incorrect connection WILL permenantly degrade connected elements!  

<div align="center">
  <div style="display: flex; align-items: flex-start;">
    
  <img src="https://github.com/nofitnessforpurpose/TopSlotRetroIO/blob/main/images/TSRIO-03.jpg?raw=true" width="400px" alt="PSION Organiser II Top Slot Retro PCBs. Image copyright (c) 01 November 2024 nofitnessforpurpose All Rights Reserved">
  </div>
</div>

## Considerations
The 3D model makes no accomodation for manufacturing tolerances, process or material - see Notes below.  
The PCB is currently beta and has been tested, it remains your responsiblity to asses suitability!  
Assembly of PCB and case has been tested.  
Connection or use of any material presented here could result in irreversible damage to your equipment. No responsability can be accepted for any degredation, how so ever arising. Compatability, suitablity or other are entirely your responsibility as is any effects so arising as a result ! See also notes below.

Minimum implementation comprises:  
- 4 layer PCB
- CD4011UBE
- 1N4148 Diode
- 47k Ohm resistor
- 2 x 8 way Right angle header (~8 mm engagement length)  
- Input - SN74HC244N Octal Buffer and Pull down resistor network (RN3H 10k Ohm)  
  or  
- Output - SN74HC374AN Octal D-Type Flip Flop  
The 47k Ohm pull down resistor network (RN1A) for the data lines and decoupling capacitor are recomended

## Please note:  
All information is For Indication only.
No association, affiliation, recommendation, suitability, fitness for purpose should be assumed or is implied.
Registered trademarks are owned by their respective registrants.
