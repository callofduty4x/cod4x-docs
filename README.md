# CoD4x

CoD4x is a community driven project that extends the basic functionality of Call of Duty 4: Modern Warfare. Initially development has started only on the server-side with the by now deprecated version 1.7a. The current version of CoD4x is 1.8 and contains modifications to the base server aswell as the client.

## Motivation

It is great that ATVI has provided such an extensive modding framework with Call of Duty 4, but a\) the official masterserver went down multiple times, and has not been fixed for several months in the past b\) punkbuster support has been discontinued, which made cheating a huge problem. c\) modders felt limited with the provided functionality.

## CoD4x Server

The CoD4x Server provides basic gameplay which can be extended in several ways

1. Plugins
   Plugins are the most low level way to extend functionality of the CoD4x Server. Plugins are write in the C Programming language an can communicate with the server core via a Plugin API. 

2. Scripting  
   CoD4\(x\) uses the GSC scripting language to define gameplay behaviour. Scripts can be self created and modfied in several ways. More on that in the scripting guide. GSC scripts are solely executed on the server, Clients do not execute GSC scripts.

3. Modding  
   The most traditional way to modify CoD4 is through the Mod Framework. A mod can contain GSC scripts as well as other ressources. You will need a mod whenever you want to change or add ressources on the Client like Menu files, assets, sounds, etc.



