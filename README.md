
<br>![appleIIvga github logo](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/f0ab0489-d28a-4196-acec-dbffe0313f11)
<br>

![appleIIvga](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/6de70c4a-55b0-410c-aaee-c455f300293b)
<br>
This project is a VGA card for Apple II/II+ and //e computers to output a crisp RGB signal to a VGA monitor instead of having to rely on the composite output. This is accomplished by snooping the 6502 bus and creating a shadow copy of the video memory within a Raspberry Pi Pico, then processing the raw video memory contents to output a "perfect" signal. 
<br>
![installed](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/b7b65cbc-0930-425f-b416-7a6d84813e2b)
<br>
These features are currently supported:<br>
Generates a 640x480@60 VGA signal with 3 bits per color channel using resistor DACs<br>
Text mode (monochrome)<br>
Lo-res mode with no color fringing between the chunky pixels<br>
Hi-res mode with simulated NTSC artifact color<br>
Mixed lo-res and hi-res modes with monochrome text and no color fringing<br>
Double hi-res and 80 column mode on the //e only<br>
![screen demo](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/a0ca7209-4e73-4d6d-adb1-44c97370cf58)
<br>

# Acknowledgements

Original design by Mark Aikens. Some minor modifications were made and a board layout made using original PI Pico source code. All parts are through hole for easy assembly. No surface mount components, simple to build.
<br>
<br>

Original design info: https://github.com/markadev/AppleII-VGA

# Soldering the Apple II VGA Card
<br>

Step 1: The Resistors<br>
![resistor](https://github.com/Retrotink/PockeTerm-II/assets/121696513/01a7b73d-7fd2-4fa3-94ff-4ebca1492b9e)
<br>
Resistors are not polarized so they can be installed either direction. I like to start with the 100ohm resistors and work my way up to the 10K ohm resistors. The gold band is the percentage of accuracy. To read a resistor, start at the opposite side of the gold band.<br>
<br>
47 ohm resistors - qty 2 - Colors Yellow Violet Black<br>
510 ohm resistors - qty 3 - Colors Green Brown Brown<br>
1K ohm resistors - qty 6 - Colors Brown Black Red<br>
2K ohm resistors - qty 3 - Colors Red Black Red<br>
10K ohm resistors - qty 4 - Colors Brown Black Orange<br>
<br>
Step 2: The Voltage Regulator<br>
![vr](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/2827283f-cf5f-4677-91dc-9fef570002bb)
