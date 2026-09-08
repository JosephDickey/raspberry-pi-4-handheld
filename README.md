# Raspberry Pi 4 Handheld

**July–August 2024 · Inspired by PiGRRL 2**  
Raspberry Pi 4B · Meshmixer · 3D printing · Linux

I built this handheld using a Raspberry Pi 4B and a 5-inch screen, with Adafruit's PiGRRL 2 guide as the starting point. The larger screen and different power supply meant changing the enclosure as well as assembling the electronics.

<img src="images/finished-handheld.jpg" alt="My red handheld displaying a basketball game's player-selection screen" width="480">

## Building the enclosure

I used Meshmixer to adapt the enclosure and went through about ten printed versions. Each one was still slightly too small once I tried fitting everything inside. I eventually used hot glue to join the sides and get it closed.

The two Meshmixer files I still have are in [cad/](cad/). This was a working prototype, but the enclosure fit was something I wanted to improve on the next build.

## Hardware and troubleshooting

| Part | Build details |
| --- | --- |
| Computer | Raspberry Pi 4 Model B |
| Display | 5-inch screen |
| Power | Battery and a different power supply from the guide |
| Controls | D-pad and physical game buttons |
| Audio | Speaker and amplifier |
| Enclosure | Adapted in Meshmixer and 3D printed |
| Software | Linux-based emulation environment |

Getting the new screen working also took some troubleshooting because the output was very pixelated. I got it working, but I no longer remember the exact fix.

The bigger problem was heat. I had overlooked ventilation in the enclosure, and the handheld overheated. I didn't fix that in this version. In the [Pi 5 upgrade](https://github.com/JosephDickey/raspberry-pi-5-handheld), I added vents and copper heatsinks.

## Build photos

### Assembly

<img src="images/assembly.jpg" alt="Display, Raspberry Pi, controls, speaker, power board, and battery during assembly" width="760">

### Internal layout

<img src="images/internal-layout.jpg" alt="Raspberry Pi, battery, and wiring inside the handheld enclosure" width="760">

## Design files and code

| Resource | Contents |
| --- | --- |
| [Meshmixer files](cad/) | My two saved enclosure project files |
| [Build notes](docs/engineering-notes.md) | More detail on fit, display, and cooling problems |
| [Software notes](docs/software-notes.md) | How the guide's input software works |
| [retrogame.c](upstream/Adafruit-Retrogame/retrogame.c) | Adafruit's original GPIO-to-keyboard utility |
| [PiGRRL 2 configuration](upstream/Adafruit-Retrogame/configs/retrogame.cfg.pigrrl2) | Adafruit's example button mapping |

The included code is unchanged Adafruit reference code. I haven't recovered my device configuration or confirmed which printed revisions the saved Meshmixer files match. Exact component models, the display fix, and temperature/runtime measurements are also missing from my notes.

## Credits

The build was inspired by [PiGRRL 2 by Adafruit's Ruiz Brothers](https://learn.adafruit.com/pigrrl-2/overview).

[Adafruit-Retrogame](https://github.com/adafruit/Adafruit-Retrogame) was originally written by Phil Burgess for Adafruit Industries, with later contributions from others. Its license notices are preserved; see [UPSTREAM.md](upstream/Adafruit-Retrogame/UPSTREAM.md) for the source version.

No ROMs, BIOS files, or disk images are included.

## Other builds

- [Pi 5 handheld](https://github.com/JosephDickey/raspberry-pi-5-handheld) — the follow-up to this project
- [Touchscreen mini TV](https://github.com/JosephDickey/raspberry-pi-touchscreen-tv)
