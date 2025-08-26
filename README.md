# Game-of-Memories

_Game of Memories_ is a Game of Life cellular automaton written in assembler. The game plays inside the memory of an _Instructor 50_ computer. It was co-created with Stefan Höltgen at the Humboldt University of Berlin in 2014.[[1]](#_ftn1)

## Concept

The _Instructor 50_ has no monitor or visual output as we are used to. Equipped only with eight red LEDs and a 7-segment display showing addresses and opcodes, the computer offers no direct way to actually see the _Game of Memories_ when run on the original hardware. The emulation of the _Instructor 50_ in WinArcadia[[2]](#_ftn2), on the other hand, provided a graphical representation of its memory, rendering the _Game of Memories_ visible.

<img src = "/Pictures/Instructor 50 von Signetics.JPG?raw=true" width = "500" title = "The Instructor 50 from Signetics, designed in 1978 for didactic purposes around the Signetics 2650 microprocessor." alt = "A retro-computer consisting of a black case, two key pads with blue and red keys, a line of 8 DIP-switches and 8 LEDs, and a 7-segment display in red showcasing “HELLO”."/>

_Figure 1. The Instructor 50 from Signetics, designed in 1978 for didactic purposes around the Signetics 2650 microprocessor._

<img src = "/Pictures/Emulator.jpg?raw=true" width = "500" title = "The WinInstructor emulation in WinArcardia." alt = "A window in Windows emulating the Instructor 50, showing in huge red letters the opcodes 03 12 A5 in an 7-segment display in red, 8 red LED below, and a huge amount of smaller buttons and folders surrounding that."/>

_Figure 2. The WinInstructor emulation of the Instructor 50 in WinArcadia._

<img src = "/Pictures/GRAFIK_GoM_Speicherfläche mit Okatgon_2.JPG?raw=true" width = "500" title = "The emulator provided a graphical representation of the memory bank in which the Game of Memories is playing, here showing an octagon." alt = "A 16 x 16 field of squares coloured in light green. Above the upper column, an index is visible from 0 to F. On the left side, the rows are indexed from $0E0x: $ to $0EFx: $. Some squares contain little black circles, forming an octagon."/>

_Figure 3. The graphical representation of the memory bank in which the Game of Memories is playing, here showing an octagon._

Only a small segment of the memory, sized 16 x 16 bytes, could be made visible at a time in WinArcadia. Therefore, we were confined to a relatively small playing field of 16 x 16 cells for the _Game of Memories_. It was possible to create most of the common elements from John Horton Conway’s Game of Life, like blinkers, beehives, octagons (see figure 3), or gliders (see figure 4). Still, due to the restricted size, the cells within our _Game of Memories_ died out or got caught up in repetitive patterns after a rather small number of generations.

<img src = "/Pictures/Gleiter.jpg?raw=true" width = "475" title = "Three generations of a glider moving across the playing field." alt = "Three boxes consisting of 4 x 4 green squares. Between the boxes are two arrows pointing from left to right. Within five squares of each box are little circles. The circles have moved to different squares from one box to another."/>

_Figure 4. Three generations of a glider moving across the playing field._

## Purpose of the Program

The _Game of Memories_ was designed to study the functionalities of an older computer with much less complexity compared to modern devices. Working in assembler on an emulated machine provided the possibility to scrutinize elementary functionalities down to the single bit in order to take up on mediatheoretical thoughts and conclusions hands-on.[[3]](#_ftn3) In particular, from this project an understanding of the connections between the different strata of computer processes developed, i.e., how _real_ states – to reference the methodological trias of Friedrich A. Kittler[[4]](#_ftn4) – are related to _symbolic_ signs within the machine. This opened up avenues to rethink mediatheoretical stances on programming and processing of digital machines as _writing_.

<img src = "/Pictures/Hex vs Zeichen.jpg?raw=true" width = "675" title = "WinArcadia made it possible to switch between two different modes for the visualisation of the content of the memory. This enabled us to use the hexadecimal values 17 and 15 to create the impression of empty and filled cells, as it is standard for most cellular automata." alt = "Two boxes, each consisting of 4 x 4 gray squares. Each box has a drop-down menu on its right with two options. For the left box, the option “Zeichen” is checked. For the right box, the option “Hexadezimal” is checked. Twelve squares of the left box are empty, and only four squares contain little circles. Twelve squares of the right box contain the value 17, and the same four squares containing the little circles now contain the value 15. Two arrows are depicted between the boxes, one pointing to the right, one to the left."/>

_Figure 5. WinArcadia made it possible to switch between two different modes for the visualisation of the content of the memory. Using the hexadecimal values 17 and 15 created the impression of empty and filled cells, as it is standard for most cellular automata._

<img src = "/Pictures/Schichten-korrekt.jpg?raw=true" width = "1000" title = "The different strata of processes within the emulated Instructor 50." alt = "Two grey areas shaped like hourglasses contain different levels with graphics and text. The lowest level consists of an irregular jigsaw line. Above this, the left hourglass contains the digits 10100101, the right the digits 00010000. The left hourglass then contains A5, the right 10. At the highest level, the left hourglass shows SUBI,r1, the right one 10. On the left of the hourglasses, these levels are indexed from bottom to top with Spannung, Bits, Opcodes (hexadezimal), and Mnemonics."/>

_Figure 6. The different strata of processes within the emulated Instructor 50, ranging from the level of measured voltage up to opcodes and mnemonics for the human user. The strata are isomorphic to one another and can be read as representations of the relations between the real and the symbolic within the machine._

## Programmer’s Notes and Instructions

After more than a decade, I do not know if WinArcadia still works the same way. In 2014, when we were loading the COS file, it depended on the version of WinArcadia whether the program would run. This problem might have been entirely due to our lack of experience with the software. Still, if you are going to run the program, it is advisable to start with the .asm file, which can be loaded directly via the CLI in higher versions of WinArcadia. We were using WinArcadia version 22.74.

When the program is loaded successfully in WinArcadia, the playing field is not yet visible. Under the tab “Werkzeuge”, activate the “Speichereditor.” The playing field is inside memory bank 0E00-0EFF. This bank has to be selected in the scroll-down menu at the top left.

## References

[[1]](#_ftnref1) The _Instructor 50_ was part of the collection of the [Signallabor](https://www.musikundmedien.hu-berlin.de/de/medienwissenschaft/medientheorien/signallabor) run by Stefan Höltgen.

[[2]](#_ftnref2) The WinArcadia Software by James Jacobs is available under: [http://amigan.1emu.net/releases/#amiarcadia](http://amigan.1emu.net/releases/#amiarcadia) (last accessed: 2025-08-23).

[[3]](#_ftnref3) For an example of mediatheoretical thoughts on this topic, see: Nückel, Thomas/Borbach, Christoph (2016): Game of Memories: Zeitschichten in einem zellulären Automaten. In: Höltgen, Stefan/van Treeck, Jan Claas (eds.): _Time to Play: Zeit und Computerspiel_. Game Studies. Glückstadt: Werner Hülsbusch, pp. 70–94. While I am still very fond of Christoph Borbach’s contributions, the conclusions drawn from the _Game of Memories_ by me remained rather underdeveloped in this text.

[[4]](#_ftnref4) For the methodological trias of the real, the symbolic, and the imaginary see Kittler, Friedrich A. (1993): Die Welt des Symbolischen - eine Welt der Maschine. In _Draculas Vermächtnis: Technische Schriften_. First edition. Leipzig: Reclam, pp. 58–80, especially pp. 68–71.

---

_last edit_: 2025-08-26
