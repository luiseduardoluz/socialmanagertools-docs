> 📌 [index](../../../README.md) / 🐣 twbot / 💾 [installation](../README.md) / 🐳 [docker](README.md)

# 🐳 Setup - Docker on Raspbian 9
## 1. Install docker
1. `curl -sSL https://get.docker.com | sh`
2. `sudo usermod -aG docker pi`

## 2. Run
1. Get [config.js](https://raw.githubusercontent.com/social-manager-tools/socialmanagertools-twbot/master/configs/config.js.tpl) remove  `.tpl ` suffix and save file in your home directory, fill it properly.
2. Edit `config.js` and set `chrome_headless` on `enabled` (or to `true` in `v0.9.X` version) and set `chrome_executable_path` to `/usr/bin/chromium-browser`. **Without this fix docker don't work.**
3. Edit `/home/pi/config.js` (in next bash command) with your correct config path and run it for start docker. Bot start automatically.

```sh
docker run --restart=always --name=socialmanagertools-twbot -d -v /home/pi/config.js:/app/configs/config.js socialmanagertools/twbot:armv7
```

**AVAILABLE TAGS:** `armv7` (Raspberry PI 2 and Raspberry PI 3), `armv8` (Raspberry PI ARM v8)

# 🐳 Setup - Docker on Debian 9
## 1. Install docker
1. `curl -sSL https://get.docker.com | sh`
2. `sudo usermod -aG docker [USERNAME]` (replace `[USERNAME]` with your debian user account)

## 2. Config
1. Get [config.js](https://raw.githubusercontent.com/social-manager-tools/socialmanagertools-twbot/master/configs/config.js.tpl) remove  `.tpl ` suffix and save file in your home directory, fill it properly.
2. Edit `config.js` and set `chrome_headless` on `enabled` (or to `true` in `v0.9.X` version) and set `chrome_executable_path` to `/usr/bin/chromium-browser`. **Without this fix docker don't work.**

## 3. Proxy (If you use debian on server)
**IMPORTANT**: **is mandatory use vpn/proxy if you don't want risk of _soft ban_ or _ban_ with server use**.

Twitter, Twitter and Facebook detects after 2-48h server/hosting/vps from ovh, aws, cloud, digital ocean and other providers... What happen if it detects you? On twitter, if the bot clicks on like, twitter removes likes after refresh page = bot will not work.

1. Buy proxy server of your country from [highproxies](https://www.highproxies.com/twitter-proxies/) or from you favorite distributor.
2. Edit `configs/config.js` and:

##### 🔙 v0.9.X or previously
- Add new value in `chrome_options` array, example: `"chrome_options": ["--window-size=1920x1080", "--proxy-server=192.192.192:3000"]`
- where `192.192.192` is ip and `3000` is proxy port.

##### 🔜 v0.10.X or newer
- Set server ip and port on `proxy` section.

## 4. Run
3. Edit `/home/[USERNAME]/config.js` (in next bash command) with your correct config path and run it for start docker. Bot start automatically.

```sh
docker run --restart=always --name=socialmanagertools-twbot -d -v /home/[USERNAME]/config.js:/app/configs/config.js socialmanagertools/twbot:amd64
```

**AVAILABLE TAGS:** `amd64` (64bit), `i386` (32bit)

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and Contributions have **CC BY 4.0 License**
* Images and Logos have **CC BY-NC 4.0 License**
* Code Snippets/Examples have **MIT License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>
