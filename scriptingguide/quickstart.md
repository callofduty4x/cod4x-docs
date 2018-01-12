```
## Quickstart - Running your first script!
```

    In this chapter we develop a small welcome script. It will wait for a player to connect to the server, and write a welcome message to his screen.

    ### Set up your scriptfile
    Inside the serverfolder create a new folder called **main_shared**<sup>[1](#myfootnote1)</sup>. Inside **main_shared** create a file called **welcome.gsc**. This file will contain our code.

    ```C
    init()
    {
        for(;;)
        {
            level waittill("connected", player); // Waits until a new player connects - player stored in "player" variable.
            player thread welcome(); // Execute a new thread for "player".
        }
    }

    welcome()
    {
        // "player" is referenced as "self" now.
        self endon("disconnect"); // If player was connected but left without spawning, thread will lock because of next statement.
        self waittill("spawned_player"); // Waits until the player spawned.
        self iprintlnbold("Welcome " + self.name); // Writes the welcome message bold and centered on the player's screen.
    }
    ```



