# aSysBus - The Arduino System Bus

aSysBus is hard- and software to build a network of arduino nodes using a CAN-bus or other interfaces. Is was build as a replacement for [iSysBus<sup>(DE)</sup>](https://www.mikrocontroller.net/articles/Hausbus_Diskussion), which used native AVR code and a java based configuration framework instead of Arduino. It is mostly used for home automation and other control communication.

Take a look around the wiki to learn more about the protocol, the included examples should help to get you started. If you speak german there are several videos over at [YouTube](https://www.youtube.com/user/adlerweb/search?query=aSysBus).

## Changes of this fork

This fork provides some small refactorings and added comments to provide a more clear understanding of the internals of the library. Also i fixed a few things like missing returns and formatting. The biggest change is a fix of the `ASB_UART::asbReceive` method that was not reading packets containing more that 4 bytes of payload and hanging forever if a packet like this was received. Finally i added the new protocol definition `ASB_CMD_S_LIGHT` for a light node.
