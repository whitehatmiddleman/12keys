# 12keys Stream Deck
Hand-wired 12 keys macro with Vial firmware

![alt stream-deck][stream-deck]

While browsing for the next keyboard build, I stumbled upon this macro pad from [thingiverse](https://www.thingiverse.com/thing:4186055). I wanted to create a macro pad that would used for streaming but also used for developing and other misc stuff. I decided to use the Vial firmware so I can change the keys and macros on the fly.


## Material
- [3d printed stream deck](https://www.thingiverse.com/thing:4186055)
- 12 Cherry MX switches
- One Pro Micro
- Wires, Female/Male jumper wires

### Optional
- 12 Cherry MX keycaps, if you don't want to print the keycaps
- rubber feet, if you didn't print the non-slip pad which needs TPU material


## Build
Following the [Hand-wiring Guide](https://docs.qmk.fm/#/hand_wire?id=hand-wiring-guide) from the QMK firmware documentation, this is how I wired up the macro pad with the controller.

![alt assembled][assembled]

Primary reason for not permanently soldering the key switches to the controller, is to give the option to change the controller or key switches. I'd like to one day try to put a nice!nano controller.

It is important to wire the controller accordingly, the firmware is coded for the specific pins as the rows and columns:
```c config.h
...
#define MATRIX_ROW_PINS { D4, C6, D7 }
#define MATRIX_COL_PINS { F4, F5, F6, F7 }
...
```

Refer to the [Pro Micro pinout](https://golem.hu/pic/pro_micro_pinout.jpg) for more details. Otherwise make sure you update the matrix row/col pins in the config.h file.


## Vial firmware

Vial firmware is a fork form the QMK firmware, but allows you to use a host gui to change the key mappings on the fly. More about the firmware can be found here: [get.vial.today](https://get.vial.today/)


Clone my firmware:
[https://github.com/greyhatmiddleman/vial-qmk.git](https://github.com/greyhatmiddleman/vial-qmk.git)

```
git clone --recurse-submodules https://github.com/greyhatmiddleman/vial-qmk.git
```

The firmware is located in `keyboards/12keys/keymaps/vial`

**Remember** there is no need to update keymaps.c file, you will be changing your keymaps from the vial application.


### Flashing Firmware

```
qmk flash -kb 12keys -km vial
```

After you've flashed the firmware, install the Vial host gui from [here](https://get.vial.today/download/). For more instructions follow the [first time use guide](https://get.vial.today/manual/first-use.html)

Connect the macro pad, run the application and you should be all set.

![alt vial-app][vial-app]


## Features
- All the cool Vial features!!!

## Troubleshooting
- Make sure your macro pad and connected based on the pin configuration
- Connect the macro pad before running the application, otherwise click on refresh

## Future Improvements
- Use a Nice!Nano controller, but will lose the Vial functionality.
- Add oled to display current layer.

<!-- -->
<div>
<blank>
<a href="https://www.buymeacoffee.com/whmiddleman" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
</blank>
</div>
<!--  -->


<!-- images -->
[stream-deck]: https://raw.githubusercontent.com/greyhatmiddleman/12keys/main/images/3d-printed-stream-desk.jpg
[assembled]: https://raw.githubusercontent.com/greyhatmiddleman/12keys/main/images/assembled.jpg
[open]: https://raw.githubusercontent.com/greyhatmiddleman/12keys/main/images/open-stream-desk.jpg
[vial-app]: https://raw.githubusercontent.com/greyhatmiddleman/12keys/main/images/vial-app.png
