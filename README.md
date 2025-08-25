# Game-of-Memories

_Game of Memories_ is a Game of Life cellular automaton inside the memory of an emulated _Instructor 50_ computer. It was co-created with Stefan Höltgen in the [Signallabor](https://www.musikundmedien.hu-berlin.de/de/medienwissenschaft/medientheorien/signallabor) at the Humboldt University of Berlin in 2014.

The _Instructor 50_ from Signetics was designed in 1978 for didactic purposes, using the Signetics 2650 microprocessor. The _Instructor 50_ provides no monitor or visual output in the sense we are used to. Containing only a 7-segment display to show addresses and opcodes and a line of eight red LEDs, there is no direct way to actually _see_ the _Game of Memories_ when run on the original hardware. The emulation of this machine in WinArcadia[[1]](#_ftn1), on the other hand, provided the possibility to graphically represent the memory of the emulated machine, rendering the Game of Memories and thereby the inner workings of the computer on the most elemental level of the machine visible.

<img src = "/Pictures/Instructor 50 von Signetics.JPG?raw=true" width = "500" title = "The Instructor 50." alt = "A retro-computer consisting of a black case, two key pads with blue and red keys, a line of 8 DIP-switches and 8 LEDs, and a 7-segment display in red showcasing “HELLO”."/>

_(1) The Instructor 50._

<img src = "/Pictures/Emulator.jpg?raw=true" width = "500" title = "The WinInstructor emulated in WinArcardia." alt = "A window in Windows emulating the Instructor 50, showing in huge red letters the opcodes 03 12 A5 in an 7-segment display in red, 8 red LED below, and a huge amount of smaller buttons and folders surrounding that."/>

_2: The WinInstructor emulated in WinArcardia._

<img src = "/Pictures/GRAFIK_GoM_Speicherfläche mit Okatgon_2.JPG?raw=true" width = "500" title = "The emulator provides us with a graphical representation of the memory bank of the emulated machine where the Game of Memories is playing, here showing an octagon." alt = "A 16 x 16 field of squares coloured in light green. Above the upper column an index is visible froom 0 to F. On the left side the rows are indexed from $0E0x: $ to $0EFx: $. Some squares contain little black circels, together forming an octagon."/>

_3: The emulator provides us with a graphical representation of the memory bank of the emulated machine where the Game of Memories is playing, here showing an octagon._

In the emulator WinArcadia only small parts of the memory with the size 16 x 16 byte could be made visible at a time. Therefore, we were confined to a rather small playing field for the _Game of Memories_ of 16 x 16 cells. It was possible to create most of the common elements from John Horton Conway’s Game of Life like blinkers, beehives, octagons (see above), or gliders (see below). Still, due to the restricted size of the playing field, the cells within our Game of Memories tended to die out or got caught up in repetitive patterns quite fast.

<img src = "/Pictures/Gleiter.jpg?raw=true" width = "475" title = "Three iterations of a glider moving across the playing field." alt = "A retro-computer consisting of a black case, two key pads with blue and red keys, a line of 8 DIP-switches and 8 LEDs, and a 7 segment LED-screen in red showcasing “HELLO”."/>

_Three iterations of a glider moving across the playing field._

<img src = "/Pictures/Hex vs Zeichen.jpg?raw=true" width = "675" title = "WinArcadia made it possible to switch between two different modes for the visualisation of the content of the memory. This enabled us to use the hexadecimal values 17 and 15 to create the impression of empty and filled cells, as it is standard for most cellular automata." alt = "A retro-computer consisting of a black case, two key pads with blue and red keys, a line of 8 DIP-switches and 8 LEDs, and a 7 segment LED-screen in red showcasing “HELLO”."/>

_WinArcadia made it possible to switch between two different modes for the visualisation of the content of the memory. This enabled us to use the hexadecimal values 17 and 15 to create the impression of empty and filled cells, as it is standard for most cellular automata._

<img src = "/Pictures/Schichten-korrekt.jpg?raw=true" width = "1000" title = "The Instructor 50." alt = "A retro-computer consisting of a black case, two key pads with blue and red keys, a line of 8 DIP-switches and 8 LEDs, and a 7 segment LED-screen in red showcasing “HELLO”."/>


## Programmer’s notes

After more than a decade, I do not know if WinArcadia still works same way as we did when we were writing the Game of Memories. asm better than COS, to not be dependend on the version of WinArcadia.

## References

[[1]](#_ftnref1) The WinArcadia Software is available under: [http://amigan.1emu.net/releases/#amiarcadia](http://amigan.1emu.net/releases/#amiarcadia) (last accessed: 2025-08-23).
