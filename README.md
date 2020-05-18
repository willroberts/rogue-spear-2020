# Playing Rainbow Six 2: Rogue Spear in 2020 and Beyond

## Obtaining the Game

The game and expansions are no longer available for sale. Instead, they can be downloaded from archive.org:

* [Rogue Spear](https://archive.org/details/Tom_Clancys_Rainbow_Six_Rogue_Spear_Version_2.05_Red_Storm_Entertainment_1999) (Ctrl-F TORRENT)
* [Urban Operations](https://archive.org/details/TomClancysRainbowSixRogueSpearMissionPackUrbanOperationsUSA) (Ctrl-F ZIP)
* [Black Thorn](https://archive.org/details/TomClancysRainbowSixRogueSpearBlackThornUSA) (Ctrl-F ZIP)
* [Covert Ops Essentials Disc 1](https://archive.org/details/Rainbow_Six_Covert_Ops_Essentials) (Ctrl-F TORRENT)
* [Covert Ops Essentials Disc 2](https://archive.org/details/Tom_Clancys_Rainbow_Six_Covert_Ops_Red_Storm_2000) (Ctrl-F TORRENT)

## Installing on Windows 10

### Rogue Spear

1. Get some software which can mount BIN/CUE CD images (such as PowerISO) and mount the Rogue Spear **BIN file**.
1. Copy the contents of the mounted disc to `C:\tmp`. If this is skipped, the installer will fail with an "insufficient memory" error.
1. Modify `C:\tmp\Setup.exe` to use `Windows 98` compatibility mode, and run it. **Install the game to `C:\Rogue Spear`**. When prompted by the game, **do not** install DirectX 6. When setup completes, you can delete `C:\tmp`.
1. Download the latest nonexperimental release of [`DDrawCompat`](https://github.com/narzoul/DDrawCompat/releases) and place `ddraw.dll` in `C:\Rogue Spear`. This will patch DirectDraw (used by DirectX 6 in-game) to work on modern systems.
1. Modify both `C:\Rogue Spear\RSConfig.exe` and `C:\Rogue Spear\RogueSpear.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
1. Run `C:\Rogue Spear\RSConfig.exe`. Select your GPU and default audio device, and click OK.
1. Rogue Spear stores its configuration in the Windows registry, so a registry patch is distributed in this repo. Download [`RogueSpearWindows10.reg`](RogueSpearWindows10.reg), open it in a text editor, and make sure it's using the right directories. The copy in this repo assumes `C:\Rogue Spear`. You may also want to set `VideoResolution` to your desired window size.
1. Right-click `RogueSpearWindows10.reg` and click `Merge` to apply your config.
1. Run `C:\Rogue Spear\RogueSpear.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.

At this point, you can run the game. The menu system will only run in 640x480 mode. Once you enter a game, the resolution will increase.

To test things out, enter a Terrorist Hunt scenario in the Training mode.

Note: If you are on a laptop which has a trackpad, your mouse may not work. Haven't found a solution for this yet.

### Urban Operations

Urban Ops is the only expansion which is not a standalone game. It has a shorter install process:

1. Mount the Urban Operations **CUE file** and copy its contents to `C:\tmp`.
1. Modify `C:\tmp\Setup.exe` to use `Windows 98` compatibility mode, and run it. When setup completes, you can delete the copy of the disc contents from your hard drive.
1. Install [Urban Operations Patch 2.52](https://www.moddb.com/games/tom-clancys-rainbow-six-rogue-spear/downloads/rogue-spear-urban-operations-252-us-patch)
1. Modify `C:\Rogue Spear\UrbanOperations.exe` to change compatibility settings: Windows 98 mode, 16-bit color, and administrator privileges.
1. Run `C:\Rogue Spear\UrbanOperations.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.

### Black Thorn and Covert Ops

Follow the Rogue Spear steps for these games, since they are standalone expansions.

## Playing Online

Rainbow Six and Rogue Spear unfortunately do not support dedicated servers. They originally used third-party services such as MSNZone, MPlayer.com, and Gamespy Arcade for peer-to-peer matchmaking. Playing online also requires at least two players to be connected before the game will start.

You can host a game from the multiplayer menu and allow someone to connect to your LAN IP (on port 2346). However, since LAN IPs aren't Internet-accessible, we need to use a third-party service for getting clients to your server.

Note: When you host, take note of the IP address in the server lobby chat. Make sure it matches what you expect. It may have bound to the wrong adapter if you have VM or VPN software installed. Alternatively, you can edit the following values in `RogueSpearWindows10.reg`:

```
"MultiplayerPreferredNetworkAddress"="your.local.ethernet.ip"
"MultiplayerUseDefaultNetworkAddress"="FALSE"
```

There are a few options here, such as Voobly (which natively supports Rogue Spear and launches the game for you) and Hamachi (which only allows users to connect to your LAN IP). Voobly only supports Rogue Spear while Hamachi can also support Urban Operations or Black Thorn.

This section will cover the usage of Voobly:

1. Make an account and download the client.
1. Log into the client, scroll down the list of games, and double click Rogue Spear.
1. If prompted, install any updates.
1. In the game lobby, choose an existing server to join.
1. If there are no populated servers, host a server by clicking `Host`.

See also: https://www.voobly.com/pages/view/209/Rogue-Spear-Q--A  
