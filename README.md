# Playing Rainbow Six 2: Rogue Spear in 2020 and Beyond

This README contains instructions for playing Rainbow Six 2: Rogue Spear and its expansions.
Instructions may also apply to Rainbow Six 1 as they share the same engine.
These instructions have been tested on Windows 10 and 11.

## Obtaining the Game

The game and its expansions are no longer available for sale.
Instead, they can be downloaded as torrents from archive.org:

* [Rogue Spear](https://archive.org/details/Tom_Clancys_Rainbow_Six_Rogue_Spear_Version_2.05_Red_Storm_Entertainment_1999)
* [Urban Operations](https://archive.org/details/TomClancysRainbowSixRogueSpearMissionPackUrbanOperationsUSA)
* [Black Thorn](https://archive.org/details/TomClancysRainbowSixRogueSpearBlackThornUSA)
* [Covert Ops Essentials](https://archive.org/details/Tom_Clancys_Rainbow_Six_Covert_Ops_Red_Storm_2000)
  * Note: This is the missions disc. If you're looking for the training disc developed by Magic Lantern Playware, see [here](https://archive.org/details/Rainbow_Six_Covert_Ops_Essentials).

## Installing Rogue Spear on Windows 10 or later

1.  Get some software which can mount BIN/CUE CDROM images, such as [WinCDEmu](https://github.com/sysprogs/WinCDEmu/releases). Mount the Rogue Spear **BIN file**.
2. Copy the contents of the mounted disc to `C:\tmp`. If this is skipped, the installer will fail with an "insufficient memory" error.
3. Modify `C:\tmp\Setup.exe` to use Windows 98 compatibility mode, and run it. **Install the game to `C:\Rogue Spear`**. When prompted by the game, **do not** install DirectX. When setup completes, you can delete `C:\tmp`.
4. Download the latest release of [DDrawCompat](https://github.com/narzoul/DDrawCompat/releases) and place `ddraw.dll` in `C:\Rogue Spear`. This will patch DirectDraw (used by DirectX in-game) to work on modern systems. Version v0.5.1 has been tested and confirmed to work.
5. Modify both `C:\Rogue Spear\RSConfig.exe` and `C:\Rogue Spear\RogueSpear.exe` to change compatibility settings:
   1. Run this program in compatibility mode for: Windows 98 / Windows Me
   2. Reduced color mode: 16-bit (65536) color
   3. Run this program as an administrator
6. Run `C:\Rogue Spear\RSConfig.exe`. Select your GPU and default audio device, and click OK.
7. Rogue Spear stores its configuration in the Windows registry, and a full configuration file is distributed in this repo. Download [RogueSpearConfig.reg](RogueSpearConfig.reg), and edit the config as desired. For example, you may want to change `VideoResolution` from the default (1600x900). If you did not install to `C:\Rogue Spear`, you will need to edit each path in this file.
8. Right-click the config in Windows Explorer, and click `Merge` to apply the config.
9. Run `C:\Rogue Spear\RogueSpear.exe` to start the game. The game disc will need to be "mounted" to play the game.

At this point, you can run the game.
The menu system will only run in 640x480 mode.
Once you enter a game, the resolution will increase.
To test things out, enter a Terrorist Hunt scenario in the Training mode.

## Installing Expansions

As with Rogue Spear, mount the expansion CDROM and run through the setup. If Rogue Spear is already installed, expansions will automatically target `C:\Rogue Spear\mods` during installation.

- For Urban Ops, set compatibility options for `C:\Rogue Spear\UrbanOperations.exe`, and apply configuration from the [UrbanOpsConfig.reg](UrbanOpsConfig.reg) file.
  - Optionally, install [Urban Operations Patch 2.52](https://www.moddb.com/games/tom-clancys-rainbow-six-rogue-spear/downloads/rogue-spear-urban-operations-252-us-patch).
- For Black Thorn, set compatibility options for `C:\Rogue Spear\BlackThorn.exe`, and apply configuration from the [BlackThornConfig.reg](BlackThornConfig.reg) file.
- For Covert Ops, set compatibility options for `C:\Rogue Spear\CovertOperations.exe`, and apply configuration from the [CovertOpsConfig.reg](CovertOpsConfig.reg) file.

## Unlocking All Custom Missions

For a mission to be available in custom mission mode, it must have been completed in campaign mode.
In order to get around this, you can import existing save files which have finished the game, instantly unlocking all maps and missions.

First, back up any existing save files in `C:\Rogue Spear\data\save` and `C:\Rogue Spear\mods\<ModName>\save`.
Then download [RogueSpearSaves.zip](RogueSpearSaves.zip) and extract the contents to your Rogue Spear directory.
This will unlock all missions for Rogue Spear, Urban Operations, and the Classic Missions from Urban Operations.

If desired, you can rename `camp0000.cmp` and the `camp0000` folder to any number to avoid overwriting your existing saves.
Additionally, you can edit `camp0000.cmp` to change the name of the save file (the second line).

## Playing Online

Rainbow Six and Rogue Spear unfortunately do not support dedicated servers.
They originally used third-party MPlayer.com and The Zone (MSN) for peer-to-peer matchmaking. 
Playing online also requires at least two players to be connected before the game will start.

Some players use Voobly to provide matchmaking similar to MPlayer, but we were not able to get it working in testing.
Instead, we decided to host a LAN game and use Hamachi to bridge our local networks.
This also allows us to play the expansions, while Voobly only supports the base game.

#### Required Setup

1. Open `MP GAME` in the Options menu.
   1. Set your `PLAYER NAME`
   2. Uncheck `BEHIND FIREWALL`
   3. Set `CONNECTION` to `LAN`
2. Open `MP SERVER` in the Options menu.
   1. Set `JOIN PORT` to `2346`
   2. Uncheck `USE PASSWORD`

#### Hosting a Game

1. Click `Create Game` in the Multiplayer menu.
2. When prompted by Windows Firewall, be sure to allow traffic on both private and public networks. You can also open Windows Firewall and change the settings for RogueSpear.exe (or expansion equivalent) there.
3. Make sure the game has chosen your desired IP address (e.g. Hamachi). This is particularly important if you have VM or VPN software which creates virtual network interfaces.
4. In the bottom-left, select `PLAYER` if you want to play or `OBSERVER` if you are simply hosting the server.
5. Select the mode, map, options, etc. in the menu.
6. When all players have connected, click the green right arrow to start the game.

#### Joining a Game

Click `Manual Join` in the Multiplayer menu and enter the host's Hamachi IP and port `2346`.

## Community Resources

- [AllR6 Discord](https://discord.com/invite/QnXXqcK)