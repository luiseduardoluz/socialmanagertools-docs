> 📌 [index](../../../README.md) / 🔌 [VPN/Proxy](README.md)

## 🔌 Setup Proxy
**IMPORTANT**: **is mandatory use vpn/proxy if you don't want risk of _soft ban_ or _ban_ with server use**.

Facebook, Twitter and Facebook detect after 2-48h server/hosting/vps from ovh, aws, cloud, digital ocean and other providers... What happen if detect you? On facebook if bot click on like, facebook remove like after refresh page = bot not work.

1. Buy proxy server of your country from [highproxies](https://www.highproxies.com/facebook-proxies/) or from you favorite distributor.
2. Edit `configs/config.js` and:

##### 🔙 v0.9.X or previously
- Add new value in `chrome_options` array, example: `"chrome_options": ["--window-size=1920x1080", "--proxy-server=192.192.192:3000"]`
- where `192.192.192` is ip and `3000` is proxy port.

##### 🔜 v0.10.X or newer
- Set server ip and port on `proxy` section.


## 🎁 Support: Donate
[![](https://img.shields.io/badge/donate-paypal-005EA6.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-opencollective-5DA4F9.svg)](http://opencollective.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io)

## 💫 License
* Documentation and Contributions have **CC BY 4.0 License**
* Images and Logos have **CC BY-NC 4.0 License**
* Code Snippets/Examples have **MIT License**

###### Copyleft (c) 2018-2019 [Patryk Rzucidło](https://ptk.dev) ([@PTKDev](https://twitter.com/ptkdev)) <[support@ptkdev.io](mailto:support@ptkdev.io)>