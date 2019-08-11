# Alpaca

Absolutely Legit Playstation Arcade-style Controller for All.

A collection of hardware and software projects for a custom Project DIVA: Future Tone (DX) arcade-style controller.

Totally not related to {T,E}LAC and that s****u guy.

## Revisions

### v1 - "Genesis - It does what <strike>Ninten</strike>other competitors don't"

Initial version. Finished somewhere in July 2018.

#### Hardware

- Laser cuttable case: [Alpaca-Case](https://github.com/dogtopus/Alpaca-Case)
- Buttons: Generic Chinese 100mm buttons w/ Sanwa OBSA-SP-200G
- Slider: Resistive (SoftPot)
- PCB: Teensy LC
  - Input: 2x CD4021B
  - Button LED: TPIC6C596
  - Auth: USB Host Shield (MAX3421E)
- Power Source: USB + 5VDC

#### Firmware

[Alpaca-FW](https://github.com/dogtopus/Alpaca-FW)

#### BOM

TBA

#### Wiring diagram

[doc/v1/wiring/out/wiring.pdf](doc/v1/wiring/out/wiring.pdf)

### v2 - "The PitchBender"

In development. Specs listed below may change at any moment.

#### Hardware

- Laser cuttable case: [Alpaca-Case#v2](https://github.com/dogtopus/Alpaca-Case/tree/v2)
- Buttons: Generic Chinese 100mm buttons w/ Sanwa OBSA-SP-200G
- Slider: 32-channel capacitive (codename LKP v1) with WS281x RGB LED
- PCB: Teensy LC + TeensyFighter LC (perfboard option is also possible)
  - Input: MCP23017 (on TeensyFighter LC PCB)
  - Button LED: TPIC6C596 (over SPI)
  - Auth: USB Host Shield (MAX3421E over SPI)
- Power Source: USB + 9V-24V DC (At least 20W)

A mod kit for Project DIVA Arcade Future Tone stock control panel is also planned.

#### Firmware

Main: [Alpaca-FW](https://github.com/dogtopus/Alpaca-FW)

LKP: TBA

#### BOM

TBA

#### Wiring diagram

TBA

#### Progress

| Subproject | Status | Description |
| ---------- | ------ | ----------- |
| Alpaca-Case v2 | WIP | ~35%. Working on support structure rework. TODO: LKP footprint and mount, edge-lit LED mount, new mounting brackets. |
| LKP v1 | WIP | FW: ~70%, EE: 100%, ME (part of Alpaca-Case): 50%. |
| TeensyFighter LC | WIP | ~40%. Working on schematic and component selection. TODO: PCB layout. |
| UHS Mini to TeensyFighter Adapter | Planned | |
| TPIC6C596 board for TeensyFighter | Planned | |
| lib15275 | WIP | ~80%. TODO: LED pattern generator (also used in LKP) |
