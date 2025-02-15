# MSX-ONE Computer

A small, easy to build MSX1 compatible computer.<br>

***See Build Notes file for special instructions!***

Designed as a cheap, and easy to build, MSX1 computer for the US Vintage Computer enthusiast.

![MSXONE]([https://github.com/jdgabbard/RD-10-Docking-Station/blob/59d0eb6cd6155eeae0b91679d095db8af9a2d37a/Renders/RD10.jpg](https://github.com/jdgabbard/MSX-ONE-Computer/blob/6c76e4c953c62954539ab062a4356bdd8ebb6146/Photos/Render.JPG))

Features include:<br><br>
-Small Footprint:
     -Mainboard size: 200mm x 150mm
     -Keyboard size: 200mm x 95mm
-Power-On Reset Supervisor Circuit providing automatic 200ms Reset.
-Flexible power input handles +12v DC to +12v AC power supplies.<br>
-Implements +12v/-12v rails, so Audio Cartridges work correctly.<br>
-2x Sega Gamepad compatible ports, since finding MSX controllers in the US is all but impossible.<br>
-TMS9118 Low Cost alternative does away with numerous DRAM chips, or finicky SRAM circuits, using just two 4bit DRAMs.<br>
-Two Primary Slots available to the user.<br>
-Construction consisting of off the shelf TTL logic, without the need for any programable logic, SPLDs or FPGAs to worry about programming.<br>
-A small form factor, consisting of a PCB approximately the same size as a ZX Spectrum: 200mm x 150mm<br>
-A stackable keyboard (Omega Home Computer Compatible) using cheap tactile switches with an optional cover for aesthetics.<br><br>


#Inspiration

This computer was heavily inspired by, and borrowing from, both Sergey Kiselev's Omega Home Computer, and the JFF Computer (https://github.com/konkotgit/JFF), as well as the Casio MX-10.<br><br>

I desired a MSX without all the fluff, but with the modularity that the Omega Computer affords.  I wanted a simplified circuit, but with nice options such as power regulation, options for a mechanical power switch, and +12v/-12v rails.  The MSX-ONE gives the casual MSX user just the basics to have a functional yet flexible machine for playing MSX1 games.  And it does this without the need for programmable logic.  The design uses all off the shelf TTL compatible parts, which are still in current production.<br><br>

#Specifications:
-TMS9118 VDP with 16k DRAM (2x4bit DRAMS)
-32k EEPROM in SLOT0 (BIOS with International Keyboard, Mapper Initializer & BASIC 1.0)
-64K SRAM in SLOT3
-Standard PSG
-International Keyboard
-No Printer Port
-No Cassette Interface
-No Disk Drive
-No Fluff
