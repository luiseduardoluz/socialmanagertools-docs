> 📌 [index](../../../README.md) / 🐣 twbot / 💾 [installation](../../installation/README.md) / 📀 [multiaccount](README.md)

# 📀 How setup multi-account
Config.js allow ONLY 1 mode but you can run multiple account or multiple modes with [cli version](../../installation/source/README.md) or [gui](../../../gui/installation/README.md).


## Multi-account for GUI - Desktop app:
1. Set username and password, select social algorithm, set available settings and press start
2. Wait 30seconds...
3. Set another username and password, select social algorithm, set available settings and press start again.
2. Wait 30seconds...
3. Set another username and password, select social algorithm, set available settings and press start again.

Now you run 3 account with different mode: bot display message warning if you try run two times same account and same mode (it's smart). You can run same account with different mode but **WARNING**: remember not exceeded 1000/like or retweet days in combo of modes or twitter daily limits.

#### How check logs of single account with gui if run more accounts:
1. Set username (only)
2. Press LOGS button.

## Multi-account for CLI:

1. Create multiple config.js in `/configs/` folder:
- `/configs/user1_likemode_classic.js`
- `/configs/user1_rtmode_classic.js`
- `/configs/user2_likemode_classic.js`

2. Don't use `npm run start` but run with multiple command line with args:

```sh
node bot.js --config="./configs/user1_likemode_classic.js"
node bot.js --config="./configs/user1_rtmode_classic.js"
node bot.js --config="./configs/user2_likemode_classic.js"
```

User1 run 2 different modes. User1 run one mode: remember not exceeded 1000/rt or like days in combo of modes or other twitter daily limits. Bot don't display warnings of istances in combo mode.

## Multi-account for Docker:

1. Create multiple `config.js` files and run docker command with different `--name` args and different config path, example:
- `docker run --restart=always --name=socialmanagertools-twbot1 -d -v /home/pi/configs/user1_likemode_classic.js:/app/configs/config.js socialmanagertools/twbot:amd64`
- `docker run --restart=always --name=socialmanagertools-twbot2 -d -v /home/pi/configs/user1_rtmode_classic.js:/app/configs/config.js socialmanagertools/twbot:amd64`
- `docker run --restart=always --name=socialmanagertools-twbot3 -d -v /home/pi/configs/user2_likemode_classic.js:/app/configs/config.js socialmanagertools/twbot:amd64`

User1 run 2 different modes. User1 run one mode: remember not exceeded 1000/rt or like days in combo of modes or other twitter daily limits. Bot don't display warnings of istances in combo mode.

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and Contributions have **CC BY 4.0 License**
* Images and Logos have **CC BY-NC 4.0 License**
* Code Snippets/Examples have **MIT License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>