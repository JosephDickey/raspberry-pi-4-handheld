# Raspberry Pi 4 Handheld — PiGRRL 2 Inspired

**July–August 2024 · Hardware integration · Meshmixer · 3D printing · Embedded Linux**

A handheld emulation system built around a Raspberry Pi 4 Model B, a 5-inch screen, battery power, physical game controls, and integrated audio. I adapted the PiGRRL 2 concept to a larger display and different power hardware, then developed the enclosure through approximately ten printed iterations.

<img src="images/finished-handheld.jpg" alt="Assembled red handheld displaying a basketball game's player-selection screen" width="460">

## My engineering work

- **System integration:** Assembled the computer, display, battery/power hardware, controls, speaker, and amplifier into a working handheld.
- **Enclosure development:** Used Meshmixer to adapt the enclosure for the larger screen and component layout. Repeated print-and-fit attempts exposed clearance problems; I used hot glue to join the sides for the final assembly.
- **Display troubleshooting:** Worked through visibly pixelated output while integrating the replacement screen. The exact configuration change that resolved it is no longer recorded.
- **Thermal assessment:** Encountered overheating in the enclosure, which lacked dedicated ventilation. This remained a limitation of this build and informed the ventilation changes in my subsequent Raspberry Pi 5 handheld.

## Explore the project

| Artifact | What it shows |
| --- | --- |
| [Meshmixer design files](cad/) | Two retained enclosure project files from my build |
| [Engineering notes](docs/engineering-notes.md) | Fit iterations, display troubleshooting, and thermal lessons |
| [Controller source code](upstream/Adafruit-Retrogame/retrogame.c) | Adafruit's GPIO-to-keyboard input utility, included with its original license notice |
| [PiGRRL 2 controller configuration](upstream/Adafruit-Retrogame/configs/retrogame.cfg.pigrrl2) | The original guide's example GPIO mapping |
| [Software notes](docs/software-notes.md) | How the reference input software works and its relationship to this build |

## Hardware and design choices

| Subsystem | My build |
| --- | --- |
| Computer | Raspberry Pi 4 Model B |
| Display | 5-inch screen replacing the guide's smaller display |
| Power | Battery and alternative power-supply hardware |
| Input | D-pad and physical game buttons |
| Audio | Speaker and amplifier |
| Enclosure | Custom adaptation developed in Meshmixer and 3D printed |
| Software | Linux-based emulation environment |

The original [PiGRRL 2 guide](https://learn.adafruit.com/pigrrl-2/overview) centers on a Raspberry Pi 2 and 2.8-inch PiTFT. My larger display required an enclosure redesign rather than simply using the original housing. Exact screen and power-board model numbers have not been recovered.

## Development and results

| Challenge | Work performed | Outcome |
| --- | --- | --- |
| Enclosure too small | Approximately ten printed fit iterations in Meshmixer | Assembled housing; hot glue used to close the sides |
| Pixelated display output | Troubleshot integration of the replacement screen | Working display; exact fix not retained |
| Heat buildup | Identified missing ventilation as a design oversight | Unresolved in this version; addressed in the next handheld |

This was a working prototype with mechanical and thermal compromises. Its value as a development project was in bringing the subsystems together and discovering what needed to change in the next design. No temperature logs, battery-runtime measurements, or performance benchmarks are available for this version.

## Build photos

### Display, controls, audio, and power during assembly

<img src="images/assembly.jpg" alt="Open enclosure with display, Raspberry Pi, ribbon cable, speaker, power board, and battery" width="760">

### Internal component layout

<img src="images/internal-layout.jpg" alt="Internal assembly showing the Raspberry Pi, battery, wiring, and rear enclosure hardware" width="760">

## Credits and source status

The build was inspired by [Adafruit's PiGRRL 2 project by the Ruiz Brothers](https://learn.adafruit.com/pigrrl-2/overview). My contributions are the hardware adaptation, Meshmixer enclosure work, assembly, and troubleshooting documented here.

The included input software is from [Adafruit-Retrogame](https://github.com/adafruit/Adafruit-Retrogame), originally written by Phil Burgess for Adafruit Industries, with subsequent upstream contributions. It is included as an unchanged reference, not as code authored by me or a recovered snapshot of my device. See [source provenance](upstream/Adafruit-Retrogame/UPSTREAM.md).

The Meshmixer files are my retained project files; they have not been geometrically validated or confirmed to represent the exact final printed revision. No game ROMs, BIOS files, or disk images are included.
