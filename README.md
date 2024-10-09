<img src="https://mi.fiime.cn/static/upload/2023/05/11/202305114617.jpg">

# ArrowOS-Extended

Getting Started
---------------
To get started with the ArrowOS sources, you'll need to get
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

To initialize your local repository, use command:

```bash
repo init -u https://github.com/ArrowOS-Extended/android_manifest.git -b arrow-13.1 --git-lfs
```

Then, sync the sources:

```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

Building the System
-------------------
First, initialize the ROM environment with the envsetup.sh script:

```bash
. build/envsetup.sh
```

After cloning the necessary device sources, set up the build environment for your device:

```bash
lunch arrow_devicecodename-buildtype
```

### Unsigned Build:
To build an unsigned ROM:
```bash
m bacon
```

### Signed Build:
If you haven't already generated keys, you can do so with the following command (email is optional; if omitted, your Git configuration email will be used):
```bash
gen_keys [email]
```

Then, proceed with building the signed ROM:
```bash
ota_sign
```
Or if you already have your keys, clone them to vendor/arrow/signing/keys.

**Changelog:**

[Changelog Monthly](https://github.com/ArrowOS-Extended/arrow_extended_changelog)

[Updates Channel](https://t.me/arrowextended)

---------------------------------------------------------------------------------------------------------------------

[ArrowOS Website](https://www.arrowos.net) | [ArrowOS Blog](https://blog.arrowos.net)

---------------------------------------------------------------------------------------------------------------------
