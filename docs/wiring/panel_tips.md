---
title: Panel Mount & Harness Tips
summary: Tips and recommended pin orders for panel-mounted connectors.
authors: Jon Harper
date: 2022-11-29
---

--8<-- "include/electrical_disclaimer.md:crimp"

## Reading Pin Order Entries

Each pin order table has three columns:

- `Name`: an abbreviation for what the pin does. This is for identification only.
- `Pin #`: order of the pin in the connector.
- `Color`: optional color-coding for the conducting wire. 
    - Colors do not always match the wire colors that usually tail a component; this is meant to maintain internal consistency.
    - Colors are solely to help visual identification.

### Entry Abbreviations

Abbreviations for components have three parts: `[Type][Position][#]`.

For example, in `MOTZ2`:

- `MOT` is motor;
- `Z` is the axis; and
- `2` refers to the second stepper.

#### Component Names

| Abbreviation | Component          |
|--------------|--------------------|
| ABL          | ABL sensor         |
| BED          | Heated bed         |
| FAN          | Fan                |
| FIL          | Filament runout sensor |
| HOT          | Hotend             |
| I2C          | I2C bus            |
| LIM          | Limit switch       |
| LGT          | Light (not RGB)    |
| MOT          | Stepper motor      |
| PE           | Protective earth   |
| RGB          | RGB LEDs           |
| SPI          | SPI bus            |
| TH           | Thermistor         |

#### Positions: Steppers and Limit Switches

| Abbreviation | Position |
|--------------|----------|
| X            | X axis   |
| Y            | Y axis   |
| Z            | Z axis   |

#### Positions: Fans, Lights, and Thermistors

| Abbreviation | Position |
|--------------|----------|
| H            | Hotend/toolhead |
| E            | Electronics enclosure   |
| C            | Chamber/printer enclosure |

### Wire Colors

Six (6) color sets of hookup wire often come with the same color combinations. We use this palette throughout, along with the following abbreviations:

| Color  | Abbreviation      |
|--------|:-----------------:|
| Black  | K ![black][black] |
| Blue   | B :blue_circle:   |
| Green  | G :green_circle:  |
| Red    | R :red_circle:    |
| White  | W ![white][white] |
| Yellow | Y :yellow_circle: |

### Secondary Colors

Most pin types will have the same wire color: analog signals are yellow, PWM pins are green.

`GND` and `VIN` are black and red, respectively. To help balance the lengths of color used in a harness, some pins list a secondary color.

- 3.3-volt and 5-volt VIN pins have blue as a secondary color where enough colors are available.
- GND pins that are drains for analog signal pins have white as a secondary color.

## Considerations

### Wire Gauges

If you do not regularly work with hookup wire, up-gauging to AWG #24 for any smaller gauge is an option to reduce sourcing costs.

##### Pros & Cons

<div class="jh-proconlist" markdown>
- [x] Saves by buying more of one type of wire.
- [x] Larger wires can be easier to work with.
- [x] Reduce number of pins types for some connectors (e.g., Molex Mini Fit family)
- [ ] Increases thickness of wire bundle.
- [ ] Can significantly increase weight of toolhead bundle.
</div>

### Panel Mount Connector Patterns

There are two ways of designing of a wiring panel. This guide starts with a one-to-one pattern, then uses this build larger cable segments in a one-to-many pattern.

#### One-to-One Panels

<figure markdown>
  [![Example of a one-to-one panel][img_single]{width="480"}][img_single]
  <figcaption>Each component of the printer has an individual connector on the panel.</figcaption>
</figure>

These are point-to-point, single component connectors.

##### Pros & Cons

<div class="jh-proconlist" markdown>
- [x] Simple to design: cables are point-to-point.
- [x] Cables can be replaced easily.
- [ ] Large number of connectors to connect & disconnect.
- [ ] Messy wire bundles.
- [ ] Significant slack must be left before wrapping bundle.
</div>

#### One-to-Many Panels

<figure markdown>
  [![Example of a one-to-many panel][img_multi]{width="480"}][img_multi]
  <figcaption>Grouping components into one connector greatly reduces the nubmer of cables and simplifies servicing.</figcaption>
</figure>

A one-to-many panel mount connects multiple components. From the panel, the cable may branch further.

##### Pros & Cons

<div class="jh-proconlist" markdown>
- [x] Easier to mate and disconnect.
- [x] Cheaper/fewer connectors to source.
- [x] Compact panels.
- [x] Tight wiring harnesses.
- [ ] Complex to design and assemble.
- [ ] Unforgiving of mistakes.
- [ ] Difficult or impossible to repair connectors with large numbers of pins.
</div>

## Further Reading

- [Falconer Electronics: Wire Harness Manufacturing Terms, Tools, and Tips of the Trade][tips]
- [Molex: Quality Crimping Handbook][crimping_handbook]
- [SparkFun: Working With Wire][sparkfun_wire]

[img_single]: ../img/wiring/single_panel.jpg
[img_multi]: ../img/wiring/multi_panel.jpg

[single]: single.md "One-to-One Connectors"
[multi]: multi.md "Segmented Connectors"

[black]: ../img/black_circle.png
[white]: ../img/white_circle.png

[tips]:             https://falconerelectronics.com/wire-harness-manufacturing/
[crimping_handbook]: ../assets/reading/qual_crimp.pdf