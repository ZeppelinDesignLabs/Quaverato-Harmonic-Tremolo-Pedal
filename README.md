# Quaverato-Harmonic-Tremolo-Pedal
Sketches and compiled software for the Quaverato Harmonic Tremolo pedal.

The Quaverato, which shipped initially August 13, 2018, is loaded with software version 1.1.3. You can download the .ino file and edit it in Arduino to your heart's content, compile and flash it back onto your Quaverato. If you manage to trash your pedal, you can always download a fresh copy of the original .hex file and stick it back on.

In late 2018 we expect to release an AutoUpdate App that will super-streamline the process of putting new or revised software on all of our products. Until then, the general procedure consist of the following:

1. From this repository, download the latest .ino sketch file and all of the wave table files. Place them all together in your sketchbook.
2. Using Boards Manager in Arduino, install the MiniCore ATmega 328P board.
3. Obtain the TASK SCHEDULER library from GitHub per directions in the .ino file itself.
4. You should now be good to open the .ino file in your favorite editor and hack away.
5. Theoretically, the sketch will compile successfully.
6. Connect your Quaverato to your PC with a USBTiny Programmer. Not all USBTinys are alike. We offer the actual programmer we use in manufacturing our products as an accessory, available on our website. We guarantee that this programmer and its accompanying driver will successfully flash to our products. We cannot guarantee success with other programmers and drivers.

7. Flash the sketch to the pedal. We usually use an independent installation of AVRdUde for this, using this command line: avrdude -c usbtiny -p m328p -V -U flash:w:Quaverato_2.3.6.ino.hex

7a. If your pedal does not have presets saved you can flash the dafaults by placing the quaveratoeeprom.hex file in the same place as your compiled sketch and appending " -U eeprom:w:quaveratoeeprom.hex:i" to the command line

That's it. Good luck!
