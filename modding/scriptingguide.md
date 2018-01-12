# GSC Scripting Guide

This scripting guide shows how to modify server side scripts on the CoD4x server.





## Stock Scripts >> wip <<
The purpose of this guide is mainly to teach how to write new script files, but obviously each mod and even the stock game already contain tons of scripts. The stock scripts are available [here](https://github.com/D4edalus/CoD4MW/tree/master/raw). The gsc scripts of the stock games and other mods are a great resource to explore the capabilities of gsc scripting. 

### Overriding Scripts >> wip <<
If you have a mod ( or the stock game ) and you want to change the behaviour of its scripts, you can simple override them. The introductory example ( welcome message script ) already showed an example of overriding the `_callbacksetup.gsc` script. `_callbacksetup.gsc` is already present in the stock scripts, and is usually loaded from one of the numerous iwd/ff files in the main/zone folder of your server. However, we can replace the original version by copying the scripts and putting it in the same virtual path as the original file. All paths inside `.iwd`, `.ff` archives and some more special folders are loaded into the same virtual file system root. 

A practical example to clarify the virtual filesystem:
Suppose we have two iwd archives named `main\common_mp.ff` and `main\localized_english_iw07.iwd`. If both of the archives contain the same file they would override eachother. Suppose we want to override `_callbacksetup.gsc`. The original `_callbacksetup.gsc` resides in `common_mp.ff/maps/mp/gametypes/_callbacksetup.gsc`. To override it we can copy its contents ( from [here](https://github.com/D4edalus/CoD4MW/blob/master/raw/maps/mp/gametypes/_callbacksetup.gsc) ) and put it into `zone/localized_english_iw07.iwd/_callbacksetup.gsc`. Since it is tedious to pack scripts into archives each development iteration it is also possible to load scripts from plain folders e.g.: `main_shared/maps/mp/gametypes/_callbacksetup.gsc` to follow the example above.

### Script Locations
In the introductory example we have already learned that scripts can be loaded from the `main_shared` folder. However, there is several more locations that scripts can be loaded from.
- localized_zone07.iwd ( among others, but that one is relevant )
- main_shared
- raw
- raw_shared

if `fs_devdir` is set to `1` also ( note that the devdirs are preferred over the other locations ) :
- dev_raw
- devraw_shared

## Troubleshooting Scripts
#### Server fatal crashed: script compile error unknown function
To see more details on the error set the "developer" variable to "1" on your server. Put `set developer 1` inside your config, or run the server with the commandline argument `+set developer 1`
