FLASH CC253X with ESP based device with MC power

Use How to flash for method to flash the CC253X, you can also use the file named méthode de flash Windows (in french)


Different firmware version:
---------------------------

router-cc253x-std.hex
=====================
The standard firmware without any additional diagnostic messages. You can plug it directly to USB charger (Exemple a phone charger) This firmware don't need any usb connection (No need computer, raspberry, ....)

router-cc253x-diag.hex
======================
The firmware with additional diagnostic messages. This firmware sends the Binary Value report 
for every neighbor in a network. This report looks like:
	
{
description: '28069/0x00158D0001DE7964',
inactiveText: 'PARENT',
presentValue: 6,
relinquish Default: 1,
minimumOffTime: 0
}

Where:

description network and MAC address.
inactive Text device role in a network.
present Value  RSSI value of the last received packet.
relinquish Default (optional)  path depth.
minimumOffTime (optional) number of associated devices.

router-cc2531-diag-usb.hex
=========================
The firmware also sends additional diagnostic messages. But this firmware has USB support inside.
If you connect this USB dongle to a computer, a new virtual COM port will appear. 
The router will also dump diagnostic messages to this port.

router-cc2530-cc2590-xxxxx.hex
=========================
The firmware is compiled for a particular version of the CC2530 board with the additional CC2590/RFX2401 RF chip.

router-cc2530-cc2591-xxxxx.hex
=========================
The firmware is compiled for a particular version of the CC2530 board with the additional CC2591 RF chip.
Note: The CC2591 RF chip is connected to CC2530 through P11 (PAEN), P14 (EN) and P07 (HGM) pins.
This is the generally used layout.

router-cc2530-cc2591-hexin-dl22-xxxxx.hex
=========================
The firmware is compiled for a particular version of the CC2530 board with the additional CC2591 RF chip.
Note: The CC2591 RF chip is connected to CC2530 through P14 (PAEN), P15 (EN) and P07 (HGM) pins. This is the proprietary layout!

router-cc2530-cc2592-xxxxx.hex
=========================
The firmware is compiled for a particular version of the CC2530 board with the additional CC2592 RF chip.


Lights
=========================

Short fast blinks (one per second) The router is connecting to a network.
Short long blinks (one per 4 seconds) Normal operations.
Three short blinks the router cannot send a report to a coordinator.

Pairing
=========================
Flash firmware and permit joining to a network on your coordinator.

Re-pairing
=========================
CC2530: Power on, wait 2 seconds, power off, repeat this cycle three times.
CC2531: Power on, press and hold down the S2 button for 5 seconds.
