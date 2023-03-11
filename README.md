# Map Confis

Allows you to have per map config files. Support for map prefix configs **(example: dm_.cfg)**

This is a complete rewrite of a map configs plugin I found somewhere.

You can have prefix configs that allow you to easily execute cvars/commands for a group of maps, without having to create a cfg file for each of them.

The executing order is alphabetical, that means configs that have the shortest name will be executed first.

### Example:

Your maps name is **js_build_puzzle_nine_v10**.

Your config files are **js_build_puzzle_nine_v10.cfg**, **js_build_.cfg** and **js_.cfg**

The executing order will be:
- js_.cfg
- js_build_.cfg
- js_build_puzzle_nine_v10.cfg

For anyone looking for the chance to change ConVars such as mp_teamplay instantly with this plugin upon map/s load, not having to set them before changing map anymore, you can use attached custom version.

Config file patterns:
- **`*.pre.cfg` (new):** For settings that must be applied as soon as map begins loading **(required for mp_teamplay)**
- **`*.cfg` (unchanged):** For settings that must be applied right after both the map and base settings **(e.g. server.cfg)** load

Use case: **"Overriding gamemode = CTF. I want to enforce mp_teamplay 1, and also set timelimit to 60"** > Add **`mp_teamplay 1`** to **`ctf.pre.cfg`** and **`mp_timelimit 60`** to **`ctf.cfg`**. +If you need to disable teamplay on the normal modes (not CTF), you could add mp_teamplay 0 to ctf.cfg; this way, the value will be 0 at the CTF session/s but teamplay disable will only be effective when returning to a normal mode.

## Credits

- [berni](https://forums.alliedmods.net/member.php?u=27799)
- [tabakhase](https://forums.alliedmods.net/member.php?u=254788)