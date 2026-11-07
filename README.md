# ButtonPresser
Its a musical thingy
and its super cool, and it will never see the real world but ill make it in KiCAD and even an enclosure, and it will be super cool and super working yes! in all seriousnes it has 5 buttons, a normal ESP32 and a buzzer when you press a button it makes a differently pitcehd sound. m making the PCB in kicad and enclosre in Fusion.

Its powered with a simple 1S LiPo, charging it is on you it doesnt have a charging circuit.

as for flashing the ESP to make it as simple as possible i decided that flashing it would officialy be a 2 to 3 man operation. the flashing will need 3 wires, so you just hold some jumpers on the board plugged into a UART like a CH340 and hope your hand doesnt slip. here is the step by step aswell as where each wire goes. 

Make sure SW6 is on and the battery is unplugged.
Press and hold SW4 (IO9). That’s the boot button.
While holding SW4, plug the battery into J1. The chip starts in download mode.
Release SW4.
Click Upload in the IDE
Unplug the battery and the adapter, then plug the battery back in. The new code runs.

Wire|	PCB end      |CH340 end
1	  |GND	U1 pin 9 |(GND)
2	  |RX	U1 pin 12  |(IO21/TXD)
3	  |TX	U1 pin 11  |(IO20/RXD)
