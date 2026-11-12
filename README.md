Melk's Plugins for Asheron's Call (InfiniteLeaftide)
=====================================================

QB updates -
Copy the Travel folder into your MelkQB folder.
Copy MQT_Travel.xml into your MelkQB folder as well (the base, not in travel)


Which zip do I want?
--------------------
  MelksPlugins_All.zip         <- START HERE. The three Decal plugins together (MelkTank, MelksQB,
                                  the Luminance tracker). This is all most people need.

  MelksTank.zip                \
  MelksQB.zip                   > the same three plugins one at a time - only for installing or updating one
  MelksLuminanceTracker.zip    /  of them. If you used MelksPlugins_All.zip you don't need these.

  Optional extras (not Decal plugins - don't add them in Decal):
  MelksQB maps zip             dungeon maps for MelksQB's map window. Extract it INTO the MelksQB folder,
                               so you end up with  Decal Plugins\MelksQB\Maps\...
  LootEditor zip               a loot-profile editor that runs outside the game (Linux / Python).
  MelkTankRemote_Linux.zip     a game launcher + phone app service for Linux (Wine) players. See its README.

You need first
--------------
  - Decal 2.9.8.3 (the current version)
  - UtilityBelt, installed and ticked in Decal (the windows are drawn with UtilityBelt's window system)
  - .NET Framework 4.8 (already part of Windows 10 / 11)

Windows: the dlls must not be "blocked"
---------------------------------------
  Windows marks files that came from the internet as blocked, and Decal can't register a blocked dll -
  it says "Failed to register". After extracting, right-click each of the three loader dlls (listed under
  Install) -> Properties -> if there's an "Unblock" tick box at the bottom of the General tab, tick it -> OK.
  Or unblock all of them at once in PowerShell (change the path to your Decal Plugins folder):
     Get-ChildItem "C:\Games\Decal Plugins\Melks*" -Recurse | Unblock-File

Install
-------
  1. Put MelksPlugins_All.zip in your Decal Plugins folder (e.g. C:\Games\Decal Plugins)
     and choose "Extract here". You should end up with:

        Decal Plugins\
           MelksTank\               MelkTank.dll, MelkTankCore.dll, Settings\, Profiles\
           MelksQB\                 MelksQuestTracker.dll, MelksQuestTrackerCore.dll, QuestDatabase.xml
           MelksLuminanceTracker\   MelksLuminanceTracker.dll, MelksLuminanceTrackerCore.dll

     (If you got an extra folder level - Decal Plugins\MelksPlugins_All\MelksTank\... - that works too, but
      it's tidier to move the three folders up one level.)

  2. Open the Decal Agent (right-click Decal's tray icon), click Add, and add these three - the small
     loader dlls, NOT the ones with "Core" in the name:
        MelksTank\MelkTank.dll
        MelksQB\MelksQuestTracker.dll
        MelksLuminanceTracker\MelksLuminanceTracker.dll
     (The dlls, not the zips - Decal can't add a zip. Unblock them first if Windows has blocked them.)
     Make sure each one is ticked.

  3. Start the game. Each plugin shows up in UtilityBelt's bar.

If Decal says "Failed to register"
----------------------------------
  1. You picked a zip - Decal can only add a .dll. Extract the zip first and add the dll from the
     extracted folder.
  2. The dll is blocked - see "the dlls must not be blocked" above.
  3. You picked a Core dll - pick the small one without "Core" in its name.
  4. The dll was moved out of its folder - each loader and its Core dll must stay together in the plugin's folder.
  5. The folder is on OneDrive or a network drive - put the plugins on your local disk (e.g. C:\Games\Decal Plugins).
  6. Decal is older than 2.9.8.3 - update Decal.
  Plugins that register but show no window: UtilityBelt isn't installed or isn't ticked in Decal.

Updating later
--------------
  Extract the new zip over the top (then unblock the dlls if Windows has blocked them). Your settings and logs aren't in the zip, so they're kept.
  The plugins reload themselves when their Core dll is replaced, so this works with the game running.
