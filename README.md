# Release notes
- 07/10/2024 - Added bill of materials list.
- 01/10/2024 - Powajoy added new feature, simulation of popular Sinclair ZX Spectrum+ reset button for ESPectrum emulator. This button emulates the F11 key pressing. Now is coded in pin A4

# Important notes
This version is forked from original by David Carrión (https://github.com/dacarsoft/DB9_2_Keyboard). 

This version only covers PS/2 driver of the original firmware. This firmware was modified to adapt to Arduino Pro Mini ATMEGA 328P 5V 16MHz (not USB support) to be used with [ESPectrum emulator](https://zxespectrum.speccy.org/), but it's possible to adapt to others (See info/ folder to see information about pinout and below to conversion pin-out)

# PowaJoy schematic
This is the schematic to make a Powa-joy. It's a conversor circuit from DB9 (joystick ports) to PS/2 for ESPectrum emulator on ESP32 LilyGo board. This project uses the firmware by David Carrion (DB9_2_Keyboard_ESPectrum - See description below) adapted to ATMEGA 328P micro.

See (schematics/esquema_328P.pdf)

![esquema](https://github.com/user-attachments/assets/bc8a1fcd-7506-4225-851f-bc96acc7a61a)


This fork aims to translate joysticks/pads button presses to keyboard presses by using a generic ATmega 328P boards Arduino Pro Mini, but is possible to integrated on, Arduino UNO, Arduino Micro and Arduino Nano, and others one.

## Bill of material (BOM)
Here I put some of the main materials that you need to ensamble a powaJoy.

- Board to mount components: [Aliexpress link](https://es.aliexpress.com/item/32947192552.html?spm=a2g0o.order_list.order_list_main.30.7005194dVDcJUr&gatewayAdapt=glo2esp)
- Micro-controller Atmega 328p / 5V / 16MHz: [Aliexpress link](https://es.aliexpress.com/item/1005007038272384.html?spm=a2g0o.productlist.main.1.320ahCyKhCyKyW&algo_pvid=003f8394-f396-439e-a2bf-6809a0b090f6&algo_exp_id=003f8394-f396-439e-a2bf-6809a0b090f6-0&pdp_npi=4%40dis%21EUR%214.85%212.09%21%21%2136.83%2115.84%21%402103835e17282555302733990ed667%2112000039179666049%21sea%21ES%21140664060%21X&curPageLogUid=ReXLLefMiLig&utparam-url=scene%3Asearch%7Cquery_from%3A)
- FTDI Programmer (for Atmega 328p): [Aliexpress link](https://es.aliexpress.com/item/1005004496027208.html?spm=a2g0o.productlist.main.1.6f40abb8joER2Q&algo_pvid=1165162a-cf88-4ff2-883c-6b47831655c7&algo_exp_id=1165162a-cf88-4ff2-883c-6b47831655c7-0&pdp_npi=4%40dis%21EUR%212.63%212.63%21%21%212.83%212.83%21%402103917f17282558018317612edc53%2112000033220413809%21sea%21ES%21140664060%21X&curPageLogUid=slVzlI3YE5OL&utparam-url=scene%3Asearch%7Cquery_from%3A)
- DB9 soldier connector: [Aliexpress link](https://es.aliexpress.com/item/4000659356343.html?spm=a2g0o.order_list.order_list_main.55.7005194dVDcJUr&gatewayAdapt=glo2esp)
- (alternative) DB9 plain cable: [Aliexpress link](https://es.aliexpress.com/item/1005003263361996.html?src=google&src=google&albch=shopping&acnt=439-079-4345&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&gclsrc=aw.ds&&albagn=888888&&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=es1005003263361996&ds_e_product_merchant_id=109053355&ds_e_product_country=ES&ds_e_product_language=es&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=21486736708&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gclid=CjwKCAjwoJa2BhBPEiwA0l0ImBg3ZFjG2OL5UcTD8StD5VbtkMc6Du19GT6VhlCzVoEgdV47jWVb2xoCHFIQAvD_BwE)
- (alternative) DB9 screw connector: [Aliexpress link](https://es.aliexpress.com/item/32878536274.html?spm=a2g0o.order_list.order_list_main.35.7005194dVDcJUr&gatewayAdapt=glo2esp)
- Mini-din 6 pins: [Aliexpress link](https://es.aliexpress.com/item/1005007205029726.html?spm=a2g0o.order_list.order_list_main.15.7005194deRnVPS&gatewayAdapt=glo2esp)
- Wire - 24AWG - [Aliexpress link](https://es.aliexpress.com/item/1005006871233984.html?spm=a2g0o.productlist.main.13.73c9d5648UH7MT&algo_pvid=86483ebd-80b9-4acc-b689-5c69af2bfe81&algo_exp_id=86483ebd-80b9-4acc-b689-5c69af2bfe81-36&pdp_npi=4%40dis%21EUR%2110.24%219.59%21%21%2177.81%2172.87%21%40211b612817282559061668373e721d%2112000038578987755%21sea%21ES%21140664060%21X&curPageLogUid=Lpv6ZCeCR7ke&utparam-url=scene%3Asearch%7Cquery_from%3A)
- Connectors (not neccesary. optional)
- Switch for reset feature: [Aliexpress link](https://es.aliexpress.com/item/1005007225726721.html?spm=a2g0o.productlist.main.111.7ade3d0ao6nNmc&algo_pvid=6ac80117-4261-4d03-bd43-9bcfca989772&aem_p4p_detail=202410061608493923290734663100035859130&algo_exp_id=6ac80117-4261-4d03-bd43-9bcfca989772-55&pdp_npi=4%40dis%21EUR%216.49%216.49%21%21%2149.32%2149.32%21%40210390c217282561298786600e1e36%2112000039874208697%21sea%21ES%21140664060%21X&curPageLogUid=UTPZHo4AQYR7&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=202410061608493923290734663100035859130_14)

## <b>Arduino Mini</b>

![image](https://github.com/user-attachments/assets/932ce9b2-a265-4cb4-aad6-31944a4d0395)

See schematic for connection, above.

## <b>Arduino Nano</b>
Pin coversion for Arduino Nano, see below.

Arduino Nano --> Arduino Mini

VCC --> 5V

GND --> GND

LED
- D13 --> PIN 13

SPECTRUM+ RESET BUTTON
- A4 (D18) --> A4

PS/2 (DATA / CLK)
- DATA: D10 --> PIN 10
- CLK:  D12 --> PIN 12
  
PORT 1
- D8  --> PIN 8
- D9  --> PIN 9
- D11 --> PIN 11
- D14  --> A0
- D15  --> A1
- D16  --> A2
- D17  --> A3

PORT 2
- D0 --> PIN 0
- D1 --> PIN 1
- D2 --> PIN 2
- D3 --> PIN 3
- D4 --> PIN 4
- D6 --> PIN 6
- D7 --> PIN 7

![image](https://github.com/user-attachments/assets/04068531-fd36-4ebb-b3d9-fd1ddf13fa01)

## Arduino UNO

Pin coversion for Arduino UNO, see below.

Arduino UNO --> Arduino Mini

VCC --> 5V
GND --> GND

LED
- 13 --> PIN 13

PS/2 (DATA / CLK)
- DATA: PIN 10 --> PIN 10
- CLK:  PIN 12 --> PIN 12

SPECTRUM+ RESET BUTTON
- A4 --> A4
  
PORT 1
- PIN 8  --> PIN 8
- PIN 9  --> PIN 9
- PIN 11 --> PIN 11
- PIN A0  --> A0
- PIN A1  --> A1
- PIN A2  --> A2
- PIN A3  --> A3

PORT 2
- PIN 0 --> PIN 0
- PIN 1 --> PIN 1
- PIN 2 --> PIN 2
- PIN 3 --> PIN 3
- PIN 4 --> PIN 4
- PIN 6 --> PIN 6
- PIN 7 --> PIN 7

![image](https://github.com/user-attachments/assets/31de5cf1-ae49-4bb5-b84b-034643c873c6)


# DB9_2_Keyboard (by David Carrión - Forked by hash6Iron)

Firmware to converts DB9 joysticks button presses to keyboard scancodes through PS/2 port.

This translation is a big help for ESPectrum (official website https://zxespectrum.speccy.org or project repository https://github.com/EremusOne/ZX-ESPectrum-IDF ) with LilyGo board to use conventional 80's DB9 joysticks or compatible DB9 gamepads (wired or not like as 8-bitDO gamepad tested)

The code sends keystrokes when a button is pressed on a joystick. Two simulatenous joysticks are supported. PS/2 keyboard scancodes are sent. The supported joysticks are standard one-two buttons joysticks, Sega three buttons joysticks and Sega 6 buttons joysticks.

The USB detection is done in the first seconds from the boot when the ATmega board is connected to a PS/2 port and powered up. ESPectrum does a negotiation to comunicate with PowaJoy.

The default map for each joystick to execute the translation from joystick buttons is done according to these sequences:


**DB9 PORT 1 (PS/2):**

> CURSOR UP, CURSOR DOWN, CURSOR LEFT, CURSOR RIGHT, RIGHT ALT, ENTER, ESCAPE, F1, Z, Y, X, M

> Q, A, O, P, M, ENTER, ESCAPE, F1, Z, Y, X, C

> CURSOR UP, CURSOR DOWN, CURSOR LEFT, CURSOR RIGHT, ZERO, ENTER, ESCAPE, F5, Z, Y, X, M

> SEVEN, SIX, FIVE, EIGHT, ZERO, ENTER, ESCAPE, F1, Z, Y, X, M


**DB9 PORT 2 (PS/2):**

> Q, A, O, P, M, ENTER, ESCAPE, F1, Z, Y, X, C

> CURSOR UP, CURSOR DOWN, CURSOR LEFT, CURSOR RIGHT, RIGHT ALT, ENTER, ESCAPE, F1, Z, Y, X, M

> CURSOR UP, CURSOR DOWN, CURSOR LEFT, CURSOR RIGHT, ZERO, ENTER, ESCAPE, F5, Z, Y, X, M

> SEVEN, SIX, FIVE, EIGHT, ZERO, ENTER, ESCAPE, F1, Z, Y, X, M


The keymaps can be changed by pressing a direction button (up, down, left, right) while the board is plugged or powered up.


# FLASH INSTRUCTIONS:

Tha Arduino IDE and tools can be used, but to flash easily the firmware on the ATmega 328P this DIY keyboard's updater program can be used also by using the  .HEX file available under the build/PowaJoy folder of the project. 
Flash tools could be downloaded from:

> MAC OS: https://github.com/qmk/qmk_toolbox/releases/download/beta/QMK.Toolbox.app.zip

> WINDOWS: https://github.com/qmk/qmk_toolbox/releases/download/beta/qmk_toolbox.exe

To upload using AVRDUDE - Example:
- avrdude -c arduino -P COM4 -b 115200 -p atmega328p -D -U flash:w:firmware.hex
