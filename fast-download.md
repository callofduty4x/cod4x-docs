# Fast Download

While players are able to download mods and custom maps of a server without any special configuration, this is only possible with a very limited download speed. Much more effective is the configuration of a fast download http server.

The following settings in your server configuration are necessary:  
`seta sv_wwwDownload "1"                            // enable download redirection`  
`seta sv_wwwBaseURL "http://domain.tld/cod4fastdl/" // defines url to download from`  
`seta sv_wwwDlDisconnected "0"                      // disconnect clients while downloading`

Where `sv_wwwBaseURL` has to point to a URL served by your http server. 

An exaple directory tree for a served folder may look as blow:
```
cod4dl/
├── mods
│   ├── pml220
│   │   ├── mod.ff
│   │   ├── pml220.iwd
│   │   ├── z_c_r.iwd
├── usermaps
│   ├── mp_nuketown
│   │   ├── mp_nuketown.ff
│   │   ├── mp_nuketown.iwd
│   │   ├── mp_nuketown_load.ff
```
