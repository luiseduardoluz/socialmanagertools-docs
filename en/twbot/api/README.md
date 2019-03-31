> 📌 [index](../../README.md) / 📚 [api](README.md)

# 🕹 Get started
Install npm package and run [sample](../installation/npm/README.md) if you want start of use this api.

### Example (with flow login)
```javascript
const config = require ("./config");
const Bot = require("@socialmanagertools/twbot");
let bot = new Bot(config);

(async () => {
	await bot.start();

	let api = await bot.api();

	let response = await api.login.flow();

	if (response.status) {
		response = await api.twofa.flow();
	}

	if (response.status) {
		// Here you are logged...
		// Calls your personal api flow here, example:
		//
		// await api.goto.profile("ptkdev");
		// response = await api.read.user_username("profile");
		// console.log(response.username);
	}

	await bot.stop();
})();
```

# 📎 API Index
Twitter api manual:
  - 📘 [Click](./click/README.md)
  - 📕 [Write](./write/README.md)
  - 📗 [Read](./read/README.md)
  - 📙 [Page](./page/README.md)
  - 📔 [Goto](./goto/README.md)
  - 📒 [Databases](./databases/README.md)
  - 📓 [Stories](./stories/README.md)
  - 📘 [Analytics](./analytics/README.md)
  - 📕 [Check](./check/README.md)

## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and contributions have **CC BY-NC 4.0 License**
* Images and logos have **CC BY-NC 4.0 License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>