---
id: getting-started
title: Wallets
sidebar_label: Getting Started
description: Build your next blockchain app on Polygon.
keywords:
  - docs
  - matic
image: https://matic.network/banners/matic-network-16x9.png 
---


This guide includes wallets that support the Polygon network which Polygon Technology is in 
partnership with, as well as and be a guide for the integration of a key management strategy on 
client side of your dApp.

:::caution Third-party wallets

These third-party wallets have integrated Polygon and support a variety of features. 
You should use your own due diligence in researching and using them. The official Polygon 
Support cannot provide support for issues with these wallets or other non-native wallets.

:::

## Wallets Supporting Polygon

| Wallet 	| Custody 	| Account Type 	| Multi-Sig 	| NFT 	| dApp Browser 	|
|---	|---	|---	|---	|---	|---	|
| [1inch](https://1inch.io/wallet/) 	| non-custodial 	| EOA 	| no 	| interface 	| yes 	|
| [Ambire](https://www.ambire.com/) 	| non-custodial 	| smart contract 	| no 	| interface 	| no 	|
| [BitKeep](https://bitkeep.com/) 	| non-custodial 	| EOA 	| no 	| interface 	| no 	|
| [Coin98](https://coin98.com/wallet) 	| non-custodial 	| EOA 	| no 	| interface 	| yes 	|
| [CypherD](https://cypherd.io/) 	| non-custodial 	| EOA 	| no 	| no 	| yes 	|
| [Guarda](https://guarda.com/) 	| non-custodial 	| EOA 	| no 	| no 	| no 	|
| [Huobi](https://www.itoken.com/en) 	| non-custodial 	| EOA 	| no 	| no 	| no 	|
| [Pillar](https://www.pillar.fi/) 	| non-custodial 	| EOA 	| no 	| interface 	| no 	|
| [Rainbow](https://rainbow.me/) 	| non-custodial 	| EOA 	| no 	| interface 	| yes 	|
| [Sequence](https://sequence.app/auth) 	| non-custodial 	| smart contract 	| no 	| interface 	| no 	|
| [SimpleHold](https://simplehold.io/) 	| non-custodial 	| EOA 	| no 	| no 	| no 	|
| [SteakWallet](https://steakwallet.fi/) 	| non-custodial 	| EOA 	| no 	| interface 	| no 	|
| [TokenPocket](https://www.tokenpocket.pro/en) 	| non-custodial 	| EOA 	| no 	| support 	| yes 	|
| [Torus](https://toruswallet.io/) 	| non-custodial 	| EOA 	| no 	| support 	| no 	|
| [Unstoppable](https://unstoppable.money/) 	| non-custodial 	| EOA 	| no 	| no 	| yes 	|
| [Venly](https://www.venly.io/) 	| hybrid 	| smart contract 	| no 	| interface 	| no 	|
| [XDeFi](https://www.xdefi.io/) 	| non-custodial 	| EOA 	| no 	| interface 	| no 	|

## Wallets for Developers

* [**Arkane**](https://arkane.network/): Arkane is a user-friendly, secure, and custodial key management system for DApps. Arkane supports both Web and mobile, and can service both crypto savvy users as well as a more mainstream audience. Being blockchain agnostic they are a great fit for supporting both Polygon and Ethereum. [For more...](arkane/intro)

* [**Coinbase Wallet**](https://github.com/coinbase/coinbase-wallet-sdk/): Coinbase Wallet is a self-custody crypto wallet, available as a browser extension and a mobile app on Android and iOS. Coinbase Wallet SDK (formerly WalletLink) is an open source SDK which allows you to connect your dapps to millions of Coinbase Wallet users, including their assets and NFTs. It works with all EVM-compatible L1/L2 networks, supports NFTs, and is multi-platform (browser extension, iOS and Android mobile apps). [For more...](https://github.com/coinbase/coinbase-wallet-sdk/)

* [**Fortmatic**](https://fortmatic.com/): Fortmatic SDK allows you to easily integrate your app with the Ethereum blockchain, whether you already have a dApp integrated with web3 or are starting from scratch. Fortmatic provides a smooth and delightful experience for both you and your app's users. [For more...](fortmatic)

* [**Metamask**](https://metamask.io/): Metamask is a browser add-on that manages a user’s Ethereum wallet by storing their private key on their browser’s data store and the seed phrase encrypted with their password. It is a non-custodial wallet, meaning, the user has full access and responsibility their private key. Once lost, the user can no longer control the savings or restore access to the wallet. [For more...](metamask)

* [**Portis**](https://www.portis.io/): Portis is a web-based wallet built keeping easy user-onboarding in mind. It comes with a javascript SDK that integrates into the DApp and creates a local wallet-less experience for the user. Further, it handles setting up the wallet, transactions and gas fees. [For more...](portis)

* [**Torus**](https://toruswallet.io/): Torus is a user-friendly, secure, and non-custodial key management system for DApps. We're focused on providing mainstream users a gateway to the decentralized ecosystem. [For more...](torus)

* [**Wallet Connect**](https://walletconnect.org/): WalletConnect is an open protocol to communicate securely between Wallets and Dapps (Web3 Apps). The protocol establishes a remote connection between two apps and/or devices using a Bridge server to relay payloads. These payloads are symmetrically encrypted through a shared key between the two peers. [For more...](walletconnect)

### High-level steps:

The overall steps would essentially remain the same for any client side application to talk to the blockchain:
 
1. **Set up Web3**: [web3.js](https://web3js.readthedocs.io/) is a javascript library that allows our client-side application to talk to the blockchain. We configure web3 to communicate via Metamask/Wallet Connect/Portis. 
> Note: Refer [Web3.js](https://web3js.readthedocs.io/en/v1.2.2/getting-started.html#adding-web3-js) docs to 
add web3 to your project 
2. **Set up Account**: To send transactions from (specifically for transactions that alter the state of the blockchain) 
3. **Instantiate contracts**: Once we have our web3 object in place, we next instantiate our deployed contract, with which we interact. 
4. **Call functions**: we fetch data via functions in the contract - through our contract object.
