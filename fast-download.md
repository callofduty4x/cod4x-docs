# Running Mods

To run a mod the servers `fs_game` variable must be set correctly. Mods reside in the `mods` folder inside `fs_homepath`.

Example directory tree:

```
mods/                                  
├── pml220                         
│   ├── mod.ff                         
│   ├── pml220.iwd                     
│   ├── z_c_r.iwd 

```

To start the server with a mod set the `fs_game` variable accordingly.

`./cod4x18_dedrun +set fs_game "pml220"`

