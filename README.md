## Adafruit CAN Pal - CAN Bus Transciever - TJA1051T/3 PCB

<a href="http://www.adafruit.com/products/5708"><img src="assets/5708.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit CAN Pal - CAN Bus Transciever - TJA1051T/3. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5708

### Description

If you'd like to connect a board with native CAN Peripheral support, the Adafruit CAN Pal Transceiver will take the 3V logic level signals and convert them to CAN logic levels with the differential signaling required to communicate. Note that not all chips have a CAN peripheral! Some that we know do have it are the ESP32/ESP32-S2/ESP32-S3 (note that ESP32 calls this interface TWAI not CAN) series of chips, SAME51, STM32F405, or Teensy 4.

Check the product documentation for the board you are wiring this to, to make sure that the chip has CAN support and the RX and TX pins are brought out for you to connect the transceiver to! Despite sharing the 'RX' and 'TX' name with UART, they're not at all the same interface.

CAN Bus is a small-scale networking standard, originally designed for cars and, yes, busses, but is now used for many robotics or sensor networks that need better range and addressing than I2C, and don't have the pins or computational ability to talk on Ethernet. CAN is 2 wire differential, which means it's good for long distances and noisy environments.

Messages are sent at about 1Mbps rate - you set the frequency for the bus and then all 'joiners' must match it, and have an address before the packet so that each node can listen in to messages just for it. New nodes can be attached easily because they just need to connect to the two data lines anywhere in the shared net. Each CAN devices sends messages whenever it wants, and thanks to some clever data encoding, can detect if there's a message collision and retransmit later. 

We've added a few nice extras to this breakout pal to make it useful in many common CAN scenarios:

* TJA1051/T3 can communicate with 3.3V~5V logic for use with modern microcontrollers. 
* 5V charge-pump voltage generator, so even though you are running 3.3V power and logic on most modern microcontroller boards, it will generate a nice clean 5V as required by the transceiver. No separate 5V power required!
* 3.5mm terminal block that can be soldered in to get quick access to the High and Low data lines as well as a ground pin.
* 2 x 60 ohm termination resistor on board (120 ohm in series), you can remove or activate the termination easily by flipping the onboard switch.

Each order comes with an assembled 'pal, terminal block and header. You will need to solder in the header yourself but its a quick task.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
