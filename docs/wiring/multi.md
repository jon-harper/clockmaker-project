---
title: Composite Connectors, Part 1
summary: Basic example of multiple components on one connector.
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

    See the [tips](panel_tips.md) page for details.

Composite connectors may not be the technical term for connectors with pins that lead to multiple endpoints, but I have not found the correct one.

### X Limit Switch and Stepper

```mermaid
flowchart BT
    subgraph Panel
        X{{"Motion #1\n6P"}}
    end
    subgraph MCU
        LIMX("LIMX\n2P")
        MOTX("MOTX\n4P")
    end
    LIMX --- X
    MOTX --- X
```

| Pin #  | Name     | Color             |  Color             | Name     | Pin #   |
|:------:|:--------:|:-----------------:|:------------------:|:--------:|:-------:|
| **1**  | LIMX SIG | Y :yellow_circle: | W ![white][white]  | LIMX GND | **4**   |
| **2**  | MOTX 1A  | R :red_circle:    | G :green_circle:   | MOTX 2A  | **5**   |
| **3**  | MOTX 1B  | B :blue_circle:   | K ![black][black]  | MOTX 2B  | **6**   |

### Y, Z, Extruder, and Bed

```mermaid
flowchart BT
    subgraph Panel
        direction LR
        Y{{"Motion #2\n18P"}}
    end
    subgraph MCU
        direction LR
        LIMY("LIMY\n2P")
        LIMZ("LIMZ\n2P")
        MOTY("MOTY\n4P")
        MOTZ("MOTZ\n4P")
        MOTE("MOTE\n4P")
        TB("TB\n2P")
    end
    TB --- Y
    LIMY --- Y
    LIMZ --- Y
    MOTY --- Y
    MOTZ --- Y
    MOTE --- Y
```

| Pin #  | Name     | Color             |  Color             | Name     | Pin #   |
|:------:|:--------:|:-----------------:|:------------------:|:--------:|:-------:|
| **1**  | TB SIG   | Y :yellow_circle: | W ![white][white]  | TB GND   | **10**   |
| **2**  | LIMY SIG | Y :yellow_circle: | W ![white][white]  | LIMY GND | **11**  |
| **3**  | LIMZ SIG | Y :yellow_circle: | W ![white][white]  | LIMZ GND | **12**  |
| **4**  | MOTY 1A  | R :red_circle:    | G :green_circle:   | MOTY 2A  | **13**  |
| **5**  | MOTY 1B  | B :blue_circle:   | K ![black][black]  | MOTY 2B  | **14**  |
| **6**  | MOTZ 1A  | R :red_circle:    | G :green_circle:   | MOTZ 2A  | **15**  |
| **7**  | MOTZ 1B  | B :blue_circle:   | K ![black][black]  | MOTZ 2B  | **16**  |
| **8**  | MOTE 1A  | R :red_circle:    | G :green_circle:   | MOTE 2A  | **17**  |
| **9**  | MOTE 1B  | B :blue_circle:   | K ![black][black]  | MOTE 2B  | **18**  |

### Toolhead

```mermaid
flowchart BT
    subgraph Panel
        direction LR
        T{{"Toolhead\n8P"}}
    end
    subgraph MCU
        direction LR
        HOT("HOT\n2P")
        TH("TH\n2P")
        FH1("FH1\n2P")
        FH2("FH2\n2P")
    end
    HOT --- T
    TH --- T
    FH1 --- T
    FH2 --- T
```

| Pin #  | Name     | Color             |  Color             | Name     | Pin #   |
|:------:|:--------:|:-----------------:|:------------------:|:--------:|:-------:|
| **1**  | HOT VIN  | R :red_circle:    | K ![black][black]  | HOT GND  | **5**   |
| **2**  | FH1 VIN  | R :red_circle:    | K ![black][black]  | FH1 GND  | **6**   |
| **3**  | FH2 VIN  | R :red_circle:    | K ![black][black]  | FH2 GND  | **7**   |
| **4**  | TH SIG   | Y :yellow_circle: | W ![white][white]  | TH GND   | **8**   |

[black]: ../img/black_circle.png
[white]: ../img/white_circle.png