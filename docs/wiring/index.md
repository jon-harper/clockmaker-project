---
title: Panel Mount Tips
summary: Tips and recommended pin orders for panel-mounted connectors.
authors: Jon Harper
date: 2022-11-29
---

!!! warning "Disclaimer"

    - These are advisory to help save time designing your own harnesses.
    - Recommendations are not universal; they are starting points to begin your own efforts.
    - No information here replaces the advice of a professional.
    - It does not matter if your harness matches the order or color in the tables, only that your harness is consistent and documented.
    - Label your wires!
    - **Test your crimps!**

## Overview

### Connector Patterns

There are two types of panel-mounted connector patterns. This guide starts with a one-to-one pattern, then uses this build larger cable segments in a one-to-many pattern.

#### One-to-One Panels

<figure markdown>
  [![Example of a one-to-one panel][img_single]{width="480"}][img_single]
  <figcaption>Each component of the printer has an individual connector on the panel.</figcaption>
</figure>

These are point-to-point, single component connectors. 

#### One-to-Many Panels

<figure markdown>
  [![Example of a one-to-many panel][img_multi]{width="480"}][img_multi]
  <figcaption>Grouping components into one connector greatly reduces the nubmer of cables and simplifies servicing.</figcaption>
</figure>

A one-to-many panel mount connects multiple components. From the panel, the cable may branch further. These are significantly more complex to assemble, but offer a much cleaner look and tighter cabling.


### Reading Entries

Each table has three columns:

- `Name`: an abbreviation for what the pin does. This is for identification only.
- `Pin #`: order of the pin in the connector.
- `Color`: optional color-coding for the conducting wire. 
    - Colors do not always match the wire colors that usually tail a component; this is meant to maintain internal consistency.
    - Colors are solely to help visual identification.

Below each tables are notes. Some common notes:

- `Typical AWG`: this value reflects commonly used wire gauges for a component
    - Dual gauges reflect cases where a larger gauge may be easier to crimp and simplify sourcing.
    - This value is typically 24/28 AWG for signal wires or low-current fans.
- `Common Termination`: for components that come pre-terminated, this lists the type of connector that the part ships with. Your MCU may not use the same type of termination.

### Wire Colors

Six (6) color sets of hookup wire often come with the same six colors. We use this palette throughout, along with the following abbreviations:

| Color  | Abbreviation      |
|--------|:-----------------:|
| Black  | K :black_circle:   |
| Blue   | B :blue_circle:   |
| Green  | G :green_circle:  |
| Red    | R :red_circle:    |
| White  | W :white_circle:  |
| Yellow | Y :yellow_circle: |

### Secondary Colors

Most pin types will have the same wire color: analog signals are yellow, PWM pins are green.

`GND` and `VIN` are black and red, respectively. To help balance the lengths of color used in a harness, some pins list a secondary color.

- 3.3-volt and 5-volt VIN pins have blue as a secondary color where enough colors are available.
- GND pins that are drains for analog signal pins have white as a secondary color.

## Considerations

[img_single]: ../img/wiring/single_panel.jpg
[img_multi]: ../img/wiring/multi_panel.jpg

[single]: single.md "One-to-One Connectors"
[multi]: multi.md "Segmented Connectors"