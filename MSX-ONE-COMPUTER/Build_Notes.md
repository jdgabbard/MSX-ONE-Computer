#MSX-ONE BUILD NOTES

I am still working on a BOM for the MSX-ONE Mainboard. However, in the meantime here are some items builders should note.

PCB version P1.1 in the Gerbs folder is the last tested version. However, this version has a small flaw. U9, the MC34063a buck converter IC used for the -12v rail needs to have pins 7 & 8 solder-jumpered together during the build process. Without this, the -12v rail will not be present, and the MC34063a will overheat and fail. In addition to this, I would suggest adding a 1-Watt 1K or 2K resistor between -12v and GND on the underside of the board. This helps to stabilize the -12v rail, resulting in less voltage ripple, as the MC34063a skips oscillation when -12v is reached. Adding this simple resistor helps prevent the skipped oscillation, making the voltage level more stable. This has been changed on the v1.0 PCB, though that PCB has not been tested at this time.

###BOM
Name        | Description              | Part#                       | DigiKey                           | Mouser                             | Notes
------------|--------------------------|-----------------------------|-----------------------------------|------------------------------------|---------------------------
U1, U12	    | 74HCT74	                 | SN74HCT74N                  | 296-1625-5-ND                     | 595-SN74HCT74N                     |
U2	        | Z80 Microprocessor       |                             |                                   |                                    | *Ebay or 2nd Hand Market
U3          | MAX701 or ATTiny85       | MAX701EPA+ or ATTINY85-20PU | MAX701EPA+-ND or ATTINY85-20PU-ND | 700-MAX701EPA or 556-ATTINY85-20PU | *Use ATTINY with provided code, it has more drive/sink current
U4, U24     | 74HCT32                  | SN74HCT32N                  | 296-1615-5-ND                     | 595-SN74HCT32N                     | 
U5          | 74LS07                   | SN74LS07N                   | 296-14878-5-ND                    | 595-SN74LS07N                      | 
U6          | TMS9118 VDP              |                             |                                   |                                    | *Ebay or 2nd Hand Market
U7, U8      | TMS4416 DRAM             |                             |                                   |                                    | *Ebay or 2nd Hand Market
U9          | MC34063A                 | MC34063ABN                  | 497-7412-5-ND                     | 511-MC34063ABN                     | 
U11         | LM2596S-5.0              | LM2596S-5.0/NOPB            | LM2596S-5.0/NOPB-ND               | 926-LM2596S-5.0/NOPB               | 
U14         | AT28C256 EEPROM          | AT28C256-15PU               | AT28C256-15PU                     | 556-AT28C25615PU                   | *Cheaper on Ebay or 2nd Hand
U15         | HM628128 SRAM            | SST39SF040-70-4C-PHE        | SST39SF040-70-4C-PHE-ND           | 804-39SF0407CPHE                   | *Ebay, but can use 39SF040/020
U16         | 74HCT02                  | SN74HCT02N                  | 296-8380-5-ND                     | 595-SN74HCT02N                     | 
U17, U19    | 74HCT157                 | SN74HCT157N                 | SN74HCT157N                       | 595-SN74HCT157N                    | 
U18         | YM2149 PSG               |  YM2149 or AY-3-8910        |                                   |                                    | *Ebay or 2nd Hand Market
U21         | 74HCT00                  | SN74HCT00N                  | 296-1603-5-ND                     | 595-SN74HCT00N                     | 
U22         | 74HCT139                 | SN74HCT139N                 | 296-8390-5-ND                     | 595-SN74HCT139N                    | 
U23         | 74HCT153                 | CD74HCT153E                 | 296-2094-5-ND                     | 595-CD74HCT153E                    | 
U26         | 82C55A PPI               | i82C55A or CP82C55A-5Z      | CP82C55A-5Z-ND                    |968-CP82C55A-5Z                     | *Cheaper on Ebay or 2nd Hand
U27         | 74HCT08                  | SN74HCT08N                  | 296-1606-5-ND                     | 595-SN74HCT08N                     | 
U28         | 74HCT138                 | SN74HCT138N                 | 296-1608-5-ND                     | 595-SN74HCT138N                    | 
L1          | 1uH Ferrite Bead         |                             |                                   |                                    | 
L2, L5      | 88uH Inductor            |                             |                                   |                                    | 
Y1          | 10.738635 MHz Crystal    | MP107-E                     | CTX1443-ND                        | 774-MP107-E                        | 
D1          | 3mm Red LED              | 732-5006-ND                 | 710-151031SS06000                 | 151031SS06000                      | 
D2          | 2W10 Bridge Rectifier    | 2W10                        | 4786-2W10GCT-ND                   | 625-2W10G-E4                       | 
D3          | 1N5819                   | 1N5819                      | 497-6610-1-ND                     | 511-1N5819                         | 
D4,D5,D6,D7 | 1N4148                   | 1N4148                      | 1N4148FS-ND                       | 512-1N4148                         | 
D9          | 1N5822                   | 1N5822                      | 497-14742-1-ND                    | 511-1N5822-TR                      | 
RN1, RN2    | 4.7kohm Resistor Array   | 4609X-101-472LF             | 4609X-101-472LF-ND                | 652-4609X-1LF-4.7K                 | 
R6          | 0.24ohm Resistor         | RR01JR24TB                  | A138235TB-ND                      | 279-RR01JR24TB                     | 
R1          | 10Kohm Resistor          |                             |                                   |                                    | 
R8          | 1Kohm Resistor           |                             |                                   |                                    | 
R7          | 8.2K Resistor            |                             |                                   |                                    | 
C14,C16,C17 | 470uF Electrol Capacitor | UVR1E471MPD                 | 493-1064-ND                       | 647-UVR1E471MPD                    | 
Elec Caps   | 10uF Electroly Capacitor | ECE-A1EKS100I               | 10-ECE-A1EKS100ICT-ND             | 667-ECE-A1EKS100I                  | C20,C21,C22,C23,C37,C38,C39
C5, C6      | 27pF Ceramic Capacitor   | RCE5C2A270J0M1H03A          | 490-7451-1-ND                     | 81-RCE5C2A270J0M1H3A               | 
Bypass Caps | 100nF Ceramic Capacitor  | FK28X7R1H104KN000           | 445-FK28X7R1H104KN000-ND          | 810-FK28X7R1H104K                  | C1,C3,C4,C7,C8,C9,C10,C11,C18,C19,C24,C25,C26,C27,C27*,C28,C29,C30,C31,C32,C33,C34,C35,C36
C12         | 1.5nF Ceramic Capacitor  | FG28X7R1H152KNT06           | 445-173589-1-ND                   | 810-FG28X7R1H152KNT6               | 
SLOT1,SLOT2 | 50pin Card Edge          | 5530843-5                   | A31718-ND                         | 571-5530843-5                      | 
Gamepad1/2  | DB9 Male                 | L717SDE09P1ACH3R            | L717SDE09P1ACH3R-ND               | 523-L717SDE09P1ACH3R               | 
J2          | Yellow RCA               | RCJ-014                     | CP-1403-ND                        | 490-RCJ-014                        | 
J3          | White RCA                | RCJ-013                     | CP-1402-ND                        | 490-RCJ-013                        | 
J1          | DC Jack                  | KLDX-0202-A                 | 2092-KLDX-0202-A-ND               | 806-KLDX-0202-A                    | 
J9          | IDC 2x8P                 | 61201621621                 | 732-2095-ND                       | 710-61201621621                    | 
SW1         |                          |                             |                                   |                                    | 
PWR_SW      |                          |                             |                                   |                                    | 

