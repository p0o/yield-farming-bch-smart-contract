## Yield Farming Bitcoin Cash Contract

This is a smart contract with helper libraries to create a token and insert the minting baton into a smart contract that is able to provide everyone the ability to mint the token with a payment to a P2PKH address called premium.

## Use cases

There are numerous use cases for this type of contract including but not limited to:

- Reward tokens for other contracts (e.g DeFi, AnyHedge, etc)
- Governance Token distribution
- Decentralized token sales without custody
- Loyalty tokens to a merchant's customers
- Fundraiser without assurance contract (e.g GoFundMe )
- Decentralized Exchange (requires and oracle for rates)

## Getting started

Clone the project, install the dependencies with NPM:

```
npm install
```

Open the `config.js` and enter the variables except tokenId. Run genesis.js using nodejs:

```
node src/genesis.js
```

The CLI will ask you to send some BCH to an address. 4000 satoshis would be fine. Run it again and you should have your genesisTokenId. Copy the id and insert it in `config.js`

Now run yieldFarming.js using node:

```
node src/yieldFarming.js
```

CLI again ask you to send some BCH to Alice address to pay for the premium and tx fees. Same amount as before would be sufficient. Run the same file again and you should have your tokens minted using the smart contract.

## Disclaimer

There are not enough testing done to this smart contract. It's an experimental type of atomic transaction and should be used with your own responsibility.
