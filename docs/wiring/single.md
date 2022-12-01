---
title: Single Components
summary: Panel mounted connector pin order guide.
authors: Jon Harper
date: 2022-11-29
---

!!! warning "Disclaimer"

    - This guide is solely to advise designing your own harnesses.
    - Recommendations are not universal; they are starting points to begin your own efforts.
    - No information here replaces the advice of a professional.
    - It does not matter if your harness matches the order or color in the tables, only that your harness is consistent and documented.
    - Label your wires!
    - **Test your crimps!**

## General Components

### Hotend

| Name     | Pin #  | Color            |
|:--------:|:------:|:----------------:|
| VIN      | 1      | R :red_circle:   |
| GND      | 2      | K :black_circle: |

- Typical AWG: 20
- Recommended Connector: Molex Micro Fit 3
- Notes:
    - Polarity does not matter.
    - JST SM is rated to 3 amperes. This may be insufficient after derating for parallel conductors (and ambient temperature for enclosed printers).

### Heated Bed

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: |
| GND      | 2      | K :black_circle: |

- Typical AWG: none, specific to bed

### Stepper Motors

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| 1A       | 1      | R :red_circle: |
| 1B       | 2      | B :blue_circle: |
| 2A       | 3      | G :green_circle: |
| 2B       | 4      | K :black_circle: |

- Typical AWG: 24
- Common Termination: JST XH 2.54, 2 position
- Notes:
    - There is not a standard wire color or pin order for stepper motors.

### Protective Earth

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| PE       | 1      | Y :yellow_circle: / G :green_circle: |

- Typical AWG: none, specific to configuration
- Recommended Connector: Ring connector

## Fans

### Fan (2 Pin)

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: |
| GND      | 2      | K :black_circle: |

- Typical AWG: 24/28
- Common Termination: JST XH 2.54, 2 position
- Notes:
    - 24 awg is easier to crimp; 28 is sufficient.


### Fan (3 Pin)

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: |
| GND      | 2      | K :black_circle: |
| TAC      | 3      | Y :yellow_circle: |

- Typical AWG: 24/28
- Common Termination: 
- Notes:
    - 24 awg is easier to crimp; 28 is sufficient.
    - This reverses the typical GND/VIN pin order of most 4-pin fans.

### Fan (4 Pin)

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: |
| GND      | 2      | K :black_circle: |
| TAC      | 3      | Y :yellow_circle: |
| PWM      | 4      | G :green_circle: |

- Typical AWG: 24/28
- Common Termination: 
- Notes:
    - 24 awg is easier to crimp; 28 is sufficient.
    - This reverses the typical GND/VIN pin order of most 4-pin fans.


## Analog Sensors

Most sensors on a printer send analog signals, from thermistors to ABL sensors. These typically use 2- and 3-conductor connectors.

### Unpowered Sensors (2-wire)

Examples of unpowered sensors are mechanical limit switches and thermistors.

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| SIG      | 1      | Y :yellow_circle: |
| GND      | 2      | W :white_circle: / K :black_circle: |

- Typical AWG: 24/28
- Common Termination: None, though JST XH 2.54 is very common
- Notes: none

### Powered Sensors (3-wire)

Examples of powered sensors are optical limit switches and 3-wire magnetic ABL sensors. Some filament runout sensors are also 3-wire.

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: / B :blue_circle: |
| SIG      | 2      | Y :yellow_circle: |
| GND      | 3      | K :black_circle: / W :white_circle: |

- Typical AWG: 24/28
- Common Termination: None
- Notes: none

## Digital Components & Buses

### BLTouch

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: / B :blue_circle: |
| GND      | 2      | K :black_circle: |
| PWM      | 3      | G :green_circle: |
| SIG      | 4      | Y :yellow_circle: |
| GND      | 4      | W :white_circle: / K :black_circle: |

### I2C

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle: / B :blue_circle: |
| GND      | 2      | K :black_circle: |
| SDA      | 3      | Y :yellow_circle: |
| SCL      | 4      | G :green_circle: |

### SPI

| Name     | Pin #  | Color |
|:--------:|:------:|:-----:|
| VIN      | 1      | R :red_circle:    |
| GND      | 2      | K :black_circle:  |
| SCLK     | 3      | G :green_circle:  |
| CS       | 4      | B :blue_circle:   |
| MOSI     | 5      | Y :yellow_circle: |
| MISO     | 6      | W :white_circle:  |
