<div align="center">
<a href="https://github.com/Yeadee/Toffee">
<img src="[https://toffeelive.com/logo.svg](https://raw.githubusercontent.com/Yeadee/ToffeeV2/refs/heads/main/images/Toffee_logo.png)" alt="Logo" width="400px">
</a>
<br/>

</div>

## About The Project

A simple script to automatically update Toffee channels list with cookies every 4 hours.<br/>

[![Yeadee - Toffee](https://img.shields.io/static/v1?label=Yeadee&message=Toffee&color=blue&logo=github)](https://github.com/Yeadee/ToffeeV2 "Go to GitHub repo")
[![stars - Toffee](https://img.shields.io/badge/made_with-python_3.10-blue)](https://www.python.org/)
[![issues - Toffee](https://img.shields.io/github/issues/Yeadee/Toffee)](https://github.com/Yeadee/ToffeeV2/issues)
[![Badge](https://hitscounter.dev/api/hit?url=https%3A%2F%2Fgithub.com%2FYeadee%2FToffeeV2&label=Visitors&icon=link&color=%23198754)](https://github.com/Yeadee/ToffeeV2)
<br/> ![GitHub Repo stars](https://img.shields.io/github/stars/Yeadee/ToffeeV2?link=https%3A%2F%2Fgithub.com%2FYeadee%2FToffeeV2)

## Key Features

- Combined the new api with the old api that will always update new channels as soon as they come. It's just better than everything out there right now.
- Premium events are also available.
- provides ready-to-use m3u file for NS player.
- provides data as json for developers' use.

## How To Use

- Use [this](https://raw.githubusercontent.com/Yeadee/ToffeeV2/main/toffee_channel_data.json) link for TV data.

- script to obtain m3u8 information:
  ```python
  import requests
  link="https://raw.githubusercontent.com/Yeadee/ToffeeV2/main/toffee_channel_data.json"
  response=requests.get(link).json()
  name=response["name"]
  for channel in response["channels"]:
    url=channel["link"]
    headers={"cookie":channel["cookie"]}
    break
  main_response=requests.get(url,headers=headers).text
  print(main_response)
  ```
>Prerequisite: You need to have [Python](https://www.python.org) installed on your machine.
- Output:
```
#EXTM3U
#EXT-X-VERSION:3

#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=1024000,RESOLUTION=1280x720
../slang/cnn_576/cnn_576.m3u8?bitrate=1000000&channel=cnn_576&gp_id=
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=768000,RESOLUTION=854x480
../slang/cnn_320/cnn_320.m3u8?bitrate=768000&channel=cnn_320&gp_id=

#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=512000,RESOLUTION=640x360
../slang/cnn_160/cnn_160.m3u8?bitrate=512000&channel=cnn_160&gp_id=

```
## FOR IPTV PLAYBACK
### Android
- Install [NS Player](https://play.google.com/store/apps/details?id=com.genuine.leone)
- Add new Playlist with [this](https://raw.githubusercontent.com/Yeadee/ToffeeV2/refs/heads/main/toffee_channel_data.json) link as URL.
### Android TV
- Install [OTT Navigator](https://apkpure.com/ott-navigator-iptv/studio.scillarium.ottnavigator/amp)
- Add new Playlist with [this](https://raw.githubusercontent.com/Yeadee/ToffeeV2/refs/heads/main/toffee_ott_navigator.m3u) link as URL.

## NOTES

- This Readme documentation is made in resemblance with the docs of the famous Toffee repo by [Byte-Capsule](https://github.com/byte-capsule).
- This script is for educational purposes only. Do not use it for any illegal activities. If the code affects the revenue of the IPTV owners, please let me know and I will delete it.
- Please give me proper credit if you share this content. Otherwise, I will take it down.
- Due to geo-restriction, the contents are only available in Bangladesh.

## Support

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/yeadee)

## QUESTIONS

Questions are welcome at [https://github.com/Yeadee/ToffeeV2/discussions](https://github.com/Yeadee/ToffeeV2/discussions).
This repo is also open for discussion.

## Find Me

<div>
  <a href="https://x.com/i3pranto" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/twitter/default.svg" width="52" height="40" alt="twitter logo"  />
  </a>
  <a href="https://t.me/pranto_bhai" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/telegram/default.svg" width="52" height="40" alt="telegram logo"  />
  </a>
</div>
