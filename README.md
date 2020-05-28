# Playing Rainbow Six 2: Rogue Spear in 2020 and Beyond

Instructions for playing Rainbow Six 2: Rogue Spear and its expansions. Instructions may also apply to Rainbow Six 1 as they share the same engine.

## Community Resources

* [AllR6 Discord](https://discord.com/invite/QnXXqcK)

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
1. Download the latest release of [`DDrawCompat`](https://github.com/narzoul/DDrawCompat/releases) and place `ddraw.dll` in `C:\Rogue Spear`. This will patch DirectDraw (used by DirectX 6 in-game) to work on modern systems. Since the latest version may change over time, there is a [known-working copy of `ddraw.dll`](ddraw.dll) in this repo as well.
1. Modify both `C:\Rogue Spear\RSConfig.exe` and `C:\Rogue Spear\RogueSpear.exe` to change compatibility settings:
   1. Run this program in compatibility mode for: Windows 98 / Windows Me
   1. Reduced color mode: 16-bit (65536) color
   1. Run this program as an administrator
1. Run `C:\Rogue Spear\RSConfig.exe`. Select your GPU and default audio device, and click OK.
1. Rogue Spear stores its configuration in the Windows registry, and a full configuration file is distributed in this repo. Download [`RogueSpearConfig.reg`](RogueSpearConfig.reg), and edit the config as desired. For example, you may want to change `VideoResolution` from the default (1600x900). If you did not install to `C:\Rogue Spear`, you will need to edit each path in this file.
1. Right-click the config in Windows Explorer, and click `Merge` to apply the config.
1. Run `C:\Rogue Spear\RogueSpear.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.

At this point, you can run the game. The menu system will only run in 640x480 mode. Once you enter a game, the resolution will increase.

To test things out, enter a Terrorist Hunt scenario in the Training mode.

### Urban Operations

Urban Ops is the only expansion which is not a standalone game. It has a shorter install process:

1. Mount the Urban Operations **CUE file** and copy its contents to `C:\tmp`.
1. Modify `C:\tmp\Setup.exe` to use `Windows 98` compatibility mode, and run it. When setup completes, you can delete `C:\tmp`.
1. Install [Urban Operations Patch 2.52](https://www.moddb.com/games/tom-clancys-rainbow-six-rogue-spear/downloads/rogue-spear-urban-operations-252-us-patch)
1. Modify `C:\Rogue Spear\UrbanOperations.exe` to change compatibility settings:
   1. Run this program in compatibility mode for: Windows 98 / Windows Me
   1. Reduced color mode: 16-bit (65536) color
   1. Run this program as an administrator
1. Run `C:\Rogue Spear\UrbanOperations.exe` to start the game, optionally using [Borderless Gaming](https://github.com/Codeusa/Borderless-Gaming/releases) to get a borderless window. The game disc will need to be "mounted" to play the game.

### Black Thorn and Covert Ops

Follow the Rogue Spear steps for these games, since they are standalone expansions. Use `C:\<Expansion>` instead of `C:\Rogue Spear` and edit the registry file before applying to work with BT/CO.

## Playing Online

Rainbow Six and Rogue Spear unfortunately do not support dedicated servers. They originally used third-party MPlayer.com and The Zone (MSN) for peer-to-peer matchmaking. Playing online also requires at least two players to be connected before the game will start.

Some players use Voobly to provide matchmaking similar to MPlayer, but we were not able to get it working in testing. Instead, we decided to host a LAN game and use Hamachi to bridge our local networks. This also allows us to play the expansions, while Voobly only supports the base game.

### Required Setup

1. Open `MP GAME` in the Options menu.
   1. Set your `PLAYER NAME`
   1. Uncheck `BEHIND FIREWALL`
   1. Set `CONNECTION` to `LAN`
1. Open `MP SERVER` in the Options menu.
   1. Set `JOIN PORT` to `2346`
   1. Uncheck `USE PASSWORD`

### Hosting a Game

1. Click `Create Game` in the Multiplayer menu.
1. When prompted by Windows Firewall, be sure to allow traffic on both private and public networks. You can also open Windows Firewall and change the settings for RogueSpear.exe (or expansion equivalent) there.
1. Make sure the game has chosen your desired IP address (e.g. Hamachi). This is particularly important if you have VM or VPN software which creates virtual network interfaces.
1. In the bottom-left, select `PLAYER` if you want to play or `OBSERVER` if you are simply hosting the server.
1. Select the mode, map, options, etc. in the menu.
1. When all players have connected, click the green right arrow to start the game.

### Joining a Game

Click `Manual Join` in the Multiplayer menu and enter the host's Hamachi IP and port `2346`.

## Additional Resources

[Rogue Spear Help Book on Voobly.com](https://www.voobly.com/pages/view/209/www.xcgaming.com/www.xcgaming.com/www.spearstats.com)
