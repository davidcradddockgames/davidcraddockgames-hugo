---
category:
  - gaming
date: "2025-06-03T00:40:14+00:00"
guid: http://www.davidcraddock.games/?p=6
title: 2 player Time Crisis 2 with Sinden Light Gun on PCSX2
url: /time-crisis-2-1-player-sinden

---

This is a work in progress guide that I'm updating to be the 'optimal' way of playing Time Crisis 2 on PC.

The current instructions require a 1080p screen and 2 footpedals, and enable 2 player mode with Sinden light guns.

## Software Required

* Time Crisis 2 (USA version) for PS2 - SLUS-210219

### Sinden Light Gun Utility Patched with support for Patched PCSX2 Emulator

* <a href="https://github.com/nixxou/SindenSoft/releases/tag/V1">Sinden Light Gun Utility</a>

### PCSX2 Emulator patched for Sinden Support

* <a href="https://github.com/nixxou/pcsx2/releases/tag/V1.1">PCSX2 Emulator</a>

### Time Crisis 2 Target Gun Cursors

* <a href="https://mega.nz/folder/IiMzQTzR#yf8BWqult3kILq6dVPp4ZQ">Cursor pack</a>

### Time Crisis 2 HD Retexture Pack (Paetron-supported)

Throw him some money, it's a thankless task!

* <a href="https://gbatemp.net/threads/my-ps2-packs.621422/">https://gbatemp.net/threads/my-ps2-packs.621422/</a>

### Notes

This is for a 40" 1080p monitor/TV. I haven't tested recoil with this setup yet.

#### Joystick mode

Ignore the instructions on the github telling you to put the lightuns in joystick mode. The latest release of the modified sinden lightgun plus PS2 emulator supports raw SDL mapping from the guns themselves, so you don't need to reply on the (broken) less accurate joystick mode.

#### Calibration Trigger

You need to set the bindings for 'Trigger' 'Off screen trigger' and 'Calibration shot' in the PSCX2 emulator to the SAME button you mapped to 'trigger' in the modified lightgun app! This is because of a bug that means sometimes that these three buttons get wrongly assigned. Ignore any other instructions otherwise - this is the only way things will consistently work.

#### COM port

Whenever you reconnect your lightguns the COM ports will change. You need to make a note of these! The best way to do this is to look on the 'Firmware' tab of the modified lightgun settings app. NEVER update using this tab!! Instead just note down the COM port numbers.

#### ROMS

Use this CHD for the game <link>. You will need to use the USA Time Crisis II CHD and make sure the SLUS number matches exactly otherwise the config won't work.

#### BIOS

You will need the official PS2 USA region bios

#### HD Texture Pack

The HD AI upscaled texture pack is available thanks to the efforts of <artist>. Please can you join his Patreon for the download link, or wait until he has one of his free weekends to download it.

#### Crosshairs

There is a bug with the modified PSCX2/lightgun emulator setup in that you can enable two crosshairs, but only one colour will be displayed for both crosshairs. None the less it is extremely useful to have a custom crosshair, and I recommend the crosshair pack mentioned above.


#### 16:9 Widescreen hack

This unfortunately DOES NOT work with this setup. Hopefully it can eventually be made to work, as it would be substantially better.

#### Hacks and patches

Make sure you accept the default hacks and patches in the modified Sinden app, and make sure you have load patches and hacks and cheats ON! Otherwise 2 player will not work.

#### USB setup

Sinden light guns prefer seperate USB root hubs. My computer has a set of USB2 ports and a set of USB3 ports. This means it has two root hubs, one for the USB2 ports and one for the USB3. So I plug one lightgun into the USB2 port and one into the USB3.

The footpedals can be a bit sensitive about USB ports too. There will be a LED on each pedal USB connector so you can make sure that you have a good connection - when it is lit RED then everything is fine.

#### Windows 11 Setup - BEFORE each play!

This is only tested on the latest version of W11. The whole setup has may bugs and is quite 'beta' in a lot of ways - there is a lot of hacking going on behind the scenes! So I suggest these measures:

1) Make sure only the minimum services are running on W11 login. Use the windows task manager and the 'startup apps' tab to turn off anything non-essential.
2) Reboot every time before you start running the game.
3) If you have been using a different Sinden lightgun config app setup, make SURE you go into the MODIFIED lightgun config app and click apply and save on EACH tab EXCEPT the firmware tab! This will ensure that your lightgun is setup with the correct settings for the PSCX2 setup.

#### Multiple monitors/screens

Just don't. Minimise the things that can go wrong by disconnecting any other displays before loading the config.

#### Multiple gaming controllers

Just don't. Minimise the things that can go wrong by disconnecting any non-keyboard and mouse controllers, such as arcade sticks, gamepads etc, before loading the config.

#### Lighting considerations

I play in a dark room with blackout curtains drawn, a pair of electric fans on, and the door closed. Only one screen is on, and that is the main screen. This ensures the lightguns get the best accuracy.

As it will be dark, I recommend you tape down the wires for your footswitches and light guns wherever possible, to avoid trip hazards.

#### Distance from the screen considerations

This is standard for all Sinden setups, but make sure your are positioned with the foot pedals and guns the required distance away from your screen. Look up on the internet the ideal distance you should be from the screen, it depends on how big your screen is.

