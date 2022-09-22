---
cover: ../../.gitbook/assets/761663813436_.pic.jpg
coverY: 0
---

# 🎓 core

### Workflow

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### aTokens

Each asset supported by the Abel finance Protocol is integrated through a aToken contract, which is an EIP-20 compliant representation of balances supplied to the protocol. By minting aTokens, users (1) earn interest through the eToken's exchange rate, which increases in value relative to the underlying asset, and (2) gain the ability to use aTokens as collateral.

aTokens are the primary means of interacting with the Abel finance Protocol; when a user mints, redeems, borrows, repays a borrow, liquidates a borrow, or transfers aTokens, he/she will do so using the aToken contract.

There are currently two types of aTokens: Single Coin and LP Coin. Though both types expose the EIP-20 interface, As such, the core functions which involve transferring an asset into the protocol have slightly different interfaces depending on the type, each of which is shown below.

### Redeem

The redeem function converts a specified quantity of aTokens into the underlying asset, and returns them to the user. The amount of underlying coins received is equal to the quantity of aTokens redeemed, multiplied by the current Exchange Rate. The amount redeemed must be less than the user's Account Liquidity and the market's available liquidity
