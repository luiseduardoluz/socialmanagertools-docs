> 📌 [index](../../../README.md) / 👮 fbbot / 💾 [installation](../README.md) / 🐧 [debian server](README.md)

# 🐧 Setup - Debian 9 Linux Server
## 1. Install dependencies:
Run `sudo apt-get install build-essential xvfb libssl-dev curl wget git chromium xauth`

## 2. Install Node on Debian
1. `curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh `
2. `sudo bash nodesource_setup.sh`
3. `rm nodesource_setup.sh`
4. `sudo apt-get install nodejs npm`

## 3. Configs
1. Download [latest bot version](https://github.com/social-manager-tools/socialmanagertools-fbbot/archive/master.zip) and extract it.
2. Run `npm install` in `socialmanagertools-fbbot-master` folder.
3. Get [config.js](https://raw.githubusercontent.com/social-manager-tools/socialmanagertools-fbbot/master/configs/config.js.tpl) remove  `.tpl ` suffix and insert file into `configs` folder, fill it properly.

## 4. You don't have monitor?
- Edit `configs/config.js` and set `chrome_headless` to `enabled`, is mandatory.

## 5. Proxy
**IMPORTANT**: **is mandatory use vpn/proxy if you don't want risk of _soft ban_ or _ban_ with server use**.

Facebook, Twitter and Facebook detect after 2-48h server/hosting/vps from ovh, aws, cloud, digital ocean and other providers... What happen if it detects you? On facebook, if bot clicks on like, facebook will remove likes after refresh page = bot will not work.

1. Buy proxy server of your country from [highproxies](https://www.highproxies.com/facebook-proxies/) or from you favourite distributor.
2. Edit `configs/config.js` and:

##### 🔙 v0.9.X or previously
- Add new value in `chrome_options` array, example: `"chrome_options": ["--window-size=1920x1080", "--proxy-server=192.192.192:3000"]`
- where `192.192.192` is ip and `3000` is proxy port.

##### 🔜 v0.10.X or newer
- Set server ip and port on `proxy` section.

## 6. Run
1. Start the bot via `npm run start`
2. If it works add a star 🌟 at this project.
3. If you want to help me: **donate on [paypal](http://paypal.ptkdev.io)/[ko-fi](http://coffee.ptkdev.io)** or become a **[backer on patreon](http://patreon.ptkdev.io)**.

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and Contributions have **CC BY 4.0 License**
* Images and Logos have **CC BY-NC 4.0 License**
* Code Snippets/Examples have **MIT License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>
