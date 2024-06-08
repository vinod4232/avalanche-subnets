# ERC20 and Vault Contracts - README

## Overview

This project contains two main Solidity contracts:

1. **ERC20 Token Contract**: A standard implementation of an ERC20 token.
2. **Vault Contract**: A contract for securely storing ERC20 tokens.

## ERC20 Token Contract

### Features

- Standard ERC20 functions (`transfer`, `approve`, etc.).
- Minting and burning capabilities.

### Deployment

1. Compile the ERC20 contract.
2. Deploy it to your desired Ethereum network.

## Vault Contract

### Features

- Deposit and withdraw ERC20 tokens.
- Tracks user balances.

### Deployment

1. Compile the Vault contract.
2. Deploy it to your desired Ethereum network.
3. Set the ERC20 token contract address in the Vault contract.

## Prerequisites

- Solidity development environment (e.g., Remix, Truffle).

## Example Usage

### Deploying ERC20 Token

```solidity
ERC20Token erc20 = new ERC20Token("MyToken", "MTK", 18, 1000000);
```

### Deploying Vault

```solidity
Vault vault = new Vault(erc20.address);
```

### Interacting

- **Mint Tokens**: `erc20.mint(address, amount);`
- **Deposit Tokens**: `erc20.approve(vault.address, amount); vault.deposit(amount);`
- **Withdraw Tokens**: `vault.withdraw(amount);`

## License

MIT License
