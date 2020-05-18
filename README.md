# Playing Rogue Spear & Urban Operations in 2020 and Beyond

## Obtaining the Game

The game and expansions can be downloaded from archive.org:

* [Rogue Spear](https://archive.org/details/Tom_Clancys_Rainbow_Six_Rogue_Spear_Version_2.05_Red_Storm_Entertainment_1999)
* [Urban Operations](https://archive.org/details/TomClancysRainbowSixRogueSpearMissionPackUrbanOperationsUSA)
* [Black Thorn](https://archive.org/details/TomClancysRainbowSixRogueSpearBlackThornUSA)

## Installing on Windows 10

1. Installing Rogue Spear
   1. Get some software which can mount BIN/CUE CD images and mount the Rogue Spear BIN file.
   1. Copy the contents of the mounted disc to a folder on your hard drive. If this is skipped, the installer will fail with an "insufficient memory" error.
   1. Modify `<DiscCopy>\Setup.exe` to use `Windows 98` compatibility mode, and run it. It may take a long time to reach 100% from 99%. Choose and install location (we'll call it `<YourGameDir>`), and install the game.
1. Running Rogue Spear
   1. Download the latest nonexperimental release of [`DDrawCompat`](https://github.com/narzoul/DDrawCompat/releases) and place `ddraw.dll` in `<YourGameDir>`. This will patch DirectDraw (used by DirectX 6 in-game) to work on modern systems.
   1. Modify both `<YourGameDir>\RSConfig.exe` and `<YourGameDir>\RogueSpear.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
   1. Run `<YourGameDir>\RSConfig.exe`. Select your GPU and default audio device, and click OK.
   1. Rogue Spear stores its configuration in the Windows registry, so a registry patch is distributed in this repo. Open [`RogueSpearWindows10.reg`](RogueSpearWindows10.reg) in a text editor and make sure it's using the right directories. The copy in this repo assumes `C:\Rogue Spear`. You may also want to set `VideoResolution` to your desired window size.
   1. Open `regedit` and drag and drop `RogueSpearWindows10.reg` into the `HKEY_LOCAL_MACHINE` directory. One of the most important things this file does is set the value of the `FullScreen` key to `FALSE`.
   1. Run `<YourGameDir>\RogueSpear.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.
1. Installing Urban Operations
   1. Mount the Urban Operations CUE file and copy its contents to your drive.
   1. Modify `<DiscCopy>\Setup.exe` to use `Windows 98` compatibility mode, and run it. It may take a long time to reach 100% from 99%.
   1. Install [Urban Operations Patch 2.52](https://www.moddb.com/games/tom-clancys-rainbow-six-rogue-spear/downloads/rogue-spear-urban-operations-252-us-patch)
   1. Modify `<YourGameDir>\UrbanOperations.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
   1. Run `<YourGameDir>\UrbanOperations.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.


At this point, you can run the game. The menu system will only run in 640x480 mode. Once you enter a game, the resolution will increase.

To test things out, enter a Terrorist Hunt scenario in the Training mode.

## Playing Online

In the Multiplayer menu, there are two submenus which still work:

### Manual Join

Paste IP here to join a server.

### Create Game

Starts a local server that you can also play on. Requires port forwarding or a VPN tunnel like Hamachi. Won't let you start game without at least 2 players connected.

### Other: Voobly and Gameranger
