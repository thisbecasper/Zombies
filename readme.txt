NetLauncher for EDuke32-OldMP
By: Striker

This utility was made to allow players to set up EDuke32-OldMP matches easily and connect via IP or the "netlaunch://" URL protocol (Windows only ATM).

------------
Instructions
------------
Installation:
- Extract this zip anywhere you like, then put duke3d.grp and duke.rts in the same folder.

NOTE: If you have DiscordLauncher.exe, DiscordLauncher-linux64, and LANLauncher.bat in your destination directory, delete them. They're outdated.

HOSTING:
- Run NetLauncher

- Hit the number for "Host Game" in the main menu to host a new lobby.

- Set player count/fraglimit/mods according to the launcher.

- Wait for the launcher to grab your IP and attempt UPnP port forward (if enabled).

- Once the lobby is up, send the IP address shown to the players you want to join.
  * Alternatively, if everyone has already used netlauncher at least once, you can
    send the other players a protocol link, formatted as: netlaunch://127.0.0.1/
    (replacing the example with your IP address). This will launch the program directly.
  * If sending the protocol URL via Discord, encase it in pointed brackets, ie: <netlaunch://127.0.0.1/>
  
- Wait for people to join. Game will start when player count is hit, or you press Y.

JOINING:
- Run NetLauncher

- Hit the number for "Join via IP" to join.

- Enter the IP address you were given for the host's game, and hit enter.
  * Alternatively, if you've already used NetLauncher at least once, and
    someone has sent you a "netlaunch://" URL, just click that, and it should launch and connect.

-----------------
Additional stuff:
-----------------
To add usermaps:
- Copy .MAP files to the "usermaps" folder.

To play cooperative
- In EDuke32, select "new game" and select the cooperative game mode, set the difficulty and friendly fire options, and start.

To play usermaps:
- In EDuke32, just select "new game" and pick a usermap from the "usermaps" folder.

To play mods:
- Copy mod grp/pk3 files to the "mods" folder. They'll show in the launcher when hosting.

----------------
Troubleshooting:
----------------
On linux, NetLauncher won't... launch.
- Did you give it execute permissions? (Both the launcher and eduke32-oldmp need execute permissions)
- You can do this by typing "sudo chmod +x ./NetLauncher-linux64" in the terminal
- You can also do this in Ubuntu/Linux Mint by right-clicking NetLauncher-linux64, and enabling "Allow executing file as program" in properties->permissons.

NetLauncher hangs when trying to port forward with UPnP.
- This means you either don't have UPnP enabled on your router, or you don't have UPnP services enabled on your system.
- In windows, make sure you have the "UPnP Device Host" and "SSDP Discovery" services are enabled, and "Network Discovery" is enabled for private networks in the "Advanced Sharing Settings" control panel.
- In linux, it should "just work" unless there's an issue with the router or UPnP is disabled on it.

EDuke32-OldMP won't launch on Linux.
- Make sure the dependencies are installed, try "sudo apt-get install libgl1-mesa-dev libglu1-mesa-dev libsdl1.2-dev libsdl-mixer1.2-dev libsdl2-dev libsdl2-mixer-dev flac libflac-dev libvorbis-dev libvpx-dev libgtk2.0-dev freepats"
- Did you give it execute permissions? Try "sudo chmod +x ./eduke32-oldmp".
- This shouldn't happen, but if it does, please send me a report with your eduke32-oldmp.log and a log of the terminal when manually launching eduke32-oldmp in the command line, here: https://gitlab.com/mossj32/EDuke32-OldMP_Maintenance/issues
- Keep in mind, this is a x64 build. x86 (32-bit) builds are not supported at this time.