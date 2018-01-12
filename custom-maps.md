# Custom Maps

Modded CoD4 servers have the ability to run with user created maps.

To run a server with a custom map, it has to first be placed in the `usermaps` folder. In case that folder does not yet exist in your server directory just create it. Just like mods, connecting clients will have to download these maps first before playing them. As the CoD4 servers download speed is quite low, setting up a [fast download server](/fast-download.md) is recommended.

```
├── usermaps
│   ├── mp_nuketown
│   │   ├── mp_nuketown.ff
│   │   ├── mp_nuketown.iwd
│   │   ├── mp_nuketown_load.ff
```

Typically, maps are prefixed by `mp_` following the maps name. 

### Running custom maps on unmodded servers

Running custom maps on unmodded servers is not supported, but there is a neat workaround to still load custom maps. First create a `mods` folder and some empty folder inside it. 

```
├── mods
│   ├── myemptymod

```

Now set `fs_game` to `mods/myemptymod` and you will be able to run custom maps. 

