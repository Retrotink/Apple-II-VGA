
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

## Step 1: The Resistors<br>
![resistor](https://github.com/Retrotink/PockeTerm-II/assets/121696513/01a7b73d-7fd2-4fa3-94ff-4ebca1492b9e)
<br>
Resistors are not polarized so they can be installed either direction. I like to start with the 100ohm resistors and work my way up to the 10K ohm resistors. The gold band is the percentage of accuracy. To read a resistor, start at the opposite side of the gold band.<br>
<br>
47 ohm resistors  - qty 2 - Colors Yellow Violet Black<br>
510 ohm resistors - qty 3 - Colors Green Brown Brown<br>
1K ohm resistors  - qty 6 - Colors Brown Black Red<br>
2K ohm resistors  - qty 3 - Colors Red Black Red<br>
10K ohm resistors - qty 4 - Colors Brown Black Orange<br>
Bend the metal wires at a 90 degree angle on each side of the resistor body.<br>
Place the resistor into the resistor location until it is flush with the PCB. <br>
Turn the board over holding the resistor in its place and bend the wires outward just slightly so the resistor can not back out of the holes. <br>
While the bottom of the board is facing up flat on your workspace, solder each of the two wires on the resistor. <br>
Make sure your solder stays only on the resistor wire and the hole. <br>
Cut the excess lead off the resistor. Repeat this procedure for all of the resistors.<br>
<br>
## Step 2: The Voltage Regulator<br>
![vr](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/2827283f-cf5f-4677-91dc-9fef570002bb)
<br>
Insert the Voltage Regulator and fold it over so it lays flat on its back.<br>
Place the small screw into the top hole and through the board.<br>
Place the nut on the screw on the back of the board and tighten down.<br>
Solder all 3 pins and cut the extra leads short with the board.<br>
<br>
## Step 3: Install the three 20 pin sockets<br>
![socket](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/fdd57e89-5894-406d-9665-edc82d9600fb)<br>
The socket has a notch on one end that matches the PCB.<br>
Place one socket into position and while holding the socket, turn the board over and lay flat on the table.<br>
Hold the board level and solder 1 pin down. Turn the board over and check that the board is flush with the PCB.<br>
If not, apply heat to the pin while pushing the socket flush to the PCB<br>
Solder the remaining pins on the socket and repeat for the other 2 sockets<br>
<br>
## Step 4: Install the 3 .1uF capacitors<br>
![cap 1](https://github.com/Retrotink/PockeTerm-II/assets/121696513/b4f1ca5c-9019-4a8d-b8e1-dcfbb06bebc8)

Install the three .1uF caps into their locations. The caps are labeled 104 and are not polarized so they can be installed either way.<br> 
Fit as flush as possible, bend the 2 wires apart a little so the capacitor does not fall out, turn the board over and set it on your workspace. <br>
Solder the leads onto the PCB and cut away the excess lead length.<br>
<br>
## Step 5: Install the 10uF Electrolytic Capacitor<br>
![cap10](https://github.com/Retrotink/PockeTerm-II/assets/121696513/c7e23a6e-7e4a-4e91-b1af-82b1a7c92350)

## CAUTION: The capacitor is polarized and must be installed correctly. <br>
It is cylinder shaped and both leads protrude from the same side and are labeled 10uF. <br>
There are two ways to tell the + and - leads. <br>
First, looking at the leads, the + is longer than the – lead. <br>
Secondly, there is a large white arrow pointing to the - lead. <br>
Install flush with the PCB and fold it over so it lays between the .1uF cap and the voltage regulator.<br>
Then bend the two leads slightly apart from one another. <br>
Turn the board over and solder onto the PCB. Cut the excess lead on the capacitor.<br>
<br>
## Step 6: Install the Raspberry Pi Pico board<br>
![pico](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/698e874b-df7a-4ea0-a0c4-bccfb4054d1c)
<br>
<br>
## CAUTION: Verify correct orientation before soldering down the Rasperry Pi Pico!<br>
Place the two 20 pin stand offs onto the board.<br>
Then place the Pico onto the stand offs and make sure everything fits flush.<br>
The Pico should be facing with the USB connector towards the VGA connector location.<br>
Solder the 40 pins onto the Pico then hold down the Pico, flip the board and solder the pins to the PCB<br>
<br>
## Step 7: Install the VGA connector<br>
![vga](https://github.com/Retrotink/PockeTerm-II/assets/121696513/09b62c6e-56cd-4fdc-ab0c-45e3034e3894)

The VGA connector has 3 rows of pins. <br>
Insert flush with PCB, turn and solder the inside row first, followed by the outer 2 rows. <br>
Check your work, and then solder the support tabs down.<br>
<br>
## Step 8: Install the 74LVC245 Buffer IC's into the sockets<br>
You will need to pin the pins slightly inwards to align with the sockets.<br>
## CAUTION: Make sure all the IC's are facing towards the Voltage Regulator.<br>
Check for bent pins. Check for missing solder points<br>
<br>
## Solderfest 202/// all Pico chips are preprogrammed for the apple //e and will work on the apple ][ plus<br>
<br>
If you wish to program or update:<br>
1. Press and hold the BOOTSEL button on the Pico while plugging into PC<br>
2. A drive will appear on the PC called RPI-RPI2. Simply drag the *.UF2 firmware file to the RPI drive. <br>
3. The RPI drive will then disappear<br>
4. Remove the cable from the Pico and you can now use the Apple ][ VGA card in your Apple ][


