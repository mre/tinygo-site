---
title: "HiFive1 RevB"
weight: 3
---

The [HiFive1 Rev B](https://www.sifive.com/boards/hifive1-rev-b) is low-cost, Arduino-compatible development board featuring the [Freedom E310](https://www.sifive.com/chip-designer#fe310) 320+ MHz [RISC-V](https://riscv.org/) chip.

## Interfaces

| Interface | Hardware Supported | TinyGo Support |
| --------- | ------------- | ----- |
| GPIO      | YES | YES |
| UART      | YES | YES |
| SPI      | YES | Not yet |
| I2C      | YES | Not yet |
| ADC      | NO | NO |
| PWM      | YES | Not yet |

## Flashing

### MSD Flashing

The HiFive1 RevB comes with a bootloader that allows Mass Storage Device (MSD) flashing. This means you can just copy the compiled `.hex` file generated by TinyGo onto it, no additional flashing software is needed.

- Plug your HiFive1 RevB into your computer's USB port.

- The HiFive1 RevB board will appear to your computer like a USB drive.

- Build and flash your TinyGo program using `tinygo flash` like this:

    ```shell
    tinygo flash -target=hifive1b [PATH TO YOUR PROGRAM]
    ```

- The HiFive1 RevB should restart and begin running your program.
