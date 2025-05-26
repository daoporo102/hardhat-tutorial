# Hardhat Tutorial Project

This project demonstrates a basic Ethereum development workflow using [Hardhat](https://hardhat.org/). It includes a time-locked smart contract, comprehensive tests, and deployment configuration using Hardhat Ignition.

## Overview

The project consists of:

- A [`Lock`](contracts/Lock.sol) smart contract that locks ETH for a specified time
- A complete test suite for the contract in [`test/Lock.js`](test/Lock.js)
- A Hardhat Ignition module for deployment

## Smart Contract

The [`Lock`](contracts/Lock.sol) contract allows:

- Locking ETH for a predetermined period
- Withdrawing funds only after the unlock time has passed
- Only the owner can withdraw the funds

## Getting Started

### Prerequisites

- Node.js and npm

### Installation

```powershell
npm install
```

### Testing

Run the test suite to verify the contract works as expected:

```powershell
npx hardhat test
```

### Deployment

Deploy using Hardhat Ignition:

```powershell
npx hardhat ignition deploy ignition/modules/Lock.js
```

You can customize deployment parameters:

```powershell
npx hardhat ignition deploy ignition/modules/Lock.js --parameters unlockTime=1893456000,lockedAmount=2000000000
```

## Project Structure

- [`contracts`](contracts) - Smart contract source code
- [`test`](test) - Test files for the contracts
- [`ignition/modules`](ignition/modules) - Hardhat Ignition deployment modules
- [`artifacts`](artifacts) and [`cache`](cache) - Compilation artifacts and cache

## License

This project is licensed under the ISC License.
