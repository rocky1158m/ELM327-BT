There's not much here yet unfortunately :( I do hope to get around to adding some proper documentation at some point. Until that time, I have listed some important bits of information down below.

- This board is designed around the ELM327 v2.1. If you're going to use a newer firmware version, please check the changelog and / or compare its documentation to the v2.1 datasheet to check for compatibility.
- The ELM327**L** is **not** pin-compatible with the ELM327, even though it has the same features in the same package. On the ELM327 (what this board is designed for) pin 6 can be pulled high or low to set the RS232 baud rate on powerup / reset. On the ELM327L there should be a capacitor (10uF tantalum or ceramic with low ESR, less than 5 Ohms) between pin 6 and GND. I recommend you either replace the header with a capacitor footprint in the layout or simply stick a capacitor in the header footprint during production.
- I have done my absolute best to check this design for errors, but haven't gotten around to actually building it. I fully expect it to work, but am unable to assure you it does. I will edit this readme to reflect the results as soon as I or someone else has built this project.
- When selecting a Bluetooth module, pay attention to its voltage levels. This pcb is designed to supply 5V to the module and has a voltage divider in its TX line to communicate at 3V3.