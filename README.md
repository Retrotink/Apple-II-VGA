
![logo](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/ddd4965e-1eef-4c7f-b45d-a95e59e9537a)
<br>
# Apple IIe DHR and 80 column being tested now
<br>

![appleIIvga](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/6de70c4a-55b0-410c-aaee-c455f300293b)
<br>
This project is a VGA card for Apple II/II+ computers to output a crisp RGB signal to a VGA monitor instead of having to rely on the composite output. This is accomplished by snooping the 6502 bus and creating a shadow copy of the video memory within a Raspberry Pi Pico, then processing the raw video memory contents to output a "perfect" signal. 
<br>
![installed](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/b7b65cbc-0930-425f-b416-7a6d84813e2b)
<br>
These features are currently supported:<br>
Generates a 640x480@60 VGA signal with 3 bits per color channel using resistor DACs<br>
Text mode (monochrome)<br>
Lo-res mode with no color fringing between the chunky pixels<br>
Hi-res mode with simulated NTSC artifact color<br>
Mixed lo-res and hi-res modes with monochrome text and no color fringing<br>
![screen demo](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/a0ca7209-4e73-4d6d-adb1-44c97370cf58)
<br>
# Acknowledgements

Original design by Mark Aikens. Some minor modifications were made and a board layout made using original PI Pico source code. All parts are through hole for easy assembly. No surface mount components, simple to build.
<br>
<br>

Original design info: https://github.com/markadev/AppleII-VGA
