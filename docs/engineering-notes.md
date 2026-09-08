# Engineering notes

## Scope

This project was built in July–August 2024. It adapts the PiGRRL 2 handheld concept to a Raspberry Pi 4 Model B, 5-inch display, and different power hardware. These notes document my recollection of the build alongside retained photographs and Meshmixer files.

## Packaging a larger screen

Changing the display changed the enclosure requirements. I worked in Meshmixer and printed approximately ten iterations because successive housings were still slightly too small. Repeated physical fit checks were central to the process.

The finished assembly used hot glue to hold the sides together. This was a practical prototype closure, not evidence that all clearance and fastening problems had been solved. The retained files are in [cad/](../cad/); I have not reconstructed a dimension-by-dimension revision history.

The mechanical lesson was to account for the assembled component stack, wiring space, and closure fit together. A part that fits individually does not establish that the complete enclosure will close.

## Display integration

The replacement screen initially produced very pixelated output. Getting it working took additional troubleshooting. I no longer remember the exact fix, so no specific resolution, driver, framebuffer setting, or scaling change is claimed here.

The finished-build photographs show the screen displaying a game. They document operation, not a measured image-quality or frame-rate result.

## Power and audio integration

I used a different power supply from the original guide and integrated battery power and audio into the enclosure. Assembly photographs show the battery, wiring, speaker, and amplifier. Exact power-board specifications, battery capacity, current measurements, and runtime are not retained.

## Thermal limitation and the next generation

I overlooked dedicated ventilation in the enclosure and encountered overheating. I did not fix it in this version. That experience informed ventilation changes in my next Raspberry Pi 5 handheld.

No recorded temperature measurements establish a thermal limit, and no controlled test isolates ventilation as the only contributor. Missing ventilation was the design oversight I identified during use.

## Evidence and limits

| Evidence | Supports |
| --- | --- |
| Finished handheld photo | Completed physical assembly and visible game output |
| Assembly photos | Component integration, wiring, and packaging |
| Two Meshmixer project files | Retained enclosure design artifacts |
| My build account | Approximately ten print iterations, pixelation troubleshooting, and overheating |
| Attributed upstream source | Inspectable reference for the guide's input software |

This repository update did not run the handheld, reproduce the display fix, reprint the enclosure, or validate battery and thermal behavior.
