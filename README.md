# Supply chain & data auditing for Fair Trade Coffee

This repository containts an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

## Supply Chain Contract Address on the Rinkeby Network

Supply Chain Contract Address on Rinkeby Network is: [0x1F37aB80412d668c788ea88b1E206242e6996864](https://rinkeby.etherscan.io/address/0x1F37aB80412d668c788ea88b1E206242e6996864)

Transaction Hash on Rinkeby Network: [0xf2264fff35f3f4347cbe7841c6376dd322073aae5f3b8e5c8159909f0102640f](https://rinkeby.etherscan.io/tx/0xf2264fff35f3f4347cbe7841c6376dd322073aae5f3b8e5c8159909f0102640f)

```
Using network 'rinkeby'.

Running migration: 1_initial_migration.js
  Replacing Migrations...
  ... 0x545f28e13dd8b42a5ea5c56646fe957c7dab3aaa434ebafb2d5c1b1b2d5db875
  Migrations: 0x1f37ab80412d668c788ea88b1e206242e6996864
Saving successful migration to network...
  ... 0x4d56937990cff483b744dc239ca2663b505037d0f6f2094bff4dcd27ed08f6d3
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Replacing FarmerRole...
  ... 0xa8f1d01a5bec3664b3ff9513a06001e2b374fb6053be7e824ae2839e5364a05b
  FarmerRole: 0x2388590a7a37904b7220b75bd28ccbaeca4a5ea7
  Replacing DistributorRole...
  ... 0x259ce718273792163992e95d9cd4660f1922c877d45072a73a6237393ed75106
  DistributorRole: 0x71d93118101b7054e410b9d94bf06102558ff96b
  Replacing RetailerRole...
  ... 0xc406f189cc8335918f026a8019c7a4f3ecdaf7083875af55e762a8ce7b696f6b
  RetailerRole: 0x5316e730d23e3588e470b6e553f530d2cb7ff45c
  Replacing ConsumerRole...
  ... 0xd3c7673614e251da75f8611aa253d588946c292cde8f504769494e1f82a690cd
  ConsumerRole: 0xdba9ebd57bda18948806f0ca50e4680dd53540c8
  Replacing SupplyChain...
  ... 0xd4823dd776f72c608751c9d42480dcfd895dfcfae98f14afb3a28a51073cce22
  SupplyChain: 0x608b172fc5acb76fa3f12cc21036872d8fec8f64
Saving successful migration to network...
  ... 0xf2264fff35f3f4347cbe7841c6376dd322073aae5f3b8e5c8159909f0102640f
Saving artifacts...
```

## UML Diagrams

### Activity Diagram

![Activity Diagram](/images/supply-chain-activity.drawio.png)

### Sequence Diagram

![Sequence Diagram](/images/supply-chain-sequence.drawio.png)

### State Diagram

![State Diagram](/images/supply-chain-state-diagram.drawio.png)

### Class Diagram

![Class Diagram](/images/supply-chain-data-model.drawio.png)

## Librarires and their versions used in this project.

- Truffle v5.0.2
- Solidity ^0.4.24
- Node v14.17.6
- Web3.js v1.2.1
- truffle-hdwallet-provider v1.0.17

## IPFS Details

No IPFS was used in this project.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Please make sure you've already installed ganache-cli, Truffle and enabled MetaMask extension in your browser.

### Installing

> The starter code is written for **Solidity v0.4.24**. At the time of writing, the current Truffle v5 comes with Solidity v0.5 that requires function _mutability_ and _visibility_ to be specified (please refer to Solidity [documentation](https://docs.soliditylang.org/en/v0.5.0/050-breaking-changes.html) for more details). To use this starter code, please run `npm i -g truffle@4.1.14` to install Truffle v4 with Solidity v0.4.24.

A step by step series of examples that tell you have to get a development env running

Clone this repository:

```
git clone https://github.com/udacity/nd1309/tree/master/course-5/project-6
```

Change directory to `project-6` folder and install all requisite npm packages (as listed in `package.json`):

```
cd project-6
npm install
```

Launch Ganache:

```
ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

Your terminal should look something like this:

![truffle test](images/ganache-cli.png)

In a separate terminal window, Compile smart contracts:

```
truffle compile
```

Your terminal should look something like this:

![truffle test](images/truffle_compile.png)

This will create the smart contract artifacts in folder `build\contracts`.

Migrate smart contracts to the locally running blockchain, ganache-cli:

```
truffle migrate
```

Your terminal should look something like this:

![truffle test](images/truffle_migrate.png)

Test smart contracts:

```
truffle test
```

All 10 tests should pass.

![truffle test](images/truffle_test.png)

In a separate terminal window, launch the DApp:

```
npm run dev
```

## Acknowledgments

- Solidity
- Ganache-cli
- Truffle
- IPFS
