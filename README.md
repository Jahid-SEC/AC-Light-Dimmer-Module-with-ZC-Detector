# AC-Light-Dimmer-Module-with-ZC-Detector
Controlling an AC load with an Arduino is simple using either a mechanical relay or a solid-state relay with an optically isolated triac. But dimming an AC lamp is trickier because just limiting current isn’t efficient and creates heat. Instead, dimming is done by phase control—turning the triac on for only part of the AC sine wave, called leading edge cutting.

To do this properly, the Arduino needs to know exactly when the AC wave crosses zero volts. This is done with a zero-crossing detector, usually built with an optocoupler, which gives the Arduino a precise timing signal. The Arduino then waits a set delay after zero crossing to trigger the triac, controlling the lamp’s brightness smoothly.

Another method, Pulse Skip Modulation, switches whole AC cycles on and off but can cause flickering, so it’s less popular. The main parts in the circuit include resistors, a bridge rectifier, a 4N25 optocoupler for zero crossing detection, and a MOC3021 opto-triac to safely trigger the triac.

Keep in mind this only works well with incandescent or halogen bulbs—not most CFL or LED lamps. And very important: because the circuit connects to mains power, proper isolation and safety are a must. Never touch the triac heatsink while powered and always use a proper enclosure.


