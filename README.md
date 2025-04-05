# Instruction Cards Layout for RetroBat

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
   Place the entire folder containing the layout and its images into the following directory in RetroBat:  
saves/mame/artwork/

2. **Configure RetroBat:**  
- Make sure **Mame64** is selected in RetroBat.
- In the advanced options for the system or game, under **Visual Rendering**, set **Disable Artwork** to **No**.

3. **Select the View:**  
In RetroBat, launch MAME (typically Mame64) and select the view named `InstructionsCardsView` with [TAB] > Video Options > Screen #0.

4. **Check Inputs:**  
Check inputs in Mame during game (Tab key -> Inputs Settings -> Input Assignements (this system) -> 1 Player Start and Up and Down buttons)

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


