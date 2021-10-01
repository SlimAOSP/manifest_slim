![SlimAOSP](https://github.com/SlimAOSP/manifest_slimaosp/blob/ten/banner/SlimAOSP.png)

# SlimAOSP #

# The Stock Experience #

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/SlimAOSP/manifest_slimaosp -b ten

You can alternatively use this command to save some space and time :

```bash
repo init --depth=1 -u https://github.com/SlimAOSP/manifest_slimaosp.git -b ten

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
```
You can just use `repo sync` or above command, but this will save you from lot of terminal spam, data and time.
```bash
repo sync -c -q --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -jX
