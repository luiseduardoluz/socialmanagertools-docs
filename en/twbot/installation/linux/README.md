> 📌 [index](../../../README.md) / 💾 [installation](../README.md) / 🐧 [debian server](README.md)

# 🐧 Setup - Debian 9 Linux Server
## 1. Install dependencies:
Run `sudo apt-get install build-essential xvfb libssl-dev curl wget git chromium xauth`

## 2. Install Node on Debian
1. `curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh `
2. `sudo bash nodesource_setup.sh`
3. `rm nodesource_setup.sh`
4. `sudo apt-get install nodejs`

## 3. Configs
1. Download [latest bot version](https://github.com/social-manager-tools/socialmanagertools-twbot/archive/master.zip) and extract it.
2. Run `npm install` in `socialmanagertools-twbot-master` folder.
3. Get [config.js](https://raw.githubusercontent.com/social-manager-tools/socialmanagertools-twbot/master/config.js.tpl) remove  `.tpl ` suffix and insert file into `configs` folder, fill it properly.

## 4. You don't have monitor?
- Edit `configs/config.js` and set `chrome_headless` to `enabled`, is mandatory.

## 5. Proxy
1. Buy proxy server of your country from [highproxies](https://www.highproxies.com/instagram-proxies/) or from you favorite distributor (NOTE: proxy are available >= v0.10 release).
2. Edit `configs/config.js` and set server ip and port on `proxy` section.

**IMPORTANT**: **is mandatory use vpn/proxy if you don't want risk of _soft ban_ or _ban_ with server use**.

## 6. Run
1. Start the bot via `npm run start`
2. If it works add a star 🌟 at this project.
3. If you want to help me: **donate on [paypal](http://paypal.ptkdev.io)/[ko-fi](http://coffee.ptkdev.io)** or become a **[backer on patreon](http://patreon.ptkdev.io)**.

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and contributions have **CC BY-NC 4.0 License**
* Images and logos have **CC BY-NC 4.0 License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>