---
title: Connectors Reference
summary: Properties of common types of connectors.
authors: Jon Harper
date: 2022-12-02
---

This page is a list of connectors. Most are commonly encountered when working with 3D printers; some may only be of interest if fabricating a wiring harness.

## Basic Considerations

- Electrical properties
    - Ampacity
    - Resistance
    - Temperature rise & operating temperature
- Physical properties
    - Mating force
    - Locking/latching method
    - Uses (board, free hanging, panel mount)
    - Pin sizes/compatible wire gauges
    - Overall connector size
- Other Considerations
    - Cost
    - Availability

!!! note
    Most entries contain a line labeled "application". This will be at least one of three values:

    - Board
    - Free hanging
    - Panel mount

    Board connectors have one connector for a board and mating connector for the cable.

    Free hanging connectors mate two two cables together. Panel mount connectors are a type of free hanging connector that can also be attached to a panel (usually by snapping in place with a pair of "ears").
    
<!-- 
### Title

Common uses:

**Specifications**

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

### Amphenol Micro Power

These are an affordable alternative to Micro Fit 3 that unfortunately do not have a panel mount option.

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 3.0mm
- Max Current Rating: 5A
- Wire Gauges: AWG #20-#30
- Applications: board, inline
- Available Positions:
    - Single Row: 2-12 position
    - Dual Row: 4-24 position

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Inexpensive
- [x] 5A current rating
- [ ] No panel mount housings
- [ ] One pin type for gauge #20-#30 may make smaller wires hard to crimp
- [ ] Not very common; no kits available
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_amp_micropower]{ .md-button }

</div></div>
</div>

### Harwin M20 / "DuPont"

These are very simple, common connectors for bare 0.1" headers. They are not latching or locking and should be avoided (or used with hot glue for retention)

1. [Why are they called DuPont connectors?][dupont_name]
2. [Why are they so hard to crimp?][dupont_crimp]

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 2.54mm
- Max Current Rating: 3A
- Wire Gauges: AWG #22-#30
- Applications: board only
- Available Positions:
    - Single Row: 2-12 position
    - Dual Row: 4-24 position

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Mates easily with headers.
- [x] Good for temporary connections.
- [ ] No latch or lock mechanism.
- [ ] Can be difficult to crimp.
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_harwin_m20]{ .md-button }

[:simple-amazon: Assorted Single Row Kit][az_harwin_m20]{ .md-button } 

</div></div>
</div>

------

### JST PH

These have wide application as a compact connector for PCBs when space is at a premium. NEMA 17 steppers often use this connector.

The small pitch can make these difficult to crimp.

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 2.0mm
- Current Rating: 2.0A / #24 AWG
- Wire Gauges: #24 - #32 AWG
- Applications: board only
- Available Positions:
    - Single Row: 2-16

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Inexpensive
- [x] Very compact
- [ ] Low mating cycle rating
- [ ] Can be difficult to crimp
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_ph]{ .md-button }

[:simple-amazon: 2-6 Position Kit][az_jst_ph]{ .md-button } 

</div></div>
</div>

------

### JST RCY

These are sometimes called JST SYP, though JST lists the product as RCY series. RCY connectors are used in 3D printing to extend wire pairs (or make them disconnectable) as an inline alternative to XH or PH connectors. RCY are also physically smaller in size than SM.

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 2.5mm
- Max Current Rating: 3.0A / AWG #22 (2.0A / AWG #24)
- Wire Gauges: AWG #22-#28
- Applications: inline only
- Available Positions: 2
- Common uses: remote-controlled cars and airplanes.
- Notes: usually red or black. Sometimes found in 2.54mm pitch.

</div></div>
<div markdown><div markdown>
**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Inexpensive
- [x] Useful for splicing
- [ ] Low mating cycle rating
- [ ] 2-position only
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_rcy]{ .md-button }

[:simple-amazon: 2 Position Kit][az_jst_rcy]{ .md-button } 

</div></div>
</div>

------

### JST SH

This connector is most familiar to BLTouch users with the 5-position female connector. The 4-position female SH connector is used for the SparkFun Qwiic and Adafruit Stemma QT interconnects for I2C.

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 1.0mm
- Current Rating: 1.0A
- Wire Gauges: AWG #28-#32
- Applications: board only
- Available Positions:
    - Single Row: 2-15, 20

</div></div>
<div markdown><div markdown>
**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Extremely compact
- [ ] Nearly impossible to crimp at home
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_sh]{ .md-button }

[:simple-amazon: 5 Position Kit][az_jst_sh]{ .md-button } 

</div></div>
</div>

------

### JST SM

Although these connectors are only for wire-to-wire connections, they are easy to crimp and can be panel mounted. A downside to SM connectors is the size of the shell.

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 2.5mm
- Max Current Rating: 3.0A / AWG #22
- Wire Gauges: AWG #22 - #28
- Applications: free hanging, panel mount
- Available Positions:
    - Single Row: 2-12 position
    - Dual Row: 18 position
- Common uses: RGB LED light strips
- Notes: found in a wide variety of colors, most commonly white or ivory.

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Easy to crimp
- [x] Simple, large latching mechanism
- [x] Panel mounts
- [ ] Bulky connector housing
- [ ] Pins are mechanically weak and prone to bending
- [ ] Not rated for frequent disconnection
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_sm]{ .md-button }

