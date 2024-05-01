# Decentralized Stablecoin (DSC) System

This repository contains the implementation of a Decentralized Stablecoin (DSC) system, which consists of two main contracts: `DecentralizedStableCoin` and `DSCEngine`. The DSC is an exogenous, decentralized, anchored (pegged), and crypto-collateralized low-volatility coin pegged to the US dollar.

## Overview

The DSC system is designed to maintain a 1:1 peg with the US dollar by utilizing overcollateralization. Users can deposit collateral (e.g., wETH, wBTC) and mint DSC tokens. The system ensures that the total value of the collateral is always greater than the total value of the minted DSC tokens.

### DecentralizedStableCoin

The `DecentralizedStableCoin` contract is an ERC20 token that represents the stablecoin. It includes standard ERC20 functionalities such as minting, burning, and transferring tokens. The minting and burning of DSC tokens are controlled by the DSCEngine contract.

### DSCEngine

The `DSCEngine` contract is responsible for managing the collateral, minting and redeeming DSC tokens, and handling the stability of the system. It keeps track of the deposited collateral and the minted DSC tokens for each user.

Users can interact with the `DSCEngine` contract to perform the following actions:

- Deposit collateral and mint DSC tokens
- Redeem collateral by burning DSC tokens
- Liquidate undercollateralized positions

The `DSCEngine` contract uses Chainlink price feeds to determine the value of the collateral in USD. It maintains a minimum health factor to ensure that the system remains overcollateralized. If a user's health factor drops below the minimum threshold, their position can be liquidated.

## Getting Started
### Prerequisites

- Node.js (v14 or higher)
- Hardhat
- Foundry

## Installation

1. Clone the repository:
```zsh
git clone https://github.com/your-username/decentralized-stablecoin.git
```


2. Install the dependencies:
```zsh
cd decentralized-stablecoin
npm install
```


## Hardhat Usage

1. Compile the contracts:
```zsh
npx hardhat compile
```


2. Run the tests:
```zsh
npx hardhat test
```


3. Deploy the contracts:
```zsh
npx hardhat run scripts/deploy.js --network <network-name>
```


## Foundry Usage

1. Install Foundry (if not already installed):
```zsh
curl -L https://foundry.paradigm.xyz | bash
```


2. Update Foundry to the latest version:
```zsh
foundryup
```


3. Build the contracts:
```zsh
forge build
```


4. Run the tests:
```zsh
forge test
```


### Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

### License

This project is licensed under the MIT License.# foundry-defi-stablecoin-f23
