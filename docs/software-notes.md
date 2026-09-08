# Software notes

The [PiGRRL 2 software guide](https://learn.adafruit.com/pigrrl-2/software) uses RetroPie and Adafruit retrogame. I've included the guide's input software for reference while my original device configuration is unavailable.

## How the buttons work in the reference software

A button connects its configured GPIO input to ground. Retrogame looks up that pin in its configuration and sends a virtual keyboard event through Linux uinput. The emulator or menu then interprets the key as a control.

| File | Purpose |
| --- | --- |
| retrogame.c | Reads inputs and generates keyboard events |
| keyTable.h | Maps key names to Linux input codes |
| keyTableGen.sh | Generates the key table |
| Makefile | Builds retrogame |
| configs/retrogame.cfg.pigrrl2 | Example PiGRRL 2 button mapping |
| README.md | Original setup notes |

The files are in [upstream/Adafruit-Retrogame/](../upstream/Adafruit-Retrogame/), with the original copyright and license notices.

## Using the reference

The mapping uses Broadcom GPIO numbers, not physical connector positions. It also includes buttons from the original PiTFT display, so it should not be treated as a wiring diagram for my larger-screen build.

The Makefile uses GCC and libgpiod; the program also depends on Linux input headers and uinput. Follow the original guide for setup and check the wiring before running it. I haven't tested this imported version on my handheld.

The exact source revision is recorded in [UPSTREAM.md](../upstream/Adafruit-Retrogame/UPSTREAM.md). My final display settings and the fix for pixelated output still need to be recovered.
