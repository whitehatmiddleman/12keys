# 12keys Stream Deck (DRAFT)
Hand-wired 12 keys macro with Vial firmware

![alt stream-deck][stream-deck]

While browsing for the next keyboard build, I stumbled upon this macro keyboard in from thinkiverse. I wanted to create a macro pad that would used for recording and streaming but also used for developing and other misc stuff. I decided to use the Vial firmware in this so I can change the keys and macros on the fly.


## Material
- [3d printed stream deck](https://www.thingiverse.com/thing:4186055)
- 12 Cherry MX switches
- One Pro Micro
- Wires, Female/Male jumper wires
- optional
 - 12 Cherry MX keycaps, if you don't want to print the keycaps
 - rubber feet, if you didn't print the non-slip pad which needs TPU material


## Build
Following the [Hand-wiring Guide](https://docs.qmk.fm/#/hand_wire?id=hand-wiring-guide) from the QMK firmware documentation, this is how I wired up the macro keyboard with the controller.

![alt assembled][assembled]

Primary reason for not permanently soldering the key switches to the controller, is to give the option to change the controller or key switches. I'd like to one day try to put a nice!nano controller.


## Vial firmware

Vial firmware is a fork form the QMK firmware, but allows you to use a host gui to change the keymapings on the fly. More about the firmware can be found here: [get.vial.today](https://get.vial.today/)


Clone my firmware:
[https://github.com/greyhatmiddleman/vial-qmk.git](https://github.com/greyhatmiddleman/vial-qmk.git)

```
git clone https://github.com/greyhatmiddleman/vial-qmk.git
```

The firmware is located in ```keyboards/12keys/keymaps/vial```


### Flashing Firmware


## Features


## Troubleshooting


## Future Improvements


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
