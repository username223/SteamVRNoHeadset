# Running SteamVR without a headset attached (using the null driver)

You will need to edit two files, the `default.vrsettings` of the null driver, and the `default.vrsettings` of SteamVR.

## Steam Directory

Both files are contained in your steam directory. Where that directory is depends on your operating system.

### Windows

On Windows this is usually `C:\Program Files (x86)\Steam\steamapps\common\SteamVR\drivers\null\resources\settings`, unless you installed Steam on another drive.

### Linux

On Linux it depends on whether you've installed steam from the homepage or from the official package manager.

If installed from the homepage, at least on Ubuntu, it should be in `~/.local/share/Steam`, while the official package manger places it in `~/.steam`.

## Null Driver File

The null driver file can be found in `*Steam Directory*/steamapps/common/SteamVR/drivers/null/resources/settings/default.vrsettings`.

Open the null driver file and replace `"enable": false,` with `"enable": true,`.

## SteamVR Config File

The second file, the SteamVR config file, can be found in `*Steam Directory*/steamapps/common/SteamVR/resources/settings/default.vrsettings`

Change `"requireHmd": true,` to `"requireHmd": false,`, `"forcedDriver": "",` to `"forcedDriver": "null",` and `        "activateMultipleDrivers": false,` to `"activateMultipleDrivers": true,`.

Notice that, like it says at the top of the file, this file will be replaced when SteamVR updates. If you want, you can place the settings in your `steamvr.vrsettings` file located somewhere in the Steam directory. Make sure you place them under the `steamvr` header.
