# Server Troubleshooting

Common problems and how to solve them

#### I have installed some new gsc scripts, now my server does not work

Read qconsole.log and find the error message. Setting the "developer" to "1" will give you better output for debugging.

#### I can't ban anyone

Storing bans is not part of the server. However, plugins do exist for that and are provided with the server download at cod4x.me. Just load the simplebanlist with "loadplugin simplebanlist" on the server console or in your server config to get started.

#### Error: Couldn't resolve\(IPv6\) cod4master.cod4x.me

Most likely not an actual error. Your server does not support IPv6. Can be ignored in most cases.

#### CoD4x and Docker

When running the CoD4x \(linux\) server inside a docker container on a windows machine the main and zone folders should not be mounted directly, but be mounted on its parent path. Otherwise the server will fail to load the iwds for some reason.

