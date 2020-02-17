# Installation

To play on a CoD4x 1.8+ enabled server, each player is required to use the CoD4x client. The client can be installed in various ways. Typically, you just connect to any CoD4x 1.8+ server and you will be asked to install the client. Choose to just temporarily run the client, or to install the client to your system, and follow the instructions.

## Installing Updates

Updates to the CoD4x Client are provided via an auto-update system. When starting the client check out the main menu, if you see a button saying "Auto update", press it and the update will be installed to your computer.

## Manual Client Installation

If the automated installer is not working for you, the client can still be installed manually. We provide the files to patch your Call of Duty 4 MW client to 1.8 on our website. The files can be [downloaded here](https://cod4x.me/downloads/cod4x_client.zip). After downloading and unpacking the files, make sure your folder structure looks as outlined below.

```
Call of Duty 4 MW
├── cod4x18_v17_9_client <<-- your unpacked folder here
    ├── cod4x_017.dll
    ├── crashrpt1403.dll
    ├── install.cmd   
    ├── uninstall.cmd
    ├── <and some more other files>
├── iw3mp.exe                     
├── miles32.dll
├── mss32.dll
├── <and some more other files and folders>
```

At this point just double-click `install.cmd` to install the CoD4x client files. Finally run your game as usual. On the main menu you will now notice that the games version changed from 1.7 to 1.8.

> Administrative permissions may be required if your game is installed to a protected directory like `C:\Program Files\`

![](/assets/cod4x-client-version.png)

## CoD4x on Mac

A native version of CoD4x is not available for Mac computers. We are sorry for not providing a Mac version of CoD4x, but for the very small audience and our limited resources it is not feasible to support other operating systems natively.

If you still want to run CoD4x on a Mac consider using [Bootcamp](https://support.apple.com/de-at/boot-camp).

## Cod4x Linux Client Installation

Linux can run Cod4x install via Wine to run the windows game client and steam natively. The following are instructions for Ubuntu 19.10 via the terimal. Adjust the commands accordingly per your distro and username and file locations.

1. Run the terminal commands to install the latest version of wine and enable support for 32 bit apps.
```
sudo apt remove winehq-stable wine-stable wine1.6 wine-mono wine-geco winetricks
sudo dpkg --add-architecture i386
wget -qO - https://dl.winehq.org/wine-builds/winehq.key | sudo apt-key add -
sudo apt-add-repository "deb https://dl.winehq.org/wine-builds/ubuntu $(lsb_release -cs) main"
sudo apt update && sudo apt install --install-recommends winehq-stable
```

2. Check the version of wine to make sure it is up to date.
```
wine --version
```

3. Wine will install a hidden c drive directory to mimic the windows file structure: /home/YourUserName/.wine/drive_c/
```
drive_c
├── ProgramData
    ├── <and some more other files>
├── Program Files
    ├── <and some more other files>                     
├── Program Files (x86) <<-- This is where Steam and Call of Duty 4 Modern Warfare will be installed.
    ├── <and some more other files>
├── users
    ├── YourUserName
├── windows
```

4. The latest version of Cod4x has steam support and servers enforce this. Download the windows steam setup executable. Go to your download directory and run it via wine. **NEVER USE ROOT/SUPER USER FOR WINE COMMANDS!**.
```
cd /home/YourUserName/Downloads
wine SteamSetup.exe
```

5. If the steam setup gives you an issue with the steam folder existing already delete it and then continue.
```
cd '/home/YourUserName/.wine/drive_c/Program Files (x86)/'
rm -R Steam
```

6. Your drive_c directory should now have Steam installed.
```
drive_c
├── ProgramData
    ├── <and some more other files>
├── Program Files
    ├── <and some more other files>                     
├── Program Files (x86)
    ├── Steam
        ├── <and some more other files>
    ├── <and some more other files>
├── users
    ├── YourUserName
        ├── <and some more other files>
    ├── <and some more other files>
├── windows
    ├── <and some more other files>
```

7. Go to where your Call of Duty 4 setup is located/mounted and run the setup executable via wine. If you have purchased Call of Duty 4 via Steam skip steps 7-9.
```
cd /media/YourUserName/COD4MW
wine Setup.exe
```

8. Your drive_c directory should now have Call of Duty 4 Modern Warfare installed.
```
drive_c
├── ProgramData
    ├── <and some more other files>
├── Program Files
    ├── <and some more other files>                     
├── Program Files (x86)
    ├── Activision
        ├── Call of Duty 4 - Modern Warfare
            ├── <and some more other files>      
    ├── Steam
        ├── <and some more other files>
    ├── <and some more other files>
├── users
    ├── YourUserName
        ├── <and some more other files>
    ├── <and some more other files>
├── windows
    ├── <and some more other files>
```

8. Download and install the official Call of Duty 4 Modern Warfare 1.6 Patch and run the setup via wine. **It might hang for 10 minutes just be patient and wait**.
```
cd /home/YourUserName/Downloads
wine cod4mw-1.6-patchsetup.exe
```

9. Download and install the official Call of Duty 4 Modern Warfare 1.7 Patch and run the setup via wine.
```
cd /home/YourUserName/Downloads
wine cod4mw-1.7-patchsetup.exe
```

10. To play on a CoD4x 1.8+ enabled server, each player is required to use the CoD4x client. The client can be installed in various ways. Typically, you just run the non Cod4x 1.8 client via wine and connect to any CoD4x 1.8+ server and you will be asked to install the client. 
```
cd '/home/YourUserName/.wine/drive_c/Program Files (x86)/Activision/Call of Duty 4 - Modern Warfare'
wine iw3mp.exe
```

11. If the automated installer is not working for you because of steam not running, the client can still be installed manually. We provide the files to patch your Call of Duty 4 MW client to 1.8 on our website. The files can be [downloaded here](https://cod4x.me/downloads/cod4x_client.zip). After downloading and unpacking the files, make sure your folder structure looks as outlined below (if installed via steam locate where it is installed).
```
drive_c
├── ProgramData
    ├── <and some more other files>
├── Program Files
    ├── <and some more other files>                     
├── Program Files (x86)
    ├── Activision
        ├── Call of Duty 4 - Modern Warfare      
            |── cod4x18_v17_9_client <<-- your unpacked folder here
                ├── cod4x_017.dll
                ├── crashrpt1403.dll
                ├── install.cmd   
                ├── uninstall.cmd
                ├── <and some more other files>
            ├── iw3mp.exe                     
            ├── miles32.dll
            ├── mss32.dll
            ├── <and some more other files and folders>
    ├── Steam
        ├── <and some more other files>
    ├── <and some more other files>
├── users
    ├── YourUserName
        ├── <and some more other files>
    ├── <and some more other files>
├── windows
    ├── <and some more other files>
```

Go to your cod4x18_v17_9_client folder directory and run the install.cmd script using the command interpreter with wine.
```
cd '/home/YourUserName/.wine/drive_c/Program Files (x86)/Activision/Call of Duty 4 - Modern Warfare/cod4x18_v17_9_client'
wine cmd.exe /C install.cmd
```

If the install.cmd script executed correctly you should see the cod4x_017 folder and files in "/home/YourUserName/.wine/drive_c/users/YourUserName/Local Settings/Application Data/CallofDuty4MW/bin/cod4x_017" 
```
drive_c
├── ProgramData
    ├── <and some more other files>
├── Program Files
    ├── <and some more other files>                     
├── Program Files (x86)
    ├── Activision
        ├── Call of Duty 4 - Modern Warfare      
            |── cod4x18_v17_9_client <<-- your unpacked folder here
                ├── cod4x_017.dll
                ├── crashrpt1403.dll
                ├── install.cmd   
                ├── uninstall.cmd
                ├── <and some more other files>
            ├── iw3mp.exe                     
            ├── miles32.dll
            ├── mss32.dll
            ├── <and some more other files and folders>
    ├── Steam
        ├── <and some more other files>
    ├── <and some more other files>
├── users
    ├── YourUserName
        ├── Local Settings
            ├── Application Data
                ├── CallofDuty4MW
                    ├── bin 
                        ├── cod4x_017 <<-- your generated install.cmd folder here
                            ├── cod4x_017.dll
                            ├── install.cmd
                            ├── uninstall.cmd
                            ├── <and some more other files>
                        ├── iw3mp.exe
                    ├── <and some more other files>
                ├── <and some more other files>
            ├── <and some more other files>
        ├── <and some more other files>
    ├── <and some more other files>
├── windows
    ├── <and some more other files>
```

12. Run Steam via wine using special arguments -no-cef-sandbox. **They must be used or steam's web forms wont load.**. Log into your steam account name. If you do have one create one. Servers will kick you if you are not running the CoD4x client through steam. Your Steam page name will be used when joining servers which is different from your steam account name. This can be changed at any time so name your steam account name anything.
```
cd '/home/YourUserName/.wine/drive_c/Program Files (x86)/Steam'
wine Steam.exe -no-cef-sandbox
```

13. If you have purchased Call of Duty 4 via Steam skip this step. Click on the top menu **Games** -> **Add a Non-Steam Game To My Library**. Call of Duty 4 Modern Warfare Single Player and Multiplayer should show up. Check them both and click **Add Selected Programs**.

14. Click on the top menu **Games** -> **Vew Games Library**. Click on Call of Duty 4 Modern Warfare Multiplayer and click the big green Play button. You should see the steam overlow show up in the bottom right corner as well as the number 17.9. Join a server and play. If you see an error like below its because the user application data files are not in the right directory and you need to place them there manually via the install.cmd script or by joining a server with the latest patch.
```
Error loading Cod4X
Failed to load CoD4X because file cod4x_xxx.dll or entry point was not found. Attempting to load Cod4 v1.7
OK
```
