# Welcome to HashLips 👄

![](https://github.com/HashLips/hashlips_nft_minting_dapp/blob/main/logo.png)

All the code in these repos was created and explained by HashLips on the main YouTube channel.

To find out more please visit:

[📺 YouTube](https://www.youtube.com/channel/UC1LV4_VQGBJHTJjEWUmy8nA)

[👄 Discord](https://discord.com/invite/qh6MWhMJDN)

[💬 Telegram](https://t.me/hashlipsnft)

[🐦 Twitter](https://twitter.com/hashlipsnft)

[ℹ️ Website](https://hashlips.online/HashLips)

# HashLips NFT minting dapp 🔥

![](https://github.com/HashLips/hashlips_nft_minting_dapp/blob/main/banner.png)

This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/HashLips/hashlips_nft_minting_dapp.git
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "", // need to add contract address as variable
  "SCAN_LINK": "https://avaxscan.com/token/", // need to add contract address as variable
  "NETWORK": {
    "NAME": "Avalanche",
    "SYMBOL": "Avax",
    "ID": 137 // get correct id for main/test
  },
  "NFT_NAME": "TestNFT", // TODO get name from smart contract
  "SYMBOL": "TCV", // TODO get symbol from smart contract
  "MAX_SUPPLY": 10000, // TODO get max supply from smart contract
  "WEI_COST": 75000000000000000, // TODO get wei cost from smart contract
  "DISPLAY_COST": 0.075, // TODO get convert from wei to ether
  "GAS_LIMIT": 285000, // TODO get gas limit for avax mainnet before release
  "MARKETPLACE": "TACVUE",
  "MARKETPLACE_LINK": "https://tacvue.io/collection/nerdy-coder-clones", //
  "SHOW_BACKGROUND": true
}
```
Copy the contract ABI to `public/config/abi.json` file.
```css
:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.png`, and
`public/logo512.png` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Nerdy Coder Clones</title>
<meta name="description" content="Mint your Nerdy Coder Clone NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "NCC",
  "name": "Coder Clone NFT"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
