---
title: Single Components
summary: Panel mounted connector pin order guide.
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

    - `Typical AWG`: This is the gauge that is most often used for a given component.
    - `Common Termination`: The type of cable termination found most often for a component

    See the [tips](panel_tips.md) page for a more details explanation.
## General Components

### Hotend

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle:    |
| GND      | 2      | K ![black][black] |

- Typical AWG: 20
- Common Termination: screw post terminals or Molex Micro Fit 3.
- Notes:
    - Polarity does not matter.
    - Many JST connectors are limited to 3 amperes. This may be insufficient after derating for parallel conductors (and ambient temperature for enclosed printers).

### Heated Bed

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle:    |
| GND      | 2      | K ![black][black] |

- Typical AWG: none, specific to bed
- Common Termination: 
    - Screw post terminals (bare/ferrules)
    - Screw block terminals (ring/fork)
    - XT60 connectors
- Notes: 
    - Some beds also use a number of parallel circuits with lower-amperage connectors.
    - **AC beds need a [protective earth](#protective-earth) connection.**

### Stepper Motors

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| 1A       | 1      | R :red_circle:    |
| 1B       | 2      | B :blue_circle:   |
| 2A       | 3      | G :green_circle:  |
| 2B       | 4      | K ![black][black] |

- Typical AWG: 24
- Common Termination:
    - Board: JST XH, 4 position
    - Component: JST PH, 6 position or bare wire
- Notes:
    - There is not a standard wire color or pin order for stepper motors.

### Protective Earth

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| PE       | 1      | G :green_circle: / K ![black][black] |

- Typical AWG: none, specific to configuration
- Recommended Connector: Ring connector

## Fans

### Fan (2 Pin)

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: |
| GND      | 2      | K ![black][black] |

- Typical AWG: 24/28
- Common Termination: JST XH, 2 position
- Notes:
    - 24 awg is easier to crimp; 28 is sufficient.


### Fan (3 Pin)

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle:    |
| GND      | 2      | K ![black][black] |
| TAC      | 3      | Y :yellow_circle: |

- Typical AWG: 24/28
- Common Termination: Molex KK 254, 3 position ([Molex PN 22013037](https://www.molex.com/molex/products/part-detail/crimp_housings/0022013037))
- Notes:
    - 24 awg is easier to crimp; 28 is sufficient.
    - This reverses the typical GND/VIN pin order of most 4-pin fans.

### Fan (4 Pin)

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle:    |
| GND      | 2      | K ![black][black] |
| TAC      | 3      | Y :yellow_circle: |
| PWM      | 4      | G :green_circle:  |

- Typical AWG: 24/28
- Common Termination: Molex KK 254, 4 position ([Molex PN 470541000](https://www.molex.com/molex/products/part-detail/crimp_housings/0470541000))
- Notes:
    - 24 awg is easier to crimp; 28 is sufficient.
    - The pin order chart reverses the typical GND/VIN pin order of most 4-pin fans.

## Analog Sensors

Most sensors on a printer send analog signals, from thermistors to ABL sensors. These typically use 2- and 3-position connectors.

### Unpowered Sensors (2-wire)

Examples of unpowered sensors are mechanical limit switches and thermistors.

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| SIG      | 1      | Y :yellow_circle: |
| GND      | 2      | W ![white][white] / K ![black][black] |

- Typical AWG: 24/28
- Common Termination: JST XH is frequently used
- Notes: none

### Powered Sensors (3-wire)

Examples of powered sensors are optical limit switches and magnetic ABL sensors. Filament runout sensors may also be 3-wire.

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle: / B :blue_circle: |
| SIG      | 2      | Y :yellow_circle: |
| GND      | 3      | K ![black][black] / W ![white][white] |

- Typical AWG: 24/28
- Common Termination: None
- Notes: none

## Digital Components & Buses

### BLTouch

BLTouches can be configured to work with 3.3V or 5V.

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle: / B :blue_circle: |
| GND      | 2      | K ![black][black] |
| PWM      | 3      | G :green_circle:  |
| SIG      | 4      | Y :yellow_circle: |
| GND      | 4      | W ![white][white] / K ![black][black] |

### I2C

I2C is a 3.3V digital signalling bus. Short cables and eliminating EMI are important to working with I2C. I2C is often used with embedded devices such as atmospheric monitoring sensors.

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle: / B :blue_circle: |
| GND      | 2      | K ![black][black] |
| SDA      | 3      | Y :yellow_circle: |
| SCL      | 4      | G :green_circle:  |

- Typical AWG: None
- Common Termination: Adafruit and SparkFun use JST SH connectors for I2C.

### SPI

SPI is, like I2C, a 3.3V digital bus. It is slightly more forgiving of distance than I2C, but still suffers from noise and voltage drop. It is commonly used for ADXL-series accelerometers.

| Name     | Pin #  | Color             |
|:--------:|:------:|:-----------------:|
| VIN      | 1      | R :red_circle:    |
| GND      | 2      | K ![black][black] |
| SCLK     | 3      | G :green_circle:  |
| CS       | 4      | B :blue_circle:   |
| MOSI     | 5      | Y :yellow_circle: |
| MISO     | 6      | W ![white][white] |

- Typical AWG: None
- Common Termination: None

[black]: ../img/black_circle.png
[white]: ../img/white_circle.png