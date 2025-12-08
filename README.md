
# READ THE TUTORIAL BEFORE DOING ANYTHING


This is a tutorial for modding NieR Automata on linux (works on Arch and Fedora confirmed, but should work on any distro)

You can either:
1) follow the tutorial for auto installing everything
2) follow the tutorial for manual installation

First of all, copy the repo, then follow one of the two methods

Overview of the files in the repo:
1) Modding-Setup-Files               (Folder containing the necessary setup files for starting modding experience)
	1) d3d11.dll                        (SpecialK dll)
	2) NierAutomata.exe        (Wolf Size Limit Breaker exe)
	3) VC_redist.x64.exe          (Installer for Microsoft c++ tools 64 bit)
	4) VC_redist.x86.exe          (Installer for Microsoft c++ tools 32 bit)

2) Mods                                        (Folder containing all the mods that will be installed with the                                                     install-important-mods.sh script) 
	1) stuff
	2) stuff




## INSTALLER METHOD
This process is more automated but if something breaks it is harder to find what actually broke

1) Run the install-prerequisites.sh file, this will put the necessary files in your Nier Automata game folder:
	1) The installer for the c++ tools will pop-up twice, once for 64 bit and once for 32 bit
	2) The game's exe will be renamed and the new exe will be put in the game's directory
	3) The SpecialK dll will be put inside the game's directory

2) Launch the game, you should now see the SpecialK UI
   If you can launch a save with nothing breaking then you can close the game
   
   Press Win+Shift+Backspace to open SpecialK interface
   I suggest going into the Framerate Limiter section and setting the Framerate Cap at your monitor's refresh rate, so that NieR will run smoother without asking your GPU for frames that your monitor can't show

4) Your Nier Automata folder should now have this files (entries ending in / are folders)
     1) d3d11.dll                                        (SpecialK dll)
     2) d3d11.ini                                        (SpecialK config)
     3) data/
     4) FAR.ini                                             (Fix Automata Resolution config)
     5) logs/                                                (SpecialK logs folder)
     6) NierAutomata.exe                        (This is the  Wolf Size Limit Breaker exe)
     7) NierAutomata(original).exe        (Original game exe)
     8) SK_Res                                            (SpecialK folder for textures)
     9) steam_api64.sll
     10) Wallpaper
  
5) You can now install any mod you want by following the tutorials on nexus mods.
   Some mods (those that require Windows specific stuff) are probably not made for Linux and
   will therefore not work, I will not cover them because I do not know the entire mod list
   by memory (obviously)




## Manual installation
This is process is longer because it is less automated, but if anything doesn't work you will notice immediatly and will know exactly what broke it

Open the Modding-Setup-Files folder and the NieR Automata game folder in your file manager (you can open it via Steam by right clicking the game -> Manage -> Browse local files)
Follow the steps below

### STEP 1 - Installing C++ Tools
Run the VC_redist.x64.exe file by running this command:
./VC_redist.x64.exe        (if it doesn't work try using wine)

A window should open asking you to agree to Microsoft T&C
Accept by ticking the box and then click install

Repat the same procedure for the x86 file:
./VC_redist.x64.exe


### STEP 2 - Substitute game's exe with Wolf Size Limite Breaker exe
Rename the game's exe (NieRAutomata.exe) by giving it any other name (I suggest NieRAutomata(original).exe just for clarity)

Copy the NieRAutomata.exe file in the Modding-Setup-Files folder in the game's folder (Steam searched for a file with that name so it will now run the Wolf Size Limit Breaker exe when you launch the game)

### STEP 3 - Put SpecialK dll in game's folder
Copy the d3d11.dll file (I renamed it like this, it was originally SpecialK-64.dll) in the game's folder

Wolf Size Limit Breaker will automatically link the dll and the game will launch with SpecialK active

Your Nier Automata folder should now have this files (entries ending in / are folders)
     1) d3d11.dll                                        (SpecialK dll)
     2) d3d11.ini                                        (SpecialK config)
     3) data/
     4) FAR.ini                                             (Fix Automata Resolution config)
     5) logs/                                                (SpecialK logs folder)
     6) NierAutomata.exe                        (This is the  Wolf Size Limit Breaker exe)
     7) NierAutomata(original).exe        (Original game exe)
     8) SK_Res                                            (SpecialK folder for textures)
     9) steam_api64.sll
     10) Wallpaper

### STEP 4 - Launch the game
Launch the game via steam

If everything was done correctly SpecialK UI shoudl appear at the top of NierAutomata's window
Press Win+Shift+Backspace to open SpecialK interface

I suggest going into the Framerate Limiter section and setting the Framerate Cap at your monitor's refresh rate, so that NieR will run smoother without asking you GPU for frames your monitor can't show