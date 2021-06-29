﻿# HDL Batch installer


[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![project status](https://img.shields.io/badge/Project%20status-Active-00cc22)
[![wxWidgets version](https://img.shields.io/badge/wxWidgets-3.0.5-blue)](https://www.wxwidgets.org/downloads/#v3.0.5)

[![Release HDL Batch Installer](https://github.com/israpps/HDL-Batch-installer/actions/workflows/Repack-and-release.yml/badge.svg)](https://github.com/israpps/HDL-Batch-installer/actions/workflows/Repack-and-release.yml)
[![GitHub release (by tag)](https://img.shields.io/github/downloads/israpps/HDL-Batch-installer/Latest/total?label=Downloads%20%5BLatest%5D)](https://github.com/israpps/HDL-Batch-installer/releases)

#### A GUI for [HDL Dump](https://github.com/israpps/hdl-dump).

 Made by Matias Israelson (AKA:El_isra)

> Originally this was a personal project to practice C++ & give a try to wxWidgets...
>
> But at the end I decided to share it here on github.
When the project gets into a decent state I'll upload it to PSX-place

### Currently implemented features (unchecked elements are WIP)

----

- [x] Install multiple Games at once
- [x] Extract multiple Games at once
- [x] Automatically assign the original Game Title before Installation
- [X] Inject MiniOPL into the game partition (to launch the Game From HDD-OSD)
- [X] Inject MBR.KELF into the HDD
- [ ] Modify Partitions Header (custom title & icon and more)
- [ ] Edit Game Title

---

# Why should I use HDLBinst instead of other programs?

#### The purpose of this GUI is to combine the strengths of each program that serves this same purpose.

So, i´ll going to list it´s strengths compared to other programs:

__Winhiip__  | __HDL Batch Installer__
--------------- | ------------
Limited to __255 games__                            | No limitations (according to uLaunchELF source code: __~`1400` games__ ) 
__Abandoned__ project                               | Project on __active development__ (Even if this GUI Get´s abandoned, you can update HDLDump
Can´t read 1tb/2tb HDDs                             | Up to 2tb HDDs are supported
Only supports DVD5 ISO´s                            | Supports both _DVD5/DVD9_ ISO´s, BIN Images, Nero Images, .iml files and global images
Games without Support for HDD-OSD or PS2BBN         | Games are compatible with HDD-OSD and PS2BBN (if miniOPL Is provided, aka: `boot.kelf`)
__Incompatible__ with uLaunchELF formatted HDDs     | __Compatible__ with uLaunchELF HDD´s (uLe 4.43a 41e4ebe or [4.43x_isr](https://github.com/israpps/wLaunchELF_ISR) are recomended)
Randomly corrupts HDD (or it's MBR program)         | 
__Filename used as game title__                     | original game title __automatically assigned__ from internal database
__Can't hide__ games __from HDD-OSD/PS2BBN__        | Capable of hiding games from HDD-OSD/PS2BBN
***
__HDL Dump Helper GUI__ | __HDL Batch Installer__
------------------- | --------------------
Uses __older hdldump__                             | uses __latest hdldump__ _(automatically updated during release creation)_
__needs Java 32bits__                                 | it's written on C++, so __no dependencies are needed__
Installs games __1 by 1__                              | capable of selecting __multiple Games__, from different paths before installing
HDD must be connected before launching the program | Capable of scanning new HDDs __without restarting program__
User must enter game title __manually for every game__ | __Original game title automatically assigned__ from internal database
__Can't hide games__ from HDD-OSD/PS2BBN               | __Capable of hiding games__ from HDD-OSD/PS2BBN


# Game Name Database:

Just like HDL Batch, this GUI will automatically search the Game Title for the PS2 ISO you're about to Install.

the program has an Internal Database with `14346` Game Titles!

however, you can use an external database Instead.

when the program can't find the Game Title on the Database (or the Database is disabled) the name of the ISO file will be Used Instead (without the extension)

#### If you find a Game ID that isn´t registered in our database Open a new [__Database Update Request__](https://github.com/israpps/HDL-Batch-installer/issues/new?assignees=&labels=Database+issue&template=database-update-request.md&title=Database+update+Request)

## Create Custom Database:


the sintax of the Database entry is:
```Bash
GAME_ID;GAMENAME
```
and the file must end with the line:
```
END_OF_DATABASE
```
the file must be named `gamename.DB`, and it must remain with the Program

a [copy of the internal database](https://github.com/israpps/HDL-Batch-installer/blob/main/Database/gamename.csv) is provided at this repo, (thanks to VTSTech and everyone that contributed to the game title list from PSX-Place)