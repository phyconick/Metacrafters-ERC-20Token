# MyToken

MyToken (MTK) is an ERC20 token with minting and burning capabilities. This smart contract is built using OpenZeppelin's secure and tested libraries.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Overview
MyToken is an ERC20 token that supports the following functionalities:
- Minting new tokens (only by the owner)
- Burning tokens

The contract leverages OpenZeppelin's libraries to ensure security and standard compliance.

## Features
- **ERC20 Standard**: Implements the ERC20 token standard.
- **Mintable**: The owner can mint new tokens.
- **Burnable**: Token holders can burn their tokens.
- **Ownable**: Ownership control is managed, allowing for privileged access to certain functions.

## Installation
1. **Clone the repository:**
    ```sh
    git clone <repository_url>
    cd <repository_directory>
    ```

2. **Install dependencies:**
    ```sh
    npm install @openzeppelin/contracts
    ```

## Usage
### Deployment
To deploy the contract, you can use the following script (e.g., using Truffle or Hardhat).

#### Example (using Hardhat)
1. **Create a deployment script:**

    ```javascript
    // scripts/deploy.js
    async function main() {
        const [deployer] = await ethers.getSigners();

        console.log("Deploying contracts with the account:", deployer.address);

        const MyToken = await ethers.getContractFactory("MyToken");
        const token = await MyToken.deploy(deployer.address);

        console.log("MyToken deployed to:", token.address);
    }

    main()
        .then(() => process.exit(0))
        .catch((error) => {
            console.error(error);
            process.exit(1);
        });
    ```

2. **Run the deployment script:**

    ```sh
    npx hardhat run scripts/deploy.js --network <network_name>
    ```

### Interacting with the Contract
#### Minting Tokens
Only the owner can mint new tokens.

```solidity
await token.mint(<recipient_address>, <amount>);
