# OpenC64Cart16K
OpenC64Cart16K is an Open Hardware Cartridge for the Commodore 64. It only supports 16 KB ROMs and uses a single (E)EPROM chip. It is the 16 KB counterpart to [OpenC64Cart](https://github.com/SukkoPera/OpenC64Cart).

![Board](https://raw.githubusercontent.com/SukkoPera/OpenC64Cart16K/master/doc/render-top.png)

### Summary
OpenC64Cart16K is designed to accept a 64 KB (512 Kilobit) (E)EPROM with a 27512-style pinout:
![27512 Pinout by Peter Schepers](https://ist.uwaterloo.ca/~schepers/ROMS/PINOUTS/27512.png)

Such chips can hold up to 4 cartridge images, which can be selected by jumpers.

The recommended part is Winbond W27C512 (or W27E512, I don't understand what differences they have), which is widely available, cheap and electrically erasable, which avoids the need for a clunky UV-eraser. This is the only part that was thoroughly tested. Other parts, even smaller in size, will probably work, but will require an ad-hoc configuration.

Usage is straightforward: just insert the EEPROM in the socket making sure that the notch and all pins are aligned, set the jumpers as desired and plug the cartridge in your C64.

### Configuration
**IMPORTANT: ALWAYS TURN YOUR C64 OFF BEFORE MOVING THE CONFIGURATION JUMPERS.**

When flashing the contents, make sure that every file is exactly 16384 bytes long and just concatenate them. If your 16 KB ROM is split into two 8 KB files, concatenate them as well, with the "low" ROM before the "high" ROM.

Then use the following table to set the jumper configuration for your image of choice:

| ROM Image # | A14 | A15 |
|-------------|-----|-----|
| 1           |  L  |  L  |
| 2           |  H  |  L  |
| 3           |  L  |  H  |
| 4           |  H  |  H  |

### License
OpenC64Cart16K is Open Hardware. If you make any modifications to the board, please contribute them back.

### Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay through this link:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/OpenC64Cart16K_V2.html)

You get my gratitude and cheap, professionally-made and good quality PCBs, I get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and yield me some more).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :). But then you can buy me a coffee if you want:

<a href='https://ko-fi.com/L3L0U18L' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi2.png?v=2' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

### Get Help
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).


### Thanks
The following links were useful during the development of this project:
- https://www.c64-wiki.com/wiki/Expansion_Port
- http://blog.worldofjani.com/?p=879
- https://ist.uwaterloo.ca/~schepers/roms.html
- http://smisioto.no-ip.org/elettronica/kicad/kicad.htm
