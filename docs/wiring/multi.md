---
title: Segmented Connectors
summary: Connectors with multiple components carried in parallel.
authors: Jon Harper
date: 2022-11-29
---

--8<-- "include/electrical_disclaimer.md:crimp"

??? note "Reading Entries"
    - `Name`: an abbreviation for what the pin does. This is for identification only.
    - `Pin #`: order of the pin in the connector.
    - `Color`: optional color-coding for the wire insulation.
        - Colors are solely to help visual identification.
        - Colors do not always match the wire colors that usually tail a component; this is meant to maintain internal consistency.

    See the [tips](panel_tips.md) page for a more details explanation.

### X Limit Switch and Stepper

| Pin #  | Name     | Color             |  Color             | Name     | Pin #   |
|:------:|:--------:|:-----------------:|:------------------:|:--------:|:-------:|
| **1**  | LIMX SIG | Y :yellow_circle: | W ![white][white]  | LIMX GND | **4**   |
| **2**  | MOTX 1A  | R :red_circle:    | G :green_circle:   | MOTX 2A  | **5**   |
| **3**  | MOTX 1B  | B :blue_circle:   | K ![black][black]  | MOTX 2B  | **6**   |

[black]: ../img/black_circle.png
[white]: ../img/white_circle.png