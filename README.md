# AC-Plugins

Asheron's Call plugins, clients and tools, packaged. Each zip unpacks to a folder of its own. The plugins and the loot editor work in either client; the clients and MelkTank Remote are in `Linux/` and `Windows/`; the sources are in `source/`.

| Package | What |
|---|---|
| `MelkTank-Retail.zip` | MelkTank for the retail client (Decal): `MelkTank.dll` (the loader) and `MelkTankCore.dll` |
| `MelkTank-ACGodot.zip` | MelkTank for ACGodot (`plugins/MelksTank`) - works in ACGodot on Linux and Windows |
| `MelksQB-Retail.zip` | MelksQB quest tracker for the retail client |
| `MelksQB-ACGodot.zip` | MelksQB for ACGodot (`plugins/MelksQB`) |
| `MelksQB_Maps1.zip`, `MelksQB_Maps2.zip` | MelksQB's dungeon map pictures (its `Maps` folder, in two parts) |
| `Linux/ACGodot-Client.zip` | ACGodot, the Godot-based AC client, for Linux (needs Godot 4.7.2 .NET and the .NET 10 runtime) |
| `Windows/ACGodotWin-Client.zip` | ACGodot for Windows: `Start ACGodot.bat` fetches Godot the first time (see `README-Windows.md` inside) |
| `Linux/MelkTankRemote.zip` | MelkTank Remote for Linux: the launcher, the phone service and the Android app |
| `Windows/MelkTankRemote_Windows-2.20.zip` | MelkTank Remote for Windows, for Asheron's Call with Decal |
| `Windows/MelkTankRemote_Windows_ACGodot-2.20.zip` | MelkTank Remote for Windows, for ACGodot |
| `LootEditor.zip` | The MelkTank loot editor, outside the game (Linux and Windows) |

`source/` holds each one's source as a zip.

## Updated Settings Files

Data files that save you typing it all in yourself: monster info, dungeon and zone names, portals and travel points. Copy each one into your plugin folder at the place shown, replacing the file that's there. Close the game first, because the plugins save over some of these files while running. If you've added entries of your own, back up your copy first.

The plugin folder is `plugins/MelksTank` or `plugins/MelksQB` inside ACGodot, or the `MelksTank` / `MelksQB` folder you unzipped for Decal. The places are the same in both.

### MelkTank (`MelksTank` folder)

| File | Goes in | What it does |
|---|---|---|
| `MelkTank_MonsterDb.txt` | `Settings/` | The monster database: weaknesses, resistances and notes for each monster, shown in the Monster DB tab |
| `vtank_gameinfo.txt` | `Profiles/Monsters/` | The VTank game info: monster species, damage-type overrides, spell cooldowns and healing kits. Plain text you can edit; MelkTank picks up changes within about 10 seconds |
| `MelkTank_Monsters.xml` | `Settings/` | A starter monster list for characters that don't have one of their own yet |
| `MelkTank_Locations.xml` | `Settings/` | Dungeon names by landblock, so dungeons show their name instead of a number |
| `MelkTank_ZoneLandblocks.txt` | `Settings/` | Which landblocks belong to which hunting zone, used by the bounty tracker |
| `MelkTank_NavPresets.xml` | `Settings/` | Ready-made blocks of nav steps (like "Mob Pack") you can drop into a route |
| `MelkTank_SpellWords.txt` | `Settings/` | The words of spell incantations, so chat sorts them as combat instead of normal chat |

### MelksQB (`MelksQB` folder)

| File | Goes in | What it does |
|---|---|---|
| `locations.xml` | `Travel/` | The full list of towns, portals and places used by the map and auto-travel |
| `MQT_Travel.xml` | (the folder itself) | What MelksQB has learned in the game: portals seen or used and where recalls, gems and commands take you |
| `MQT_PortalBots.xml` | (the folder itself) | Portal bots: who to send a tell to and which portal they open |
| `MQT_NewFlags.xml` | (the folder itself) | Quest flags seen in the game, for the Edit Quest tab to pick from |
| `MelksQB Travel.mtnav` | `Travel/` | The last route auto-travel built |
| `MelksQB Travel (shown).mtnav` | `Travel/` | The route drawn on the map for that trip |
