<img src="https://github.com/Nelfe80/RetroBat-Instruction-Cards/blob/master/_img/logo.png?raw=true"/>

# Instruction Cards Layout for Mame & RetroBat

This project provides a customizable MAME layout that displays interactive instruction cards on the left and right sides of the screen. The layout is designed for use with multiple games and lets you switch instruction cards by holding the Start button and pressing Up or Down.

<img src="https://github.com/Nelfe80/RetroBat-Instruction-Cards/blob/master/_img/sf2ce.png"/>

## Overview

The layout shows two sets of instruction cards:
- **Left Side (Player 1)**
- **Right Side (Player 2)**

When active, the layout lets you change the instruction cards as follows:

- **Player 1 (Left Side):**  
  Hold the Start button and press Up or Down to cycle through the instruction cards on the left.

- **Player 2 (Right Side):**  
  Hold the Start button and press Up or Down to cycle through the instruction cards on the right.

The layout script uses input port values and bit masks defined as variables and applies edge detection so that the card only changes once per button press.

## Installation

1. **Copy the Artwork Folder:**  
   Place the entire folder containing the layout of the game and its images into the following directory in RetroBat:  
saves/mame/artwork/ \<RomNameWithoutExtension\> /

   Or directly in the folder /mame/artwork/ \<RomNameWithoutExtension\> / (if you don't have RetroBat)

2. **Configure RetroBat:**  
- Make sure **Mame64** is selected in RetroBat.
- In the advanced options for the system or game, under **Visual Rendering**, set **Disable Artwork** to **No**.
- Do **not select a bezel**.
- If you observe a problem in RetroBat, make sure "**layout&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1**" is in the file "plugin.ini" in /bios/mame/ini/plugin.ini (the plugin seems to be activated by default, but it's a good idea to check this out) ==> We need LUA scripts to be supported in Mames Layout thanks to the mame “layout” plugin.

3. **Configure Mame:**

- If you don't use RetroBat, make sure "**layout&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1**" is in the file "plugin.ini" in the Mame emulator folder.
==> We need LUA scripts to be supported in Mames Layout thanks to the mame “layout” plugin.
- If you observe a problem, update your MAME and roms if necessary

4. **Select the View:**  
- Launch your game with Mame64. In MAME select the view named `InstructionsCardsView` with [TAB] > Video Options > Screen #0.

5. **Check Inputs:**  
- If you observe a problem, check inputs in Mame during game (Tab key -> Inputs Settings -> Input Assignements (this system) -> 1 Player Start and Up and Down buttons)

<img src="https://github.com/Nelfe80/RetroBat-Instruction-Cards/blob/master/_img/check.png"/>

## Usage

- **Player 1 (Left Side):**  
- **Start Button:Hold the Start button**
- **Up:Next card**
- **Down:Prev card**

When Player 1 holds Start and presses Up or Down, the left instruction card cycles to the next or previous image.

- **Player 2 (Right Side):**  
- **Start Button:Hold the Start button**
- **Up:Next card**
- **Down:Prev card**

When Player 2 holds Start and presses Up or Down, the right instruction card cycles accordingly.

RetroBat-Instruction-Cards is a Mame-integrated solution that uses only Mame's Layout plugin and exploits the inputs of the various emulated systems to access the Start, Up and Down keys. 
This solution does not depend on external development or enhanced software. It can therefore be easily used in all systems running Mame.

You may run into problems and start or up or down may not react the way you want.
If you've made configurations before, you may have cached files with your old configuration. It's already happened. Look for the name of the rom in your retrobat folder and delete the cache (zip or others, but not scrap images and your rom 😉) and .lay files except those in saves/mame/artwork.

Instructions cards from Marlon Lopez :
https://www.mmg1designs.com/instruction-cards-for-hyperlaunch-with-moves-list-for-various-street-fighter-games/
Thanks !

