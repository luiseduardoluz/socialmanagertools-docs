> 📌 [index](../../../README.md) / 💾 [installation](../../installation/README.md) / 📀 [multiaccount](README.md)

# 📀 How setup multi-account
Config.js allow ONLY 1 mode but you can run multiple account or multiple modes with [cli version](../../installation/source/README.md) or [gui](../../../gui/installation/README.md).

## Example (CLI):

1. Create multiple config.js in `/configs/` folder:
- `/configs/user1_likemode_realistic.js`
- `/configs/user1_comment_realistic.js`
- `/configs/user1_fdf_realistic.js`
- `/configs/user2_likemode_realistic.js`
- `/configs/user2_likemode_classic.js`

2. Don't use `npm run start` but run with multiple command line with args:

```sh
node bot.js --config="./configs/user1_likemode_realistic.js"
node bot.js --config="./configs/user1_comment_realistic.js"
node bot.js --config="./configs/user1_fdf_realistic.js"
node bot.js --config="./configs/user2_likemode_realistic.js"
node bot.js --config="./configs/user2_likemode_classic.js"
```

User1 run 3 different modes. User2 run two same like modes: remember not exceeded 1000/like days in combo of modes or instagram daily limits.

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and contributions have **CC BY-NC 4.0 License**
* Images and logos have **CC BY-NC 4.0 License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>