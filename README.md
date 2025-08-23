# Game-of-Memories

A Game of Life Simulation running inside the memory of an Instructor 50 computer, co-created with Stefan Höltgen in 2014.

These are the original notes from 2014/15 with minor changes to fit the materials uploaded here on GitHub.

## GAME OF MEMORIES

Thomas Nyckel
17.11.15

### 1. UMFANG

Dieses Paket enthält die folgenden Dateien:

Game of Memories.COS
Game of Memories.asm
Readme.txt

### 2. BESCHREIBUNG

Game of Memories ist ein Game of Life nach dem Regelsatz von John Horton Conway. Es wurde für den Emulator des Instructor 50 Microprocessor geschrieben.

Das Besondere an Game of Memories ist, dass das Spielfeld für das Game of Life in einen 16x16 Byte großen Speicherbereich gelegt wurde, den der Emulator graphisch darstellen und so dem Betrachter zugänglich machen kann - wodurch sich der Name des Programms erklärt: Game of Memories.

### 3. GAME OF MEMORIES.COS - DAS AUSFÜHRBARE PROGRAMM

Die Datei Game of Memories.COS kann im Emulator Winarcadia geladen werden. Winarcadia wurde erstellt von James Jacobs und ist unter diesem link downloadbar:

[http://amigan.1emu.net/releases/#amiarcadia](http://amigan.1emu.net/releases/#amiarcadia) (last accessed: 2025-08-23)

WICHTIG: Die Datei Game of Memories.COS wurde mit der Version 22.74 von Winarcadia erstellt. Bei anderen Versionen als Winarcadia 22.74 kommt es mit einiger Wahrscheinlichkeit zu Versionskonflikten. Eine Lösung dieses Problems mag die .asm Datei darstellen:

### 4. GAME OF MEMORIES.ASM - DER CODE MIT KOMMENTAREN

Die Datei Game of Memories.asm enthält ebenfalls den Code in Assembler.
In späteren Versionen von Winarcadia kann diese Datei über die Befehle der CLI direkt eingelesen werden, so dass Versionskonflikte evtl. umgangen werden können.

### 5. HANDHABUNG

Zur Handhabung von Winarcadia im Allgemeinen s. der link oben.

Wenn das Programm in Winarcadia geladen ist, ist das Spielfeld noch nicht zu sehen. Unter der Registerkarte ‚Werkzeuge‘ muss erst der ‚Speichereditor’ aufgerufen werden. Das Spielfeld befindet sich in Speicherbank 0E00-0EFF. Diese muss im Scrolldown-Menü oben links ausgewählt werden.

_Last edit_: 2025-08-23
