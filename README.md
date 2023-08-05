# arduino-collection

This is a collection of arduino project either created from scratch or heavily customised for my own projects

serial_monitor.ino  

This is a cheap RX serial monitor, this was created referencing various code snippets off the net but using this as a basis (all credits to the original author... https://www.instructables.com/HOW-TO-use-the-ARDUINO-SERIAL-MONITOR/) 

The main changes were:
- changing the speed ie Serial.begin(115200);
- commenting out a lot of the code i didn't need
- adding an if statement to so that it could correctly interpret carriage returns and new lines ie IF ((ByteReceived, HEX) == 'D') and also IF ((ByteReceived, HEX) == 'A')

This fixes an issue where it would keep inserting new lines after every character was received.

On my arduino nano pin 0 = TX, pin 1 = RX (this one), and GND for ground - these are written clearly on the pcb, so shouldn't be too hard to find.

Make sure you have installed and opened the Arduino IDE, plug in the arduino to the pc usb port, then and make sure you have turned on the Serial monitor (in the menu options)
It will display any information received via RX port to support further debugging.
