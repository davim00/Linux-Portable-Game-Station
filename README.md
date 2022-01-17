![PortableGameStation](docs/Portable_Game_Station_Banner.png "PortableGameStation")

***

A set of configurations for EmulationStation and RetroArch on Linux that can be installed on a USB or portable hard drive. Forked from the Windows version by HerbFargus ([https://github.com/HerbFargus/Portable-Game-Station](https://github.com/HerbFargus/Portable-Game-Station)).

## Usage

Before you can use EmulationStation, you must place valid ROM files in the roms directory located in the EmulationStation.AppImage.home/.emulationstation directory. The directories inside the roms direcotry are named using EmulationStation's suggested platform names (See "Emulators" [here](https://retropie.org.uk/docs/)).

Run RetroArch first by launching it's appimage located in EmulationStation.AppImage.home/.emulationstation/systems/retroarch. This will generate the necessary configuration folders and files in the RetroArch-Linux.AppImage.home directory located in that same retroarch directory. Configure Retroarch using it's GUI to your tastes, then be sure to quit using the menu so that the configuration is saved.

Launch EmulationStation using one of the bash scripts (Windowed or Fullscreen). It will ask you to configure a controller first. You can configure any X-input (Xbox-compatible) controller or the keyboard. Once completed EmulationStation will load the platform selection screen where you will see the platform(s) for which you have ROMs placed in the roms directory.

## Cores

EmulationStation is preconfigured with selected cores for each system specified in the es_systems.cfg file. You can specify different cores by changing the core name in the ''<command>'' parameter.

## Systems

You can add other platforms and systems by adding them to the es_systems.cfg file. Use the existing parameters as a guide to add new systems. If you want to use other emulators besides RetroArch, place their binaries in their own directories inside the .emulationstationsystems directory. For Linux, is is advised to use self-contained applications such as appimages, for this task. It is also advised to keep the home directory configurations for the emulators with the applications to keep everything portable. For example, if you are using an appimage, you can create a folder alongside the appimage file with the same name as the appimage with ".home" appended to the end. The appimage will use this directory as the appimage's home directory and place all configurations in that folder.

## EmulationStation

The version of EmulationStation included in this project is the forked version from the [Retropie](https://github.com/RetroPie/EmulationStation) project. It it compiled from that source to create the appimage and must be run with it's configurations located in it's home directory. It will fail to launch if the appimage is run by itself, since it is designed to compile as part of a script that generates the necessary resource files to run on a Raspberry Pi. Someday I may look into what needs to be changed so that it will run on it's own, but for now it's just easier to keep it with it's resource files in it's home directory.
