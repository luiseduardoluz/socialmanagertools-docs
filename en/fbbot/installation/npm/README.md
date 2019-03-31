> 📌 [index](../../../README.md) / 💾 [installation](../README.md) / ⛏ [npm](README.md)

## ⛏ NPM Usage
1. Run `npm install @social-manager-tools/fbbot`
2. Get [config.js](https://raw.githubusercontent.com/social-manager-tools/socialmanagertools-fbbot/master/configs/config.js.tpl) file for step 3, fill it properly and remove `.tpl` suffix.
3. On your code require library, config and run bot, example:
```javascript
const config = require ("./config");
const Bot = require("@socialmanagertools/fbbot");
let bot = new Bot(config);

(async () => {
	await bot.start();

	let api = await bot.api();

	let response = await api.login.flow();

	if (response.status) {
		response = await api.twofa.flow();
	}

	if (response.status) {
		response = await api.mode.flow();
	}

	await bot.stop();
})();
```
4. If it works add a star 🌟 at this project.
5. If you want to help me: **donate on [paypal](http://paypal.ptkdev.io)/[ko-fi](http://coffee.ptkdev.io)** or become a **[backer on patreon](http://patreon.ptkdev.io)**.

See [API Documentation](../../api/README.md) for more methods or if you want create your bot.

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and Contributions have **CC BY 4.0 License**
* Images and Logos have **CC BY-NC 4.0 License**
* Code Snippets/Examples have **MIT License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>