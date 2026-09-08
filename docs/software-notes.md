# Software reference

The [PiGRRL 2 software guide](https://learn.adafruit.com/pigrrl-2/software) uses RetroPie for emulation and Adafruit retrogame for physical button input. The source included here is the retrogame reference associated with that guide. The exact software versions and configuration from my 2024 device have not been recovered.

## Input path

In the reference implementation, a physical button connects a configured GPIO input to ground. Retrogame interprets that input using a GPIO-to-key mapping and emits Linux virtual keyboard events through uinput. An emulator or frontend then uses those keyboard events as game controls.

## Included code

| File | Purpose |
| --- | --- |
| retrogame.c | Input handling and virtual keyboard event generation |
| keyTable.h | Mapping between key names and Linux input codes |
| keyTableGen.sh | Generates the key table from Linux input headers |
| Makefile | Builds the retrogame executable |
| configs/retrogame.cfg.pigrrl2 | Adafruit's PiGRRL 2 example button mapping |
| README.md | Original upstream documentation |

All are under [upstream/Adafruit-Retrogame/](../upstream/Adafruit-Retrogame/). Copyright and license notices remain in the source.

## Mapping versus my build

The example configuration uses Broadcom GPIO numbering, not connector pin positions. It includes PiTFT-specific buttons belonging to the original design. It is not a confirmed wiring map for my 5-inch-screen adaptation.

No screen driver or resolution settings are supplied as my recovered configuration. The exact pixelation fix is not known.

## Build context

The included Makefile uses GCC and links libgpiod. The source also uses Linux input headers and uinput. It is a reference snapshot for inspection, not a tested installer for this handheld. Its compatibility with the software on my device has not been verified.

Consult the original guide and upstream documentation for setup details, and match any GPIO configuration to the actual wiring before running it. The upstream source may have evolved after the original build; its exact imported revision is recorded in UPSTREAM.md.
