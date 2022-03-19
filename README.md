# amolinae's Half-Life mod tutorial

Welcome to the wonderful Half-Life modding scene here you will learn all about the folder structure of a basic mod of your own.

## Creation of your mod

Open Steam and browse for Half-Life's local files ``\steamapps\common\Half-Life`` and create a folder with any name **WITHOUT** spaces or caps, now open the folder that you just have created and generate a new text file, rename it as ``liblist.gam`` ignore the extension change popup. After that create 2 new folders one named ``dlls`` and the other one ``cl_dlls`` now you are done!

for now...

## Explanation of the main game files

### liblist.gam file

The liblist.gam file is one of the most important files in your Half-Life mod, it tells Steam and the engine information about your mod and where are the game's dlls located. In this repository we have an example of the liblist.gam, you can modify it as you wish, here we have a few options that can be used with the file:

>- game - The name of the mod
>- version - The mod's version number
>- cldll - "1" if the mod requires a matching client.dll
>- type - If this mod is "multiplayer_only", then the single player buttons ( New Game/Hazard Course/Load game etc.) are disabled in the Half-Life launcher
>- gamedll - The game DLL to load for running a server for this mod.
>- startmap - When a user chooses "New Game" for a single player mod, this is the map that is loaded.
>- trainmap - When a user chooses "Hazard Course" for a single player mod, this is the map that is loaded.

### Dynamic Link Libraries

Your Half-Life mod requieres some dlls (Dynamic Link Libraries) to work (These files tell the engine how npcs and other stuff work), Valve has [their own SDK](https://github.com/ValveSoftware/halflife) available to the public, however it is outdated and cannot be compiled with modern software. Hopefully SamVanheer has taken the time to refactor and update [the code](https://github.com/SamVanheer/halflife-updated) to be compiled under newer versions of Visual Studio.

## Running your mod

After preparing the mod you have to restart Steam, then search for the name of your mod and launch it, the game will automatically read the files and start. Now you have a fully functional Half-Life mod.