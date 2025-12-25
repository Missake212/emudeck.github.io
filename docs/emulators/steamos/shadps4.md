# shadPS4 is an experimental Sony Playstation 4 Emulator.


Website: [https://shadps4.net/](https://shadps4.net/)

FAQ: [https://shadps4.net/about/faq/](https://shadps4.net/about/faq/)

GitHub: [https://github.com/shadps4-emu/shadPS4](https://github.com/shadps4-emu/shadPS4)

Compatibility List: [https://github.com/shadps4-compatibility/shadps4-game-compatibility/](https://github.com/shadps4-compatibility/shadps4-game-compatibility/)

shadPS4 Wiki: [https://github.com/shadps4-emu/shadPS4/wiki](https://github.com/shadps4-emu/shadPS4/wiki)

***

## shadPS4 Table of Contents

1. [Getting Started with shadPS4](#getting-started-with-shadps4)
    - [Configuration](#shadps4-configuration)
    - [shadPS4 Folder Locations](#shadps4-folder-locations)
    - [How to Update shadPS4](#how-to-update-shadps4)
    - [How to Launch shadPS4 in Desktop Mode](#how-to-launch-shadps4-in-desktop-mode)
    - [File Formats](#shadps4-file-formats)

***

## Getting Started with shadPS4
[Back to the Top](#shadps4-table-of-contents)

In order to play a game on shadPS4, you need to put your game folder in the `Emulation/storage/shadps4/games` folder.

Read the [Configuration](#shadps4-configuration) section to learn more about shadPS4 and its folder locations.

To launch your ROMs in game mode, use Steam ROM Manager and use one of the following parsers to play your Playstation 4 ROMs:

* `ES-DE`
    * To play PS4 games in ES-DE, see [How to Configure shadPS4 to Work With ES-DE and Pegasus](#how-to-configure-shadps4-to-work-with-es-de-and-pegasus)
* `Sony PlayStation 4 - shadPS4 (Shortcut)`
    * Read the [File Formats](#shadps4-file-formats) section to learn more about these various file formats
* `Emulators`

***

### shadPS4 Configuration
[Back to the Top](#shadps4-table-of-contents)

* Type of Emulator: AppImage
* Config Location: `/home/deck/Applications/shadps4-qt.AppImage`
* Storage Location: `Emulation/storage/shadps4/games`
* DLC Location: `Emulation/storage/shadps4/dlc`
* ROM Location: `Emulation/roms/ps4`
* Saves:
    * Folder: `Emulation/saves/shadps4/saves`

* BIOS: You will need firmware modules for some games to work, more information can be found [here](https://github.com/shadps4-emu/shadPS4/wiki/I.-Quick-start-%5BUsers%5D#4-dumping-firmware-modules)

#### Works With
* Steam ROM Manager
* ES-DE
* Pegasus

***

### shadPS4 Folder Locations
[Back to the Top](#shadps4-table-of-contents)

These file locations apply regardless of where you chose to install EmuDeck (to your internal SSD, to your SD Card, or elsewhere). Some emulator configuration files will be located on the internal SSD as listed below.

??? info "The Basics"

    {{ home }}

    {{ emulation }}

    {{ hiddenfolders }}



`~/.config/shadps4`

`~/.local/share/shadps4`

`Emulation/storage/shadps4`

```
shadps4/
└── games
└── dlc
```

***

### How to Update shadPS4
[Back to the Top](#shadps4-table-of-contents)

* Through the `Update your Emulators` section on the `Manage Emulators` page in the `EmuDeck` application
* Through `binupdate.sh` in `Emulation/tools/binupdate`, double click to launch

***

### How to Launch shadPS4 in Desktop Mode
[Back to the Top](#shadps4-table-of-contents)

* Launch `shadPS4 AppImage` from the Applications Launcher (Steam Deck icon in the bottom left of the taskbar)
* Launch the script from `Emulation/tools/launchers`, `shadps4.sh`
* Launch the emulator from `Steam` after adding it via the `Emulators` parser in `Steam ROM Manager`


***

### shadPS4 File Formats
[Back to the Top](#shadps4-table-of-contents)

shadPS4 uses normal folder format for games, simply place your game folder in `Emulation/storage/shadps4/games` to have your games show up in the UI.

***

### How to Configure shadPS4 to Work With ES-DE and Pegasus
[Back to the Top](#shadps4-table-of-contents)

## AppImage

1. In `Desktop Mode`, open shadPS4
2. Skip this step if you have already added your games to shadPS4:
    * Add your game folder to the `Emulation/storage/shadps4/games` folder. For more information, read the [File Formats](#shadps4-file-formats) section
3. Right click your game, click `Create Shortcut`, click `Create Desktop Shortcut`
4. On your desktop, you should see an icon for your game. Move this icon to `Emulation/roms/ps4/shortcuts`
    * If your desktop shortcut contains special icons any special symbols (Ex: the copyright symbol, `©`), rename the desktop file to remove these symbols.
        * For example, rename `God Of War® Collection.desktop` to `God Of War Collection.desktop`, removing the `©` after `War`
5. (Optional) If the desktop file is opening shadPS4 instead of the game:
    * In Desktop Mode, right click the desktop file
    * Click `Properties`
    * On the `General` tab, click `Change` to the right of the `Open With` line
    * Under `Application Preference Order`, click `shadPS4`
    * Click `Remove` on the right
    * Click `Apply` in the bottom left and click `OK`
    * The desktop file will not work in Desktop Mode, but will launch the game directly either through a terminal or through ES-DE
6. Your game should now show up in and launch directly from ES-DE and Pegasus

If you get an `Invalid file or folder` error message, you will need to change the `Alternative Emulator` in ES-DE for PlayStation 4 to `shadPS4 Shortcut [Standalone]`.

On a game, press the `select ` button, scroll down and select `EDIT THIS GAME'S METADATA`, scroll down and select `ALTERNATIVE EMULATOR`, select PS4 and select the corresponding format.

Refer to [https://gitlab.com/es-de/emulationstation-de/-/blob/master/USERGUIDE.md#sony-playstation-4](https://gitlab.com/es-de/emulationstation-de/-/blob/master/USERGUIDE.md#sony-playstation-4), for additional information.

***
