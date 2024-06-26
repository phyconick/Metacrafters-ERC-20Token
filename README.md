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

## Authors

- [@phyconick](https://github.com/phyconick)


## License

This project is licensed under the [MIT](https://choosealicense.com/licenses/mit/) License. See the LICENSE file for details.
