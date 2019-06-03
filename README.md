"# DSEtutor" 

Arduino development IDE download here: https://www.arduino.cc/en/Main/Software

PlatformIO uses the Microsoft VSCode environment which includes source control and debugging capability.
It is free and available here: https://platformio.org/install/ide?install=vscode

The example program uses a LED / Button board TM1638QY image here: ![GitHub Logo](/IMG_20190603_171809.png)
More board info here: http://we.easyelectronics.ru/part/osobennosti-adresacii-kontrollera-tm1638-dlya-indikatorov-s-oa.html 

Example program uses the TM1638 library, download here: https://github.com/rjbatista/tm1638-library

Information needed to use low cost WAVGAT UNO R3 loard here: https://forum.arduino.cc/index.php?topic=572510.0

A simple application of the button / display module would be to make a calculator. There are plenty of kkeys available for digits and other functions.

A versatile way would be where numbers could be entered onto a stack and then operated on by pressing one of the buttons.

Here is an example implementation of a LIFO stack program: https://www.sanfoundry.com/c-program-stack-implementation/

Tm1638-notes
Keypad 16 button map

Codes are hex values coresponding to button presses
The character symbols represent the button purpose
Arithmatic operators on the left, enter and shift on right.

|0001 '+'	|0002 '7'	|0004 '8'	|0008 '9'|
|0010 '-'	|0020 '4'	|0040 '5'	|0080 '6'|
|0100 'x'	|0200 '1'	|0400 '2'	|0800 '3'|
|1000 '/'	|2000 '0'	|4000 's'	|8000 'e'|

Reverse polish implementation

Numbers are pushed onto a stack, operators perform on numbers on stack leaving result as top value on stack. It would be usual for the operation to remove the numbers operated on. The 'e' button is the enter key, the 's' button will be used for a shift key if additional functions needing more buttons are implemented.

Typical key press and display sequences.

* key	display
* blank
* 1	1
* 2	12
* 3	123
* e	blank
* 4	4
* 5	45
* 6	456
* e	blank
* +	479
