# Playing Rogue Spear and Urban Operations in 2020 and Beyond

## Obtaining the Game

The game and expansions can be downloaded from archive.org:

* [Rogue Spear](https://archive.org/details/Tom_Clancys_Rainbow_Six_Rogue_Spear_Version_2.05_Red_Storm_Entertainment_1999)
* [Urban Operations](https://archive.org/details/TomClancysRainbowSixRogueSpearMissionPackUrbanOperationsUSA)
* [Black Thorn](https://archive.org/details/TomClancysRainbowSixRogueSpearBlackThornUSA)

## Installing on Windows 10

1. Get some software which can mount BIN/CUE CD images and mount the Rogue Spear disc.
1. Copy the contents of the mounted disc to a folder on your hard drive. If this is skipped, the installer will fail with an "insufficient memory" error.
1. Modify `Setup.exe` to use the `Windows XP (Service Pack 2)` compatibility mode
1. Run `Setup.exe`, choose and install location (we'll call it `<YourGameDir>`), and install the game.
1. Modify both `<YourGameDir>\RSConfig.exe` and `<YourGameDir>\RogueSpear.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
1. Run `RSConfig.exe`. Select your GPU and default audio device, and click OK.
1. Open [`RogueSpearWindows10.reg`](RogueSpearWindows10.reg) in a text editor and make sure it's using the right directories. The copy in this repo assumes `C:\Rogue Spear`. You may also want to set `VideoResolution` to your desired window size.
1. Open `regedit` and drag and drop `RogueSpearWindows10.reg` into the `HKEY_LOCAL_MACHINE` directory. One of the most important things this file does is set the value of the `FullScreen` key to `FALSE`.
1. Download the latest nonexperimental release of [`DDrawCompat`](https://github.com/narzoul/DDrawCompat/releases) and place `ddraw.dll` in `<YourGameDir>`.
1. Run `<YourGameDir>\RogueSpear.exe` with [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a fullscreen window.

At this point, you can run the game. The main menu is buggy as it can only run in 640x480 mode. Once you enter a game, the resolution will adapt.
