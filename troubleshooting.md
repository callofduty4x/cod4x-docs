# Server Troubleshooting

Common problems and how to solve them

#### I have installed some new gsc scripts, now my server does not work

Read qconsole.log and find the error message. Setting the "developer" to "1" will give you better output for debugging.

#### I can't ban anyone

Storing bans is not part of the server. However, plugins do exist for that and are provided with the server download at cod4x.me. Just load the simplebanlist with "loadplugin simplebanlist" on the server console or in your server config to get started.

#### Error: Couldn't resolve\(IPv6\) cod4master.cod4x.ovh

Most likely not an actual error. Your server does not support IPv6. Can be ignored in most cases.

#### CoD4x and Docker

When running the CoD4x \(linux\) server inside a docker container on a windows machine the main and zone folders should not be mounted directly, but be mounted on its parent path. Otherwise the server will fail to load the iwds for some reason.

#### How do I take a screenshot of a player? 

In your server console, type `status`. This will display a list of users that are currently connected to your server. Take the number of the user off of that list, or type their user name into this command.... i.e `getss 3`. Once the command is issued to the server it will save the screenshot of the user under a new folder called `screenshots` in your main server directory. 

#### How do I fix this annoying PunkBuster error?
- Download the PunkBuster [fixed files.](https://github.com/promod/CoD-PunkBuster-Files)
- Click on green button `<> Code` and then click `Download ZIP.`
- Extract the `pb` folder that is inside `.zip file/Call of Duty 4/Windows/pb` 
- Copy the `pb` folder and paste it inside COD4 directory where you installed the game.

#### How do you open the console in game?
- Press the tilde key `( ~ )` that's below `Esc (escape key)` to open the console.
- You can also press `Shift + ( ~ )` to expand the console further.
- If console is not working, go to `Options -> Game Options -> Switch "Enable console" to yes`.
