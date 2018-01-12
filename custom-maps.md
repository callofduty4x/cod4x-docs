# Custom Maps

Modded CoD4 servers have the ability to run with user created maps.

To run a server with a custom map, it has to first be placed in the `usermaps` folder. In case that folder does not yet exist in your server directory just create it. Just like mods, connecting clients will have to download these maps first before playing them. As the CoD4 servers download speed is quite low, setting up a [fast download server](/fast-download.md) is recommended. 





Easiest solution to this currently is to create an empty mod and create a usermaps folder in your server directory. Once the usermaps folder is created, a sub directory for the map name is required. In the case of a map called Koalaty, mp_koalaty is the folder name and mp_koalaty ff files are inside of that folder.

Incases of wanting to keep stats from the base game, set modstats "0" in your config. With this players can keep their current level without having to level up within the mod.
