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
    - `Color`: optional color-coding for the conducting wire. 
        - Colors do not always match the wire colors that usually tail a component; this is meant to maintain internal consistency.
        - Colors are solely to help visual identification.
    
    | Color  | Abbreviation      |
    |--------|:-----------------:|
    | Black  | K ![black][black] |
    | Blue   | B :blue_circle:   |
    | Green  | G :green_circle:  |
    | Red    | R :red_circle:    |
    | White  | W ![white][white] |
    | Yellow | Y :yellow_circle: |

X Limit Switch and Stepper

| Pin #  | Name     | Color             | Pin #   | Name     |  Color             |
|:------:|:--------:|:-----------------:|:-------:|:--------:|:------------------:|
| 1      | LIMX SIG | Y :yellow_circle: | 4       | LIMX GND | W ![white][white]  |
| 2      | MOTX 1A  | R :red_circle:    | 5       | MOTX 2A  | G :green_circle:   |
| 3      | MOTX 1B  | B :blue_circle:   | 6       | MOTX 2B  | K ![black][black]  |


[black]: ../img/black_circle.png
[white]: ../img/white_circle.png