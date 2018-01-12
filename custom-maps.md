# Custom Maps

In order to use custom maps, we have to be able to load them through other means. Normally a map is loaded via map mp_<name>. This is fine as stock maps are loaded on every client, but in the case of custom maps, users have to download these files to their local directory in order to play. We can't do this over ATVIs implementation without a mod. 



Easiest solution to this currently is to create an empty mod and create a usermaps folder in your server directory. Once the usermaps folder is created, a sub directory for the map name is required. In the case of a map called Koalaty, mp_koalaty is the folder name and mp_koalaty ff files are inside of that folder.
