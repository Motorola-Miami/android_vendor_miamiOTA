# Miami OTA repo
This repo is to provide OTA updates to Motorola Edge 30 Neo (miami) devices.

## 1. Introduction ##
In order for a device to be OTA compliant, there are a few things to know.

### 1.1 JSON structure ###
```
{
  "response": [
    {
        "maintainer": "Name (nickname)",
        "oem": "OEM",
        "device": "Device Name",
        "filename": "ROM-<version>-<type>-<date>-<variant>-UNOFFICIAL-miami.zip",
        "download": "https://github.com/Motorola-Miami/miami_releases/releases/download/<tag>/<Name_of_the_ROM_file.zip",
        "timestamp": 0000000000,
        "md5": "abcdefg123456",
        "sha256": "abcdefg123456",
        "size": 123456789,
        "version": "<ROM-Version>",
        "buildtype": "Testing/Alpha/Beta/Weekly/Monthly",
        "forum": "https://forum link",
        "gapps": "https://gapps link",
        "firmware": "https://firmware link",
        "modem": "https://modem link",
        "bootloader": "https://bootloader link",
        "recovery": "https://github.com/Motorola-Miami/miami_releases/releases/download/%232/TWRP.img",
        "paypal": "https://donation link",
        "telegram": "https://t.me/motoedge30neoglobal",
        "dt": "https://github.com/Motorola-Miami/android_device_motorola_miami",
        "common-dt": "https://github.com/Motorola-Miami/android_device_motorola_sm6375-common",
        "kernel": "https://github.com/Motorola-Miami/android_kernel_motorola_sm6375"
    }
  ]
}
```

### 1.2 changelog.txt structure ### 
```
Highlights & Device Specific Changes:
Build type: Testing/Alpha/Beta/Weekly/Monthly
Device: Motoroala Edge 30 Neo
Device maintainer: <Your_Name>

===== <date> =====
- change 1
- change 2
- change 3
```

## 2 Guidelines ##
* Check if JSON is intact with help of online validator tools like [jsonformatter.curiousconcept](https://jsonformatter.curiousconcept.com) or [jsonformatter](https://jsonformatter.org)
* Check if no extra / missing spaces
* If you're not hosting the ROM on Motorola-Miami Github/Sourceforge then :-
  - Hosting on Google Drive is not allowed.
  - Temporary hosting is not allowed.

### 3 Initial support ###
After you have build and booted the ROM for which you wanna provide OTA updates for
1. Make sure you read [this](https://github.com/Motorola-Miami/android_miami_packages_apps_Updater) OTA updater repo and apply the modification while building instead of the default one synced from ROM's source or unofficial OTA will not work.
1. Contact @Rakhshan7070 on [Telegram](https://t.me/shan_rakh) or Email (alirakhshan7070@gmail.com) if you want to release your build on Motorola-Miami github organisation or Motorola-Miami Sourceforge. If you want to host it somewhere else then skip this point.
1. Fork this repo to your own GitHub account and clone it locally.
2. Create changelog_<ROM>.txt and <VANILLA/GAPPS/CORE>_<ROM>.json
3. Modify the files accordingly. (see 1.1)
6. Submit a pull request to this repo (this way we validate that you understood the requirements and if all is good you'll be granted direct push access to this repo)

