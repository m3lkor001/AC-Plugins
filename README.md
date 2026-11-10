Melk's Plugins for Asheron's Call (InfiniteLeaftide)
=====================================================

What's in here
--------------
  MelksTank\               MelkTank - combat, buffs, pets, nav, metas, looting, Monster-Dex catching
     MelkTank.dll          the plugin Decal loads (a small loader)
     MelkTankCore.dll      everything else (the loader loads it - keep the two together)
     Settings\             monster database, zone landblocks, saved locations
     Profiles\             loot profiles, metas, nav routes, monster lists
  MelksQB\                 MelksQB quest tracker
     MelksQuestTracker.dll
     MelksQuestTrackerCore.dll  (the loader loads it - keep the two together)
     QuestDatabase.xml     every quest, its QB flags and its walkthrough
  MelksLuminanceTracker\   luminance / coin tracker
     MelksLuminanceTracker.dll
     MelksLuminanceTrackerCore.dll

You need first
--------------
  - Decal
  - UtilityBelt (the plugins draw their windows with UtilityBelt's window system - it has to be installed and on)

Install
-------
  1. Put this zip in your Decal Plugins folder (where your other plugins live, e.g. C:\Games\Decal Plugins)
     and "Extract here". You get the three folders above.
  2. Open Decal (the Decal Agent - right-click the Decal icon in the tray, or run "Decal Agent"), click Add,
     and pick each plugin's dll:
        MelksTank\MelkTank.dll                (NOT MelkTankCore.dll)
        MelksQB\MelksQuestTracker.dll
        MelksLuminanceTracker\MelksLuminanceTracker.dll
     Make sure each one is ticked (enabled).
  3. Start the game. Each plugin gets a window / bar icon. Settings are saved per character next to the dll
     the first time you change something.

Updating later
--------------
  Extract a newer zip over the top. Your settings and logs are separate files and aren't in the zip,
  so they're kept. All three reload themselves when their Core dll is replaced, so you can update with the game running.
  (A new loader dll - MelkTank.dll, MelksQuestTracker.dll, MelksLuminanceTracker.dll - needs a game restart.)

  The MelksQB dungeon maps aren't in this set - keep your existing MelksQB\Maps folder.
