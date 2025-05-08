# FundMe Smart Contract

A decentralized crowdfunding application built on Ethereum, utilizing Chainlink price feeds for ETH/USD conversion.

## Overview

This project consists of a `FundMe` contract that allows users to:
- Fund the contract with ETH (minimum $5 USD equivalent)
- Track funders and their contributions
- Allow only the owner to withdraw all funds

The contract uses Chainlink's price feed to ensure that contributions meet the minimum USD threshold.

## Smart Contracts

- **FundMe.sol**: The main crowdfunding contract
- **PriceConverter.sol**: Library for ETH/USD price conversion using Chainlink oracles

## Technical Features

- Gas optimizations with `constant` and `immutable` variables
- Multiple withdrawal methods (transfer, send, call)
- Fallback and receive functions to handle direct ETH transfers
- Custom error handling
- Function modifiers for access control

## Requirements

- Solidity ^0.8.24
- Chainlink Contracts

## Setup Instructions

1. Clone this repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Compile contracts:
   ```bash
   npx hardhat compile
   ```

## Deployment

To deploy to a testnet (e.g., Sepolia):

```bash
npx hardhat run scripts/deploy.js --network sepolia
```

## Testing

```bash
npx hardhat test
```

## License

MIT
