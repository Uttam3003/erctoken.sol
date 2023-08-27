# erctoken.sol
# RewardToken Smart Contract
This is a simple Ethereum smart contract that represents a custom token with reward functionality. The contract allows the creator to mint tokens, send rewards, and burn tokens. Users can also transfer tokens to others.

## Token Details
### Token Name: META
### Token Symbol: MTA
### Total Supply: 100 Tokens

## Contract Owner
The creator of this contract has special privileges to manage the token.

## Contract Functions
Send Reward
Function: sendReward(address recipient, uint amount)

## Description: Allows the sender to send tokens to another address as a reward.

## Modifiers:

Requires the sender to have a sufficient token balance.
Updates the sender's and recipient's token balances accordingly.
Burn Tokens
Function: burnTokens(uint amount)

## Description: Allows the sender to burn (destroy) a specific amount of their own tokens.

## Modifiers:

Requires the sender to have a sufficient token balance.
Reduces the sender's token balance.
Decreases the total token supply.
Mint Reward Tokens
Function: mintRewardTokens(address to, uint amount)

## Description: Allows the contract owner (creator) to mint new tokens and assign them to a specific address.

## Modifiers:

Only the contract owner can call this function.
Increases the recipient's token balance.
Increases the total token supply.
# Usage
Deploy the contract to the Ethereum network.
Use the functions to interact with the contract:
### sendReward: Send tokens as rewards to another address.
### burnTokens: Destroy a specific amount of your own tokens.
### mintRewardTokens: Mint new tokens and assign them to an address (only available to the contract owner).
# Important Note
The contract's token supply is set to 100 initially and can change as tokens are minted, sent, or burned.
Make sure to understand the implications of minting, sending, and burning tokens.
# License
This project is licensed under the MIT License. See the LICENSE file for details.

