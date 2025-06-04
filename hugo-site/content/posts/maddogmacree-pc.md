---
category:
  - gaming
date: "2025-06-03T00:40:14+00:00"
guid: http://www.davidcraddock.games/?p=7
title: 2 player Mad Dog Mcree with Sinden Light Gun on PC
url: /mad-dog-mcree-sinden-pc

---

This is how I got Mad Dog Mcree, the 1990 American Laser Game, working with two Sinden light guns.

## Software Required

* Mad Dog Mcree 2 player HD enhanced ROM [https://archive.org/details/hypseus_singe_maddog-hd_2p](https://archive.org/details/hypseus_singe_maddog-hd_2p)

* DirtBagXon's version of hypseus-singe American Laser Game compatible emulator [https://github.com/DirtBagXon/hypseus-singe](https://github.com/DirtBagXon/hypseus-singe) - you will specifically need to download the portable version version '2.11.3'

* Gojidan's bezels for the American Laser Games - [https://github.com/gojidan/hypseus-singe-bezels](https://github.com/gojidan/hypseus-singe-bezels)

* The standard 2.07 beta Sinden light gun utility - I recommend you keep a separate copy dedicated to hypseus-singe games and their config

* The batch file I will list below

### Notes

This is for a 40" 1080p monitor/TV.

#### Manymouse

The `-sinden` flag for hypseus-singe uses 'Manymouse' which allows native windows 11 support for dual mouse mode using the standard Sinden light gun software. This results in very accurate aiming.

#### Bezel

Gojidan provides a great 1080p bezel for hypseus-singe in the repo above. Definitely recommended for the full experience.

#### Rompack

The ROM linked above is a special self-contained compressed rompack format that makes things easier, instead of a large directory structure, and is supported by the version of hypseus-singe linked above

#### hypseus-singe Setup

1. Install hypseus-singe
2. Extract the ROM zip above to the following directory under hypseus-singe root:
```roms\hypseus_singe_maddog-hd_2p```
directory. There should be a further zip file in this directory along with some other files. That zip file contains the video content.
3. Extract the bezels zip and install the mad-dog-mccree bezels in this directory in relation to the hypseus-singe root:
```singe\mad-dog-mccree\```
4. Create a batch file 'MAD DOG.bat' in the hypseus-singe root directory with the following contents:

```
.\hypseus.exe singe vldp -zlua roms\hypseus_singe_maddog-hd_2p\maddog-hd\maddog-hd.zip -framefile roms\hypseus_singe_maddog-hd_2p\maddog-hd\maddog-hd.txt -fullscreen -volume_nonvldp 40 -volume_vldp 50 -bezeldir singe\mad-dog-mccree\1920x1080\ -bezel maddog.png -scanlines -manymouse
```

#### Sinden Lightgun.exe config util setup for hypseus-singe

1. Make sure the firmware is updated to the latest version on both lightguns
2. Make sure joystick mode is turned off on the Main tab
3. Set the control mapping to 'default mouse controls' on BOTH controllers
4. Map the border activation hotkey to 'alt-b'
5. That is all you should need to do, leave everything else as default

#### Further setup

* Create two windows shortcuts, one to the Sinden Lightgun hypseus-singe setup, and one to the ```MAD DOG.bat``` file in the hypseus-singe directory


#### To Play

1. Restart the PC to be on the safe side
2. Run the Sinden Lightgun hypseus-singe shortcut, make sure the lightguns are detected, and turn on the border with 'alt b'
3. Run the MAD DOG.bat shortcut
4. Play the game!


