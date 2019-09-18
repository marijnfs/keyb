Teensy Keyboard driver (Arduino)
=====================

This is simple USB keyboard driver made for a Teensy board.
It loops over the raster and checks if switches are engaged, builds up a proper HID message and sends it.
It has layer support, to change the keymap when a certain key is pressed.

Define the out_pins and in_pins according to the desired pinout. 
The input pins are set to INPUT_PULLUP, and the output pins to HIGH. 
Then one by one the output pins are set to LOW and the inputs are read, if one read LOW it must be connected.
By repeating this process the keyboard is read out.