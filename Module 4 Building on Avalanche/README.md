Degen Gaming Introduction

Degen Gaming 🎮, a renowned game studio, has approached you to create a unique token that can reward players and take their game to the next level. You have been tasked with creating a token that can be earned by players in their game and then exchanged for rewards in their in-game store. A smart step towards increasing player loyalty and retention 🧠

Project Tasks

Minting new tokens: The platform should be able to create new tokens and distribute them to players as rewards. Only the owner can mint tokens.
Transferring tokens: Players should be able to transfer their tokens to others.
Redeeming tokens: Players should be able to redeem their tokens for items in the in-game store.
Checking token balance: Players should be able to check their token balance at any time.
Burning tokens: Anyone should be able to burn tokens, that they own, that are no longer needed.

Contract Explanation

Overview
The GameClone contract is a simple token and in-game item management system built on the Ethereum blockchain. It allows the contract owner to mint tokens, and users can transfer, burn, and redeem tokens for items in the in-game store.

Key Components
State Variables:

owner: The address of the contract owner.
name, symbol, decimals, totalSupply: Token metadata and supply.
ItemName, Itemprice: Mappings for storing item names and prices.
balance: Mapping for storing user balances.
redeemedItems, redeemedItemCount: Mappings for tracking redeemed items.
Constructor:

Initializes the contract with token details and sets up the initial items in the game store.
Events:

Mint: Emitted when new tokens are minted.
Transfer: Emitted when tokens are transferred.
Burn: Emitted when tokens are burned.
Redeem: Emitted when an item is redeemed.
Functions:

GameStore: Allows the owner to add items to the store.
mint: Allows the owner to mint new tokens.
balanceOf: Returns the token balance of a given address.
transfer: Allows users to transfer tokens to another address.
burn: Allows users to burn their tokens.
Itemredeem: Allows users to redeem tokens for in-game items.
getRedeemedItemCount: Returns the number of items a user has redeemed.
