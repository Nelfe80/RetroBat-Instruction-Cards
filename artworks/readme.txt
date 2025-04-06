Push Artwork to /saves/mame/artwork/

In Retrobat Mame
Config system : 
EMULATOR > MAME64
Visual Rendering > Disable Artwork > No

NB:
Many CPS1 & CPS2 games needs qsound_hle.zip : add qsound_hle.zip in your folder mame rom (MAME64 needs this file)
CPS3 Games : add chd file in a folder with rom name in rom folder
ALTBEAST : use altbeast.7z 4MO

If you have a problem and the keys are not recognized, you can try on RetroBat to put 
Advanced System Options > Emulator > Mame64
and launch the game
and then 
Advanced System Options > Emulator > Auto
and launch the game
and again 
Advanced System Options > Emulator > Mame64
and test.
This seems to reset a few things and has already helped me get Final Fight working, for example.

<!--

- Artwork type: Instructions Cards
- Converted for MAME by Nelfe80
- IC Images from Marlon Lopez, Thanks!
- Lay file by Nelfe80

-->

In Mame RetroBat, to change instruction card, press and hold start, then use the up and down buttons to select which instruction card to display.

If you have problems, you can launch a game directly with the layout plugins enabled by going to the /emulators/mame/ folder and opening a powershell :
./mame -plugins -plugin layout <rom name without extension>

If this still doesn't work, it may be a problem with RetroBat settings. Try setting everything to auto for the game and the Mame system, then launch the game. Then exit the game and select only Mame64 in the System advanced options and launch the game again. This sometimes allows you to reset certain parameters that could interfere with the normal launch of Mame.
