<img src="https://mi.fiime.cn/static/upload/2023/05/11/202305114617.jpg">

# ArrowOS-Extended

Getting Started
---------------
To get started with the ArrowOS sources, you'll need to get
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

To initialize your local repository, use command:

```bash
repo init -u https://github.com/ArrowOS-Extended/android_manifest.git -b arrow-13.1
```

Then sync up:

```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

Building the System
-------------------
 Initialize the ROM environment with the envsetup.sh script.

```bash
. build/envsetup.sh
```

Lunch your device after cloning all device sources if needed.

```bash
lunch arrow_devicecodename-buildtype
```

Start compilation

```bash
m otapackage
```

OR

```bash
m bacon
```

**Changelog:**

[Changelog Monthly](https://github.com/ArrowOS-Extended/arrow_extended_changelog)

---------------------------------------------------------------------------------------------------------------------

[ArrowOS Website](https://www.arrowos.net) | [ArrowOS Blog](https://blog.arrowos.net)

---------------------------------------------------------------------------------------------------------------------