#### Setup 1: Foot pedals

I use 2 of these cheap but sturdy metal footswitch pedals. They work OK, probably not the best, but the best for the price:
[https://www.amazon.co.uk/dp/B07Z1VDLK1](https://www.amazon.co.uk/dp/B07Z1VDLK1)

When the pedal is depressed it functions like a keypress. You need to set a key that the keypress will activate in the setup utiltity for both foot pedals, obviously pick different keys for each pedal. Make sure you label the pedal for each gun - I have a red sticker on one because I have a red light gun, for example.

For the purposes of the ini file I provide below, I have the following keys mapped:

```
Lightgun 1 "." (period/fullstop)
Lightgun 2 "," (comma)
```

#### Setup 2: Modified Lightgun app

* Make sure you use the UNMODIFIED OFFICAL app ONLY to update the firmware! Otherwise you potentially may brick your lightguns. Make sure you are running the latest firmware available from the 2.07 version of the official lightgun app for this setup.
* Keep the UNMODIFIED OFFICIAL lightgun app seperate, use this modified lightgun app ONLY with PSCX2

Recommended settings for the modified lightgun settings are as follows -

##### Border tab:

No outer border.
2% inner border

##### Lightgun 1 Keybindings:

a,b,c,d,e,f,g etc from the top to bottom for BOTH offscreen and onscreen.

##### Lightgun 2 Keybindings:

0,1,2,3,4,5,.. etc from the top to bottom for BOTH offscreen and onscreen

##### Offset tab:

RESET the offset so the values are

```
0
1
0
1
```

Do not use the manual offset (turn it off)

If you don't get the offset values right then the aiming will be off and it will be a frustrating gaming experience.

#### Setup 3: Modified PSCX2 Emulator

1. Launch the modified PSCX2 Emulator for the first time and run the game. Then close both the game and the emulator.
2. It should have generated a ini file in the inis directory.
3. Open it with notepad. Find each stanza e.g. "[InputSources]" listed in your ini file. Delete each one and replace them with the values below:

```
[InputSources]
Keyboard = true
Mouse = true
SDL = true
DInput = false
XInput = false
SDLControllerEnhancedMode = false
SDLRawInput = true

[USB1]
Type = guncon2
guncon2_cursor_path = ..\..\Crosshairs\Crosshairs\Custom Crosshair Gold.png
guncon2_Gun4IRComPort = 4
guncon2_scale_x = 0
guncon2_Trigger = Keyboard/A
guncon2_ShootOffscreen = Keyboard/A
guncon2_Recalibrate = Keyboard/A
guncon2_A = Keyboard/Period
guncon2_B = Keyboard/F
guncon2_C = Keyboard/E
guncon2_Start = Keyboard/1
guncon2_Select = Keyboard/Q
guncon2_Up = SDL-0/Button27
guncon2_Down = SDL-0/Button28
guncon2_Left = SDL-0/Button29
guncon2_Right = SDL-0/Button30
guncon2_screen_height = 240
guncon2_scale_y = 0
guncon2_custom_config = false

[USB2]
Type = guncon2
guncon2_cursor_path = ..\..\Crosshairs\Crosshairs\Custom Crosshair Green.png
guncon2_Trigger = Keyboard/0
guncon2_A = Keyboard/Comma
guncon2_Select = Keyboard/W
guncon2_ShootOffscreen = Keyboard/0
guncon2_Recalibrate = Keyboard/0
guncon2_B = Keyboard/2
guncon2_C = Keyboard/4
guncon2_Start = Keyboard/2
guncon2_Gun4IRComPort = 5
guncon2_Up = SDL-1/Button27
guncon2_Down = SDL-1/Button28
guncon2_Left = SDL-1/Button29
guncon2_Right = SDL-1/Button30
guncon2_scale_x = 0
guncon2_scale_y = 0
guncon2_custom_config = false
```

4. Replace the COM ports in the ini file with the COM ports corresponding to the COM ports mentioned on the modified sinden 'firmware' app. Note that every time you reconnect the lightguns you will have to look this up again as they may change.
5. Replace the guncon2_cursor_path paths with the custom crosshair you downloaded earlier. Note that due to a bug it will only use two copies of the first one, but set both of them anyway.
6. Launch the emulator and load the PS2 ROM.
7. You should notice that textures cheats and hacks should be loaded, and the game will run. Exit the game.
8. Change the PER GAME settings on the Sinden app for optimal video play. These are the optimal settings, I have a Nvidia 4070 graphics card, 32GB DDR4 RAM and a 12th Gen i7 CPU, so assuming you have a similar setup, these settings will look the best:

```
Internal Resolution: 1080p
Texture Filtering	Bilinear (PS2)
Anisotropic Filtering	16x
Anti-Aliasing (FXAA)	On
Dithering	Off
Blending Accuracy	Basic (raise if issues arise)
Post-Processing Shaders	 Scanlines
```

#### Playing the game

One thing to note is the gun config at the start - what you should do is take the light gun it mentions and shoot the centre of the crosshair from different angles until the custom cursor AND the game cursor line up. When they line up, press the foot pedal for that gun, and that gun is configured.

Now you are finally ready to play the game!



