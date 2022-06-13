Simple NFT minting page with Add to White List , WL Mint, Public Mint, and NFT reveal menu for the creator
Mint option with quantity for everyone else.
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

TODO: Add usage

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