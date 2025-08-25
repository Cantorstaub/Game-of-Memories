# Game-of-Memories

_Game of Memories_ is a Game of Life cellular automaton inside the memory of an emulated _Instructor 50_ computer. It was co-created with Stefan Höltgen in the [Signallabor](https://www.musikundmedien.hu-berlin.de/de/medienwissenschaft/medientheorien/signallabor) at the Humboldt University of Berlin in 2014.

The _Instructor 50_ provides no monitor or visual output we are used to. Containing only a 7-segment display to show addresses and opcodes and a line of eight red LEDs, there is no direct way to actually _see_ the _Game of Memories_ when run on the original hardware. The emulation of this machine in WinArcadia[[1]](#_ftn1), on the other hand, provided the possibility to graphically represent the memory of the emulated machine, rendering the _Game of Memories_ and the inner workings of the computer visible.

<img src = "/Pictures/Instructor 50 von Signetics.JPG?raw=true" width = "500" title = "The Instructor 50 from Signetics, designed in 1978 for didactic purposes around the Signetics 2650 microprocessor." alt = "A retro-computer consisting of a black case, two key pads with blue and red keys, a line of 8 DIP-switches and 8 LEDs, and a 7-segment display in red showcasing “HELLO”."/>

_Figure 1. The Instructor 50 from Signetics, designed in 1978 for didactic purposes around the Signetics 2650 microprocessor._

<img src = "/Pictures/Emulator.jpg?raw=true" width = "500" title = "The WinInstructor emulation in WinArcardia." alt = "A window in Windows emulating the Instructor 50, showing in huge red letters the opcodes 03 12 A5 in an 7-segment display in red, 8 red LED below, and a huge amount of smaller buttons and folders surrounding that."/>

_Figure 2. The WinInstructor emulation in WinArcadia._

<img src = "/Pictures/GRAFIK_GoM_Speicherfläche mit Okatgon_2.JPG?raw=true" width = "500" title = "The emulator provided a graphical representation of the memory bank of the emulated machine where the Game of Memories is playing, here showing an octagon." alt = "A 16 x 16 field of squares coloured in light green. Above the upper column, an index is visible from 0 to F. On the left side, the rows are indexed from $0E0x: $ to $0EFx: $. Some squares contain little black circles, forming an octagon."/>

_Figure 3. The emulator provided a graphical representation of the memory bank of the emulated machine where the Game of Memories is playing, here showing an octagon._

Only a small segment of the memory, sized 16 x 16 bytes, could be made visible at a time in WinArcadia. Therefore, we were confined to a relatively small playing field for the _Game of Memories_ of 16 x 16 cells. It was possible to create most of the common elements from John Horton Conway’s Game of Life, like blinkers, beehives, octagons (see figure 3), or gliders (see figure 4). Still, due to the restricted size, the cells within our _Game of Memories_ died out or got caught up in repetitive patterns after a rather small number of generations.

<img src = "/Pictures/Gleiter.jpg?raw=true" width = "475" title = "Three iterations of a glider moving across the playing field." alt = "Three boxes consisting of 4 x 4 green squares. Between the boxes are two arrows pointing from left to right. Within five squares of each box are little circles. The circles have moved to different squares from one box to the other."/>

_Figure 4. Three iterations of a glider moving across the playing field._

## Purpose of the Program

The _Game of Memories_ was designed to study the inner workings of a retrocomputer with much less complexity compared to modern computers. Using the WinArcadia emulator provided the possibility to take up on mediatheoretical thoughts and conclusions in a hands-on fashion by peeking into the emulated machine, in our case, into its memory. Working in Assembler on an emulated machine let us scrutinize the elementary functionalities of the computer down to the single bit. In particular, it facilitated an understanding of the connections between the different strata of computer processes and how _real_ states – to reference the methodological trias of Friedrich A. Kittler – are related to _symbolic_ signs within the machine, opening up avenues to rethink the mediatheoretical stance on programming and processing of digital machines as forms of _writing_.

<img src = "/Pictures/Hex vs Zeichen.jpg?raw=true" width = "675" title = "WinArcadia made it possible to switch between two different modes for the visualisation of the content of the memory. This enabled us to use the hexadecimal values 17 and 15 to create the impression of empty and filled cells, as it is standard for most cellular automata." alt = "Two boxes, each consisting of 4 x 4 gray squares. Each box has a drop-down menu on its right with two options. For the left box, the option “Zeichen” is checked. For the right box, the option “Hexadezimal” is checked. Twelve squares of the left box are empty, and only four squares contain little circles. Twelve squares of the right box contain the value 17, and the same four squares containing the little circles now contain the value 15. Two arrows are depicted between the boxes, one pointing to the right, one to the left."/>

_Figure 5. WinArcadia made it possible to switch between two different modes for the visualisation of the content of the memory. This enabled us to use the hexadecimal values 17 and 15 to create the impression of empty and filled cells, as it is standard for most cellular automata._

<img src = "/Pictures/Schichten-korrekt.jpg?raw=true" width = "1000" title = "The different strata of processes within the emulated Instructor 50." alt = "Two grey areas shaped like hourglasses contain different levels with graphics and text. The lowest level consists of an irregular jigsaw line. Above this, the left hourglass contains the digits 10100101, the right the digits 00010000. The left hourglass then contains A5, the right 10. At the highest level, the left hourglass shows SUBI,r1, the right one 10. On the left of the hourglasses, these levels are indexed from bottom to top with Spannung, Bits, Opcodes (hexadezimal), and Mnemonics."/>

_Figure 6. The different strata of processes within the emulated Instructor 50, ranging from the level of measured voltage up to opcodes and even mnemonics for the human user. The strata are isomorphic to one another and can be read as representing the connection between the real and the symbolic within the machine._

## Programmer’s Notes and Instructions

After more than a decade, I do not know if WinArcadia still works the same way as it did. In 2014, we encountered problems with the emulator: when using a COS-file, it depended on the version of WinArcadia, whether the program would run. This problem might have been entirely due to our lack of experience with the software. Still, if you are going to run the program, it might be advisable to start with the asm-file, which can be loaded directly in higher versions of WinArcadia via the CLI.

When the program is loaded successfully in WinArcadia, the playing field is not yet visible. Under the tab “Werkzeuge”, activate the “Speichereditor.” The playing field is inside memory bank 0E00-0EFF. This bank has to be selected in the scroll-down menu at the top left.

## References

[[1]](#_ftnref1) The WinArcadia Software is available under: [http://amigan.1emu.net/releases/#amiarcadia](http://amigan.1emu.net/releases/#amiarcadia) (last accessed: 2025-08-23).

_Last edit_: 2025-08-25
