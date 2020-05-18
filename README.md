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
   1. Modify `<DiscCopy>\Setup.exe` to use `Windows 98` compatibility mode, and run it. It may take a minute or two to reach 100% from 99%. Choose an install location (we'll call it `<YourGameDir>`) and install the game. When setup completes, you can delete the copy of the disc contents from your hard drive.
1. Running Rogue Spear
   1. Download the latest nonexperimental release of [`DDrawCompat`](https://github.com/narzoul/DDrawCompat/releases) and place `ddraw.dll` in `<YourGameDir>`. This will patch DirectDraw (used by DirectX 6 in-game) to work on modern systems.
   1. Modify both `<YourGameDir>\RSConfig.exe` and `<YourGameDir>\RogueSpear.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
   1. Run `<YourGameDir>\RSConfig.exe`. Select your GPU and default audio device, and click OK.
   1. Rogue Spear stores its configuration in the Windows registry, so a registry patch is distributed in this repo. Open [`RogueSpearWindows10.reg`](RogueSpearWindows10.reg) in a text editor and make sure it's using the right directories. The copy in this repo assumes `C:\Rogue Spear`. You may also want to set `VideoResolution` to your desired window size.
   1. Open `regedit` and drag and drop `RogueSpearWindows10.reg` into the `HKEY_LOCAL_MACHINE` directory.
   1. Run `<YourGameDir>\RogueSpear.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.
1. Installing Urban Operations
   1. Mount the Urban Operations CUE file and copy its contents to your drive.
   1. Modify `<DiscCopy>\Setup.exe` to use `Windows 98` compatibility mode, and run it. It may take a long time to reach 100% from 99%. When setup completes, you can delete the copy of the disc contents from your hard drive.
   1. Install [Urban Operations Patch 2.52](https://www.moddb.com/games/tom-clancys-rainbow-six-rogue-spear/downloads/rogue-spear-urban-operations-252-us-patch)
   1. Modify `<YourGameDir>\UrbanOperations.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
   1. Run `<YourGameDir>\UrbanOperations.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.


At this point, you can run the game. The menu system will only run in 640x480 mode. Once you enter a game, the resolution will increase.

To test things out, enter a Terrorist Hunt scenario in the Training mode.

## Playing Online

Playing online requires at least two players to be connected before the game will start.

You can host a game from the multiplayer menu and allow someone to connect to your LAN IP (on port 2346). However, since LAN IPs aren't Internet-accessible, we need to use a third-party service for getting clients to your server.

There are a few options here, such as Voobly (which natively supports Rogue Spear and launches the game for you) and Hamachi (which only allows users to connect to your LAN IP). Voobly only supports Rogue Spear while Hamachi can also support Urban Operations or Black Thorn.

This section will cover the usage of Voobly:

1. Make an account and download the client.
1. Log into the client, scroll down the list of games, and double click Rogue Spear.
1. If prompted, install any updates.
1. In the game lobby, choose an existing server to join.
1. If there are no populated servers, host a server by clicking `Host`.

See also: https://www.voobly.com/pages/view/209/Rogue-Spear-Q--A  
