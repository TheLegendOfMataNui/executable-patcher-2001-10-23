# Executable Patcher 2001-10-23

BIONICLE: The Legend of Mata Nui Executable Patcher for build 2001-10-23


## Overview

Useful for applying patches to BIONICLE: The Legend of Mata Nui build 2001-10-23.

Works with both Python 2 and Python 3.


## Usage

This script modifies the file it is run on, so make sure you make a backup of the file first.

Always run this script on an unmodified copy of the original file as it does not revert patches.

```
usage: patcher.py [-h] [-e ENABLED | -d DISABLED] file

TLOMN Build 2001-10-23 Patcher
Version: 1.17.0

positional arguments:
  file                  File to be patched

optional arguments:
  -h, --help            show this help message and exit
  -e ENABLED, --enabled ENABLED
                        Only apply listed patches
  -d DISABLED, --disabled DISABLED
                        No not apply listed patches

patches:
  dragonmelee           Dragon melee attack fix
  frenchcharacter       Patch character for the French language
  hunaaicontroller      Avoid null pointer error on characters without an AI controller with Huna
  hvp                   Hardward vertex processing
  pausetoggle           Pause double toggle fix
  matoranrgb            Fix RGB values for Onu-Matoran
  pickupsnapping        Patch pick up snapping to disable snapping to terrain
  rockbossdamage        Rock boss always vulnerable and hurt when toa is hurt fix
  rockbosshitpoints     Rock boss hit points crash fix
  rockbossraindeath     Rock boss death by elemental power rain fix
  savequit              Patch to prevent save corrupting save on quit code
  screenres4            Set default screen resolution to 4
  screenresini          Allow ini to control screen resolution
  soundcacheremove      Avoid sound cache use-after-free error by removing on Gc3DSound destructor
  soundtableamount      Avoid SoundTable error message
  win10                 Windows 10
  windbossmovetoa       Wind boss move toa attack and release fix

Copyright (c) 2018-2022 JrMasterModelBuilder
Licensed under the Mozilla Public License, v. 2.0
```

Using `-e` options, you can apply only specific patches.

```bash
./patcher.py -e win10 -e hvp 'LEGO Bionicle.exe'
```

Using `-d` options, you can skip applying specific patches.

```bash
./patcher.py -d screenresini -d screenres4 'LEGO Bionicle.exe'
```


## Bugs

If you find a bug or have compatibility issues, please open a ticket under issues section for this repository.


## License

Copyright (c) 2018-2022 JrMasterModelBuilder

Licensed under the Mozilla Public License, v. 2.0
