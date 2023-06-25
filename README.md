
![logo](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/ddd4965e-1eef-4c7f-b45d-a95e59e9537a)

<br>

![appleIIvga](https://github.com/Retrotink/Apple-II-VGA/assets/121696513/6de70c4a-55b0-410c-aaee-c455f300293b)
<br>
This project is a VGA card for Apple II computers to output a crisp RGB signal to a VGA monitor instead of having to rely on the composite output. This is accomplished by snooping the 6502 bus and creating a shadow copy of the video memory within a Raspberry Pi Pico, then processing the raw video memory contents to output a "perfect" signal. 
