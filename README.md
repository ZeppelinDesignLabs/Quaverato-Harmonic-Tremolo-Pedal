# Quaverato-Harmonic-Tremolo-Pedal
Sketches and compiled software for the Quaverato Harmonic Tremolo pedal.

Release History:
Initial Release, August 13, 2018: v1.1.3

Major Update, December 11, 2018: v2.3.6. Added complete MIDI functionality. Significant improvement to function of RATE knob.

If you need to re-flash the software to your Quaverato, please obtain the free Updater App for PC from our web store, www.zeppelindesignlabs.com. This simple app provides a convenient interface for obtaining and installing all official releases of our software, for all products. Follow the simple installation instructions on the web page, then consult the HELP file inside the app.

To edit, compile and flash customized software is a little more involved. Please follow these instructions:

1. From this repository, download the latest .ino sketch file and all of the wave table files. Place them all together in your sketchbook.
2. Obtain the MiniCore board library from this address:
https://github.com/MCUdude/MiniCore
Use Boards Manager in Arduino to install the MiniCore ATmega 328P board.
3. Obtain the TASK SCHEDULER library from GitHub per directions in the .ino file itself. You also need the MIDI library at https://github.com/FortySevenEffects/arduino_midi_library and the EEPROMex library at https://github.com/thijse/Arduino-EEPROMEx
4. You should now be good to open the .ino file in your favorite editor and hack away.
5. Theoretically, the sketch will compile successfully.
6. Connect your Quaverato to your PC with a USBTiny Programmer. Not all USBTinys are alike. We offer the actual programmer we use in manufacturing our products as an accessory, available on our website. We guarantee that this programmer and its accompanying driver will successfully flash to our products. We cannot guarantee success with other programmers and drivers.

7. Flash the sketch to the pedal. We usually use an independent installation of AVRdUde for this, using this command line: avrdude -c usbtiny -p m328p -V -U flash:w:Quaverato_2.3.6.ino.hex

7a. If your pedal does not have presets saved you can flash the dafaults by placing the quaveratoeeprom.hex file in the same place as your compiled sketch and appending " -U eeprom:w:quaveratoeeprom.hex:i" to the above command line

That's it. Good luck!
