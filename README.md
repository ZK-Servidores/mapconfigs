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

## Credits

- [berni](https://forums.alliedmods.net/member.php?u=27799)
- [tabakhase](https://forums.alliedmods.net/member.php?u=254788)