---
title: Common Connectors
summary: Properties of common types of connectors.
authors: Jon Harper
date: 2022-12-02
---

## Basic Considerations

- Electrical properties
    - Ampacity
    - Resistance
    - Temperature rise & operating temperature
- Physical properties
    - Connection/disconnection force
    - Locking/latching method
    - Uses (board, inline, panel mount)
    - Pin sizes/compatible wire gauges
    - Overall size
- Other Considerations
    - Cost
    - Availability

<!-- 
### Title

Common uses:

**Summary**

- Pitch: 
- Max Current Rating: 
- Wire Gauges: 
- Panel Mount: 
- Available Positions:
    - Single Row: 
    - Dual Row: 
- Notes:

**Links**

[:material-order-alphabetical-ascending: Datasheet][link]{ .md-button }

[Digikey][link]{ .md-button } 
-->

## Pin and Socket Connectors

### JST PH

6-position PH connectors are common on NEMA 17 stepper motors.

**Summary**

- Pitch: 2.0mm
- Current Rating: 2.0A @ 24 awg
- Wire Gauges: 24 - 32 awg
- Applications: board only
- Available Positions:
    - Single Row: 2-
    - Dual Row: 
- Common uses: These have wide application as a compact connector for PCBs when space is at a premium.
- Notes: The small pitch can make these difficult to crimp.

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_ph]{ .md-button }

[:simple-amazon: Amazon 2-6 Position Kit][az_jst_ph]{ .md-button } 

### JST RCY

These are sometimes called JST SYP, though JST lists the product as RCY series. RCY connectors are used in 3D printing to extend wire pairs (or make them disconnectable) as an inline alternative to XH or PH connectors. RCY are also physically smaller in size than SM.

**Summary**

- Pitch: 2.5mm
- Max Current Rating: 3.0A @ 22 awg (2.0A @ 24 awg)
- Wire Gauges: 22-28 awg
- Applications: inline only
- Available Positions: 2
- Common uses: remote-controlled cars and airplanes.
- Notes: usually red or black. Sometimes found in 2.54mm pitch.

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_rcy]{ .md-button }

[:simple-amazon: Amazon Kit][az_jst_rcy]{ .md-button } 

### JST SM

Although these connectors are only for wire-to-wire connections, they are easy to crimp and can be panel mounted. A downside to SM connectors is the size of the shell.

**Summary**

- Pitch: 2.5mm
- Max Current Rating: 3.0A @ 22 awg
- Wire Gauges: 22 - 28 awg
- Applications: inline, panel mount
- Available Positions:
    - Single Row: 2-12 position
    - Dual Row: 18 position
- Common uses: RGB LED light strips
- Notes: found in a wide variety of colors, most commonly white or ivory.

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_sm]{ .md-button }

[:simple-amazon: Amazon 2-5 Position Kit][az_jst_sm_small]{ .md-button } 

[:simple-amazon: Amazon 2-9 Position Kit][az_jst_sm_full]{ .md-button } 

### JST XH 2.5

Common uses: most common connector for 3D printers (e.g., most boards-side connectors & limit switches)

**Summary**

- Pitch: 2.5mm
- Current Rating: 3.0A @ 22 awg
- Wire Gauges: 22 - 30 awg
- Applications: board only
- Available Positions:
    - Single Row: 2-16 position & 20 position

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_xh]{ .md-button }

[:simple-amazon: Amazon 2-5 Position Kit][az_jst_xh]{ .md-button } 

### Molex Micro Fit 3.0

Perfect but for the price.

Common uses: 3D printers, particularly for high temperature and high-current applications.

**Summary**

- Pitch: 3.0mm
- Max Current Rating: up to 8.5A
- Wire Gauges: 18 - 24, 26 - 30 awg (two pin sizes)
- Applications: board, inline, panel mount
- Available Positions:
    - Single Row: 2-11 position
    - Dual Row: 2-24 position

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_molex_mf3]{ .md-button }

[:simple-digikeyelectronics: Digikey][dk_molex_mf3]{ .md-button } 

### Molex Mini Fit Jr

Common uses: ATX connectors in computers

**Summary**

- Pitch: 4.2mm
- Max Current Rating: 9A
- Wire Gauges: 18 - 24, 24 - 28 awg (two pin sizes)
- Applications: board, inline, panel mount
- Available Positions:
    - Single Row: 2-6 position
    - Dual Row: 2-24 position

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_molex_mfjr]{ .md-button }

[:simple-digikeyelectronics: Digikey][dk_molex_mfjr]{ .md-button } 

## Closed Barrel Connectors

These connectors are often used in automotive and marine applications. Their current-carrying capacity is dependant on the size of the surface contact area. The larger the mating contact, the more current that can be safely carried.

Avoid uninsulated terminals; fully insulated marine terminals are best for 3D printing applications.

Generally speaking, closed barrel connectors do not use pins and thus are single-conductor connections.

### Common Examples

!!! todo "TODO: Expand"

- Ring
- Fork
- Spade
- Bullet
- Ferrules

## Other Connectors

### Harwin M20 / "DuPont"

**FAQ Explanations**

1. [Why are these called DuPont connectors?][dupont_name]
2. [Why are these so hard to crimp?][dupont_crimp]

**Summary**

- Pitch: 2.54mm
- Max Current Rating: 3A
- Wire Gauges: 22-30 awg
- Panel Mount: No
- Available Positions:
    - Single Row: 2-12 position
    - Dual Row: 4-24 position

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_harwin_m20]{ .md-button }

[:simple-amazon: Amazon Kit][az_harwin_m20]{ .md-button } 


### Aviation

!!! todo "TODO: Expand"
### DSUB

!!! todo "TODO: Expand"
### IDC Ribbon

IDC stands for Insulation-displacement contact. These are meant for low-voltage, low-current applications, particularly digital signaling. They are most frequently found on LCD 3D printer displays.

!!! todo "TODO: Expand"

[tips]:             https://falconerelectronics.com/wire-harness-manufacturing/

[ds_molex_mf3]:     ../assets/datasheets/molex_mf3.pdf
[ds_molex_mfjr]:    ../assets/datasheets/molex_mfjr.pdf
[ds_jst_ph]:        ../assets/datasheets/jst_ph.pdf
[ds_jst_sm]:        ../assets/datasheets/jst_sm.pdf
[ds_jst_xh]:        ../assets/datasheets/jst_xh.pdf
[ds_jst_rcy]:       ../assets/datasheets/jst_rcy.pdf
[ds_harwin_m20]:    ../assets//datasheets/harwin_m20.pdf
