# Universal CPK Mod Installer

Universal CPK Mod Installer (uCPKmi) is a mod installer made in a .bat script, that simplifies the process of installing mods into games that use CPK files to store data.
It automatically extracts, repacks, and saves a backup of your CPK of choice, so you don't need to be afraid of loosing your game files, or to extract and repack files yourself.


## FAQ
- *How do I use this?*

First, set up the installer by modifying the included configuration file. Change the CPK path, the name, and customize different paths used by the installer if you so desire. Then. put your mods in the mod folder (the one you chose), and they'll be ready for instalation.

- *How do I configure uCPKmi?*

Open the included configuration file (uCPKmi.cfg). You should configure it like this (text between "%%" are comments):
```
[CPK]
CPKPath=%The path to your CPK File% (ex: ".\cpk\". Add the final slash or else it won't work. If the CPK is in the same folder as the tool, leave this blank)
CPKName=%The name of your cpk file% (ex: data.cpk)

[Mods]
ModsDatabase=%Where you want uCPKmi to save a list of currently installed mods% (ex: ".\mods\ModsDB.ini")
ModsFolder=%Where you have your mod folders% (ex: ".\mods")

[uCPKmi]
uCPKmiCacheLocation=%Where you want uCPKmi to save cache% (ex: ".\uCPKmi")
CPKTool=%The CPK extractor you want to use% (ex: ".\CpkTool\PackCPK.exe")
```
The releases of uCPKmi already include PackCPK by Skyth, so you normally don't need to mess around with the cpk tool options. uCPKmi was also made using PackCPK as a base, but you can always try to use different tools to see if they work!

- *How do I make my mods compatible with uCPKmi?*

Set up your mod like this (text between "%%" are comments):
```
%modfolder%\%a folder%\%filesgohere%
%modfolder%\mod.ini
```
The mod folder cannot have any spaces in its name!
You can also pack the mod itself in a CPK file. Just make sure to put it in the path you specify in mod.ini.

Your mod.ini should be setup like this:
```
[Main]
ModFiles=%The path for your mod files inside the mod folder% (ex: "modfiles" or "cpk\data" or "disk\wars_patch")

[Desc]
Title=%The title of your mod%
Description=%The Description of your mod%
Version=%The Version%
Date=%The Date%
Author=%Your Name%
```

## Credits
- PackCPK by Skyth

