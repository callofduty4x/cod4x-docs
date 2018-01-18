# CoD4x

CoD4x is a community driven project that extends the basic functionality of Call of Duty 4: Modern Warfare. Initially development took place on the server-side with Cod4x 1.7a,which is now deprecated. The current version of CoD4x ,1.8, contains modifications to the base server as well as the client.

## Motivation

It is great that ATVI has provided such an extensive modding framework with Call of Duty 4, but a\) The official masterserver went down multiple times, and was not been fixed for several months in the past, making difficulties for the players. b\) Punkbuster support has been discontinued, which made cheating a huge problem. c\) modders felt limited with the provided functionality.

## CoD4x Server

The CoD4x Server provides basic gameplay which can be extended in several ways

1. Plugins  
   Plugins are the most low level way to extend functionality of the CoD4x Server. Plugins are written in the C Programming language an can communicate with the server core via a Plugin API.

2. Scripting  
   CoD4\(x\) uses the GSC scripting language to define gameplay behaviour. Scripts can be self created and modfied in several ways. More on that in the scripting guide. GSC scripts are solely executed on the server, Clients do not execute GSC scripts.

3. Modding  
   The most traditional way to modify CoD4 is through the Mod Framework. A mod can contain GSC scripts as well as other ressources. You will need a mod whenever you want to change or add ressources on the Client like Menu files, assets, sounds, etc.

## Masterserver

CoD4x is running its own master server. The masterserver is used to communicate running gameservers to the clients. Note that the CoD4x masterserver only lists CoD4x servers of the latest main version \(1.8\). As you might notice while playing, the CoD4x Clients serverbrowser supports both the original ATVI masterserver as well as the CoD4x masterserver.

If you want to check if your server is correctly listed, check out: [http://cod4master.cod4x.me/](http://cod4master.cod4x.me/)

## CoD4x Client

Besides many bugfixes the CoD4x Clients adds several new features for players.

* CoD4x specific master server
* Many cheats are broken
* PBSS like screenshots
* Auto updater
* Steam Integration



