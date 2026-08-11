Pokémon Ultra Sun / Ultra Moon Expansion
=========================================

This project expands Pokémon Ultra Sun and Ultra Moon with Pokémon, forms,
moves, and abilities introduced in Generations VIII and IX. Gigantamax forms
and some Terastal forms are not included.

This is a work in progress. Back up your game and save data before installing,
save frequently, and expect that unfinished features may still cause crashes.


Supported games
---------------

  Pokémon Ultra Sun  (USA 1.0)  Title ID: 00040000001B5000
  Pokémon Ultra Moon (USA 1.0)  Title ID: 00040000001B5100

Ultra Sun and Ultra Moon use different executable files. Always download and
install the archive that matches your game.


Archive contents
----------------

Each game has one complete archive:

  UltraSun_Expansion.zip
  UltraMoon_Expansion.zip

The archive opens directly to this layout:

  README.txt
  SpritesCredits/
    Credits.txt
  exefs/
    code.bin
  romfs/
    Battle.cro
    a/
    ...

The same archive works for console and emulator installations. Follow the
appropriate instructions below because each platform places code.bin in a
different location.


Installing on a Nintendo 3DS with Luma3DS
-----------------------------------------

1. Confirm that Luma3DS custom firmware is installed.

2. Enable game patching:

   - Power off the system.
   - Hold SELECT while turning it on.
   - Enable "Enable game patching" in the Luma3DS configuration menu.
   - Press START to save and reboot.

3. On the SD card, open luma/titles. Create the titles directory if it does not
   already exist, then create the directory matching your game:

   Ultra Sun:  SD:\luma\titles\00040000001B5000\
   Ultra Moon: SD:\luma\titles\00040000001B5100\

4. Extract the archive that matches your game.

5. Copy the complete romfs directory into the matching title directory.

6. Copy exefs/code.bin into the title directory itself. On the SD card it must
   be named code.bin and sit next to romfs. Do not copy the exefs directory to
   the title directory.

The finished SD card layout should resemble this:

  SD:\
  `-- luma\
      `-- titles\
          `-- 00040000001B5000\       <- Ultra Sun title ID
              |-- code.bin             <- copied from exefs\code.bin
              `-- romfs\               <- complete romfs directory
                  |-- Battle.cro
                  `-- a\
                      |-- 0\...
                      |-- 1\...
                      |-- 2\...
                      `-- 3\...

For Ultra Moon, use the title directory 00040000001B5100 instead. Restart the
system after installing or replacing game files.


Installing on Azahar or Citra
-----------------------------

1. Extract the archive that matches your game.

2. Locate the emulator's load/mods directory:

   - On desktop, right click the game and choose the option that opens its mods
     location. In Azahar, this is under Open > Mods Location.
   - On Android, press and hold the game, then open its mods location.

3. Open or create the directory named with the Title ID for your game:

   Ultra Sun:  Azahar/load/mods/00040000001B5000/
   Ultra Moon: Azahar/load/mods/00040000001B5100/

   Citra uses the same load/mods/Title ID structure inside its data directory.

4. Copy exefs, romfs, SpritesCredits, and README.txt directly into the matching
   Title ID directory. Avoid creating an additional directory around them.

The resulting layout should resemble this:

  Azahar/
  `-- load/
      `-- mods/
          `-- 00040000001B5000/       <- Ultra Sun title ID
              |-- README.txt
              |-- SpritesCredits/
              |   `-- Credits.txt
              |-- exefs/
              |   `-- code.bin
              `-- romfs/
                  |-- Battle.cro
                  `-- a/...

For Ultra Moon, use the Title ID directory 00040000001B5100 instead.

Restart the emulator after installing or replacing game files.


Gameplay and save notes
-----------------------

The expansion adds Pokémon to the game data, but does not automatically add
them as wild or overworld encounters. This PKHeX fork can be used to add them
to a save:

  https://github.com/Aqua-0/PKHeX/releases/tag/v1.0

Modified saves may be incompatible with services such as Pokémon Bank. Keep an
untouched backup of every save before editing it.

Compatibility with other mods is not guaranteed. Combining mods can overwrite
files from either project and is done at your own risk.


General setup and installation guides
-------------------------------------

The following are general guides. They were not made for this expansion and do
not show its specific files. The emulator setup guides include sections that
explain how to install mods. The console link is a general mod installation
guide.

Nintendo 3DS mod installation:
  https://www.youtube.com/watch?v=geTkR1oKbkg

PC emulator setup and mod installation:
  https://www.youtube.com/watch?v=--GRK4OKSaY

Android emulator setup and mod installation:
  https://www.youtube.com/watch?v=wL8NlGGvxJ4


Project page and license
------------------------

Official project page:
  https://gamebanana.com/wips/102511

This project is free. If you paid for it, you were scammed. When sharing or
referencing the project, preserve the appropriate credits, link to the official
project page, and comply with its license:

  https://creativecommons.org/licenses/by-nc-nd/4.0/
