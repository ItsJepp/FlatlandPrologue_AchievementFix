# Flatland: Prologue Achievement Fix
An xdelta patch to fix the broken achievements in Flatland: Prologue.

## Installation Instructions
1. Download the .xdelta file from this repo
2. Download [Delta Patcher](https://www.romhacking.net/utilities/704/)
3. Run Delta Patcher and select the required files
   - **Original file:** The `data.win` file in the game files (e.g. `C:\Program Files (x86)\Steam\steamapps\common\Flatland Prologue\data.win`)
   - **XDelta patch:** The downloaded .xdelta file
4. Press `Apply patch`, then go forth and achieve!

## How do I get the achievements?
### WELCOME TO FLATLAND!
Select "Intro" from the level select or start a new game and complete the level.

### I see you in Flatland Vol.1 <3
Select "Level 10" from the level select and complete the level.

## Why were the achievements broken?
I'm not super familiar with GameMaker, but in case anyone is interested here's a very quick explanation of what I think was going on.

It seems like many of the level completion achievements were unlocked when the player collided with the "door" object at the end, however I think an alternate custom version of the door object was used on the first and last levels of the game, meaning the achievement checking code is never run for those.