[:simple-amazon: 2-5 Position Kit][az_jst_sm_small]{ .md-button } 

[:simple-amazon: 2-9 Position Kit][az_jst_sm_full]{ .md-button } 

</div></div>
</div>

------

### JST XH

This is the most common connector for 3D printers (e.g., most board-side connectors & limit switches)

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 2.5mm
- Current Rating: 3.0A / AWG #22
- Wire Gauges: AWG #22 - #30
- Applications: board only
- Available Positions:
    - Single Row: 2-16 position & 20 position

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Easy to crimp larger gauges
- [x] Very common and inexpensive
- [ ] Not rated for more than a few mating cycles
- [ ] Difficult to crimp smaller gauge wires
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_jst_xh]{ .md-button }

[:simple-amazon: 2-5 Position Kit][az_jst_xh]{ .md-button } 

</div></div>
</div>

------

### Molex Micro Fit 3.0

Perfect but for the price. Found on 3D printers, particularly as hotend connectors.

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 3.0mm
- Max Current Rating: up to 8.5A
- Wire Gauges: AWG #18 - #24, #26 - #30 (two pin sizes)
- Applications: board, free hanging, panel mount
- Available Positions:
    - Single Row: 2-11 position
    - Dual Row: 2-24 position

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Easy to crimp
- [x] Reliable latching mechanism
- [x] Board, inline, and panel mounted
- [x] Relatively high current rating
- [x] High temperature rating
- [ ] Expensive
- [ ] Can be hard to source
- [ ] Connectors larger than 16 position are hard to remove
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_molex_mf3]{ .md-button }

[:simple-digikeyelectronics: 2-6 Position Kit][dk_molex_mf3]{ .md-button } 

</div></div>
</div>

------

### Molex Mini Fit Jr

This is the familiar ATX connector used in computers for motherboard and video card power.

This connector may have application for heated beds (using two or more parallel circuits).

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Pitch: 4.2mm
- Max Current Rating: 9A
- Wire Gauges: AWG #18 - #24, #24 - #28 (two pin sizes)
- Applications: board, free hanging, panel mount
- Available Positions:
    - Single Row: 2-6 position
    - Dual Row: 2-24 position

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Large, reliable latch
- [x] Panel mounts
- [ ] Large connector housing
- [ ] Expensive
- [ ] Can be hard to source
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_molex_mfjr]{ .md-button }

[:simple-digikeyelectronics: Dual Row 2-20 Position Kit][dk_molex_mfjr]{ .md-button } 

</div></div>
</div>

------

### XT60

Unlike most pin and socket connectors in this list, wires are soldered in place for XT60 connectors. These are an inexpensive solution for high current applications (such as powering a heated bed).

<div class="nt-cards nt-grid cols-2" markdown>
<div markdown><div markdown>

**Specifications**

- Max Current Rating: 30A (60A instantaneous)
- Wire Gauges: AWG #12
- Applications: free hanging, panel mount
- Available Positions: 2 position
- Common uses: RC car batteries

</div></div>
<div markdown><div markdown>

**Pros and Cons**

<div class="jh-proconlist" markdown>
- [x] Inexpensive
- [x] High current rating
- [x] Panel mounts
- [ ] Requires soldering
</div>

</div></div>
<div markdown><div markdown>

**Links**

[:material-order-alphabetical-ascending: Datasheet][ds_xt60]{ .md-button }

[:simple-sparkfun: SparkFun Connector Pair][sf_xt60]{ .md-button } 

</div></div>
</div>


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

### Aviation

!!! todo "TODO: Expand"
### DSUB

!!! todo "TODO: Expand"

## Low-Voltage, Low-Current Connectors
### IDC Ribbon

IDC stands for insulation-displacement contact. These are meant for low-voltage, low-current applications, particularly digital signaling. They are most frequently found on LCD 3D printer displays.

These connectors are not meant for frequent mating and removal. They should be avoided where possible.

### RJ-45

RJ-45 is the specification for the connector that terminates Ethernet cables, often generically referred to as Cat5 or Cat6 cables. RJ-45 connectors are not suitable for applications with more than a few hundred milliamps of current.

**Pros and Cons**

<div markdown class="jh-proconlist">
- [x] Readily available
- [x] Inexpensive
- [x] Latching
- [ ] Large connector housing and mating terminal
- [ ] Very low current rating
</div>

!!! todo "TODO: Expand"

## Further Reading

- [SparkFun: Connector Basics][sparkfun_connectors]

[ds_molex_mf3]:     ../assets/datasheets/molex_mf3.pdf
[ds_molex_mfjr]:    ../assets/datasheets/molex_mfjr.pdf
[ds_jst_ph]:        ../assets/datasheets/jst_ph.pdf
[ds_jst_sm]:        ../assets/datasheets/jst_sm.pdf
[ds_jst_xh]:        ../assets/datasheets/jst_xh.pdf
[ds_jst_rcy]:       ../assets/datasheets/jst_rcy.pdf
[ds_harwin_m20]:    ../assets//datasheets/harwin_m20.pdf
[ds_jst_sh]:        ../assets/datasheets/jst_sh.pdf
[ds_xt60]:          ../assets/datasheets/xt60.pdf
[ds_amp_micropower]:          ../assets/datasheets/micro_power.pdf