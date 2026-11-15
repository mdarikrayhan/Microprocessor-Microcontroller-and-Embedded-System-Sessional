# Microprocessor, Microcontroller and Embedded System Sessional

8086 assembly programs for **CSE-4102 Microprocessors, Micro-controllers and Embedded System Sessional**, a lab course in the B.Sc. in CSE at BAUET (Bangladesh Army University of Engineering & Technology), written in 2023. The programs drive an 8×8 green and red LED dot-matrix display, a seven-segment display and LEDs through an 8255 PPI, both on the MDA-8086 trainer kit and in Proteus simulations of an 8086 with an 8255A. [Code Book.docx](Code%20Book.docx) lists the lab problems.

## Contents

### Lab problems ([Dot Matrix and Seven Segment](Dot%20Matrix%20and%20Seven%20Segment))

These programs start at `ORG 1000H` and use the kit's port addresses (18H to 1EH), except problem 7, which uses the Proteus addresses (00H to 06H). The folder also has a Proteus design, `Dot Matrix.pdsprj.pdsprj`.

| Problem | Program | What it does |
| --- | --- | --- |
| 1 | [1_Green_Light_Left_to_Right.asm](Dot%20Matrix%20and%20Seven%20Segment/1_Green_Light_Left_to_Right.asm), [1_Red_Light_Left_to_Right.asm](Dot%20Matrix%20and%20Seven%20Segment/1_Red_Light_Left_to_Right.asm) | Moves a green (or red) line across the dot matrix from left to right |
| 2 | [2_Green_Light_Right_to_Left.asm](Dot%20Matrix%20and%20Seven%20Segment/2_Green_Light_Right_to_Left.asm), [2_Red_Light_Right_to_Left.asm](Dot%20Matrix%20and%20Seven%20Segment/2_Red_Light_Right_to_Left.asm) | The same line, right to left |
| 3 | [3_Green_Light_Up_to_Down.asm](Dot%20Matrix%20and%20Seven%20Segment/3_Green_Light_Up_to_Down.asm), [3_Red_Light_Up_to_Down.asm](Dot%20Matrix%20and%20Seven%20Segment/3_Red_Light_Up_to_Down.asm) | Lights one row at a time from top to bottom |
| 4 | [4_Green_Light_Down_to_Up.asm](Dot%20Matrix%20and%20Seven%20Segment/4_Green_Light_Down_to_Up.asm), [4_Red_Light_Down_to_Up.asm](Dot%20Matrix%20and%20Seven%20Segment/4_Red_Light_Down_to_Up.asm) | Lights one row at a time from bottom to top |
| 5 | [5_Seven_Segment_Display_0_10.asm](Dot%20Matrix%20and%20Seven%20Segment/5_Seven_Segment_Display_0_10.asm) | Counts 0 to 9 on the seven-segment display in a loop |
| 6 | [6_Green_Light_Single_Alphabet.asm](Dot%20Matrix%20and%20Seven%20Segment/6_Green_Light_Single_Alphabet.asm), [6_Red_Light_Single_Alphabet.asm](Dot%20Matrix%20and%20Seven%20Segment/6_Red_Light_Single_Alphabet.asm) | Shows one letter in green (or red) by scanning an 8-byte font column by column |
| Extra | [7_Green_Light_String.asm](Dot%20Matrix%20and%20Seven%20Segment/7_Green_Light_String.asm) | Shows two letters one after the other in green |
| 7 | [8_BAUET_String.asm](Dot%20Matrix%20and%20Seven%20Segment/8_BAUET_String.asm) | Shows the letters of "BAUET" one after another |

### MDA-8086 kit ([MDA-8086 KIT](MDA-8086%20KIT))

| Program | What it does |
| --- | --- |
| [EX-2.asm](MDA-8086%20KIT/EX-2.asm) | A short run of `MOV`, `ADD`, `SUB`, `INC`, `DEC` and `XCHG` instructions ending in `HLT`, for reading the register values on the kit |
| [LED.asm](MDA-8086%20KIT/LED.asm) | Problem 8: blinks the kit's four LEDs |

### Proteus simulations ([Proteus](Proteus))

8086 and 8255A circuits for Proteus. Each `.bin` file is the assembled form of the `.asm` file with the same name.

| Folder | Contents |
| --- | --- |
| [Dot Matrix](Proteus/Dot%20Matrix) | Single letter, "BAUET", and lines moving right to left, left to right, top to bottom and bottom to top (programs at `ORG 0000H`, ports 00H to 06H), with three designs: `Dot Matrix`, `Green_Dot_Matrix` and `Red_Dot_Matrix` |
| [Green & Red Dot Matrix](Proteus/Green%20%26%20Red%20Dot%20Matrix) | The green and red line programs of problems 1 to 4, with their `.bin` files and a design |
| [Seven_Segment_Display](Proteus/Seven_Segment_Display) | The 0 to 9 counter with its `.bin` file and `Seven_Segment_Display.pdsprj` |

### Quiz preparation ([Quiz](Quiz))

[Quiz/Code](Quiz/Code) holds practice versions of the lab programs: a seven-segment counter, an "X" pattern on the dot matrix (`ALPHABATE.asm`, `mycode.asm`), green and red line sweeps, the LED blinker and `EX-2.asm`. [Quiz/PDF](Quiz/PDF) holds scanned lab manual pages, handwritten quiz notes, screenshots of quiz questions and the MDA-Win8086 kit manual.

## Getting started

- **Proteus:** open a `.pdsprj` design in Proteus 8 (the designs were saved with release 8.13). Edit the 8086 component, set **Program File** to the `.bin` you want to run, then start the simulation. Only the `Green & Red Dot Matrix` and `Seven_Segment_Display` designs point at a `.bin` that is in the repo; the others name files that are missing, so set the path yourself.
- **MDA-8086 kit:** the kit programs are assembled for `ORG 1000H`. Load and run them as described in the kit manual, [Quiz/PDF/Full Manual.pdf](Quiz/PDF/Full%20Manual.pdf).
- **Rebuilding a `.bin`:** assemble the `.asm` file as a flat binary with an 8086 assembler.

## Author

Md Arik Rayhan — [mdarikrayhan.com](https://mdarikrayhan.com)

## License

[GNU General Public License v3.0](LICENSE)
