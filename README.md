# CustomToken Smart Contract

## Overview

The CustomToken smart contract is an Ethereum-based ERC-20 token that extends the functionality of the OpenZeppelin ERC20 implementation. This token, named "Whale" with the symbol "WHA," allows for the creation, transfer, and destruction of tokens on the Ethereum blockchain.

## Features

1. **Ownership Control**: The smart contract includes a simple ownership mechanism. The individual who deploys the contract is set as the initial owner, and only the owner can perform certain actions, such as minting new tokens.

2. **Minting Token**: The owner can mint new Whale (WHA) tokens and assign them to a specified recipient. This functionality is restricted to the owner to prevent unauthorized token creation.

3. **Burning Tokens**: Token holders can burn their own tokens, reducing the total supply. This process requires the account initiating the burn to possess a sufficient balance of WHA tokens.

4. **Token Transfer**: Token holders can transfer WHA tokens to other addresses, facilitating peer-to-peer transactions. The transfer function includes an event (`TokensMoved`) that logs the movement of tokens.

## Smart Contract Details

- **Name**: Whale
- **Symbol**: WHA
- **Decimals**: 18
- **Initial Supply**: The total supply of WHA tokens is specified during contract deployment, and the initial supply is assigned to the contract deployer's address.

## Usage

### Deployment

1. Deploy the smart contract, specifying the initial supply of WHA tokens.

### Interacting with the Contract

1. **Mint Tokens**:
   - Call the `mintTokens` function, specifying the recipient's address and the amount of WHA tokens to mint. This action is restricted to the contract owner.

2. **Burn Tokens**:
   - Call the `burnTokens` function, specifying the amount of WHA tokens to burn. This action can only be performed by the token holder.

3. **Transfer Tokens**:
   - Call the `transferTokens` function, specifying the recipient's address and the amount of WHA tokens to transfer.

### Ownership

- The ownership of the contract is initially assigned to the address deploying the contract (`msg.sender`).
- Only the owner can mint new tokens.
- Ownership can be transferred by deploying a new contract or by modifying the contract code.

### Events

- The contract emits the `TokensMoved` event whenever tokens are minted, burned, or transferred. This event logs the sender, recipient, and the amount of tokens moved.

## Author 

Mohammed Faiz
mohammedfaiz866@gmail.com
