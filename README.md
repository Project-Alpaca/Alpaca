<p align="center"><img alt="alpaca" src="./alpaca2.webp" /></p>

# Alpaca

Absolutely Legit P\*\*\*\*\*\*\*\*\*n Arcade-style Controller for All.

A collection of hardware and software projects for a custom Project DIVA: Future Tone (DX) arcade-style controller.

## Revisions

### v1 - "Genesis - It does what <strike>Ninten</strike>other competitors don't"

Initial version. Finished somewhere in July 2018.

#### Hardware

- Laser cuttable case: [Alpaca-Case#v1](https://github.com/Project-Alpaca/Alpaca-Case/tree/v1)
- Buttons: Generic Chinese 100mm buttons w/ Sanwa OBSA-SP-200G
- Slider: Resistive (SoftPot)
- PCB: Teensy LC
  - Input: 2x CD4021B
  - Button LED: TPIC6C596
  - Auth: USB Host Shield (MAX3421E)
- Power Source: USB + 5VDC

#### Firmware

[Alpaca-FW](https://github.com/Project-Alpaca/Alpaca-FW)

#### BOM

TBA

#### Wiring diagram

[doc/v1/wiring/out/wiring.pdf](doc/v1/wiring/out/wiring.pdf)

### v2 - "The PitchBender"

In development. Specs listed below may change at any moment.

#### Hardware

- Laser cuttable case: [Alpaca-Case](https://github.com/Project-Alpaca/Alpaca-Case)
- Buttons: Generic Chinese 100mm buttons w/ Sanwa OBSA-SP-200G
- Slider: [LKP](https://github.com/Project-Alpaca/LKP) with WS2813 RGB LED strip (144/m, 72 LEDs total)
- PCB: Teensy LC ~~+ TeensyFighter LC~~ (perfboard option is also possible)
  - Input: ~~MCP23017 (on TeensyFighter LC PCB)~~ 2x CD4021B
  - Button LED: TPIC6C596 (over SPI)
  - Auth: USB Host Shield (MAX3421E over SPI)
- Alternative PCB: Alpaca-NGIO
  - Input: On-chip GPIO
  - Button LED: External MCP23008+ULN2803A over I2C. (details TBA)
  - Auth: On-board USB or native
- Alternative PCB: [Alpaca-OwO](https://github.com/Project-Alpaca/Alpaca-OwO/tree/v1.0)
  - Input: On-chip GPIO
  - Button LED: External MCP23008+ULN2803A over I2C. (details TBA)
  - Auth: Native
- Power Source: USB + 9V-24V DC (At least 20W)

A mod kit for Project DIVA Arcade Future Tone stock control panel is also planned.

#### Firmware

Main: [Alpaca-FW](https://github.com/Project-Alpaca/Alpaca-FW) for v1 electronics, passinglink (details TBA) for Alpaca-NGIO.

LKP: [LKP-FW](https://github.com/Project-Alpaca/LKP-FW) (Native variant, WIP.)

#### BOM

TBA

#### Wiring diagram

TBA

#### Progress

Crucial: Whether or not using alternatives from Alpaca v1 is feasible.
- Yes: No alternative from Alpaca v1. Component is essential for Alpaca v2.
- No: Alpaca v1 components will work to some extent and their v2 counterpart can be developed later. Or the component is optional.

##### Hardware

| Subproject | Crucial? | Status | Description |
| ---------- | -------- | ------ | ----------- |
| Alpaca-Case v2 | ⭕ Yes | ✅ Done | Prerelease. |
| LKP v1 | ⭕ Yes | ✅ Done | Schematic and parts: Done, PCB: Done. |
| LKP-Diva-Assy | ⭕ Yes | ✅ Done | LKP PCB holder: Done, LED strip mount: Done. |
| ~~Alpaca-NGIO~~ | ❌ No | ❌ Delayed indefinitely | |
| Alpaca-OwO | ❌ No | 🚧 WIP | Pending testing |

##### Software

| Subproject | Crucial? | Status | Description |
| ---------- | -------- | ------ | ----------- |
| Alpaca-FW | ⭕ Yes | 🚧 WIP | RP2040 support: 0%, LKP interop: 0%, lib15275 interop: WAIT. |
| LKP-FW | ⭕ Yes | ✅ Done | Native: Done (First PoC), 15275 Serial: Done. |
| lib15275 | ❌ No | 🚧 WIP | ~80%. Request/response: Done, LED pattern generator: TODO |
