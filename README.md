
> `Tips`

> Currenttly, Online published projects does not work because from 2022 many of cloud providers canceled or changed free services and instances especially Herokou.


# Online 

[Order Market](https://armanriazi.github.io/site/public/blockchain/solidity/smart-contract-sale)


[Energy-Trading](https://armanriazi.github.io/site/public/blockchain/solidity/smart-contract-marketplace-in-energy/)


[Real-Estate](https://armanriazi.github.io/site/public/blockchain/solidity/smart-contract-real-estate/)


# Included Repositories

[armanriazi-ethereum-market](https://github.com/armanriazi/armanriazi-ethereum-market)

[armanriazi-ethereum-marketplace-in-energy](https://github.com/armanriazi/armanriazi-ethereum-marketplace-in-energy)

[armanriazi-ethereum-in-real-estate](https://github.com/armanriazi/armanriazi-ethereum-in-real-estate)

#  A templete guide to demonstrating the smart contracts

## Prerequisites
This documentation has been intended for readers with a basic understanding on the Solidity smart contract programming language and on basic web developing tools. In order to run, the demo requires the following software to be installed. For verified functionality, the specified versions are recommended:

```
Ubuntu 16.04.2 LTS

TestRPC, version 3.0.4

Truffle, version 3.2.1

Node.js, version 7.9.0

Running an Ethereum client
```

### Install dependencies

Before the first run, dependencies need to be installed for the test scripts and the status viewer.

```
cd scripts/
npm install
cd scripts/status
bower install
```

### Run a deterministic TestRPC session
For demoing purposes, TestRPC is a good choice for a client, for a number of reasons. Firstly, TestRPC creates a new blockchain instance and transactions can be paid with tokens of the said blockchain. The creator of the TestRPC session gains access to the tokens for free and therefore transactions can be made without a cost. Secondly, by default, TestRPC is configured in such a way that there is no block time—instead, blocks are created on demand, whenever transactions occur. This type of a configuration is well suited for quick testing and demoing. Finally, TestRPC can be run in deterministic mode. This means that a smart contract’s address, for example, can be known already before deploying it in the blockchain. This makes it possible to reference the address in scripts made for testing or demoing purposes.

```
testrpc -d
```

### Deploy the contract
The smart contracts written in Solidity need to be compiled and deployed to the blockchain. This can be achieved by using a development environment for Ethereum called Truffle. A simple migration script needs to be created for Truffle, after which the contracts can be deployed using the following command:

```
truffle migrate
```

### Run the issuer script that issues smart meter ownerships
For the demo, a seller and a buyer are needed. Furthermore, the ownership of a smart meter needs to be assigned to both of these parties. In our demo, we utilize an approach where a master key holder has the power to establish ownerships to the system participants. 

### Open the status view in browser
Without a graphical user interface, none of the process steps can be visually observed in any way. Therefore, a simple web-browser-based status viewer has been added to the demo appli cation. It shows the changes in the status of the different entities as a crude HTML table. The status viewer can be accessed by opening the web page index.html in any web browser.

### Smart Contracts
The logic of the  market smart contract is defined in the Solidity file Market.sol. The contract defines the public methods for creating sell offers, accepting them, sending smart meter reports and withdrawing assets.

### GUI
The status viewer is a web page which is useful for observing changes in the blockchain while running the demo. It shows the status of all the created sell offers and the account balances of the buyer, the seller and the  market smart contract. The status viewer can be run by opening the file index.html in any web browser.

## Reference

[PersonalWebSite-Blockchain](https://armanriazi.github.io/site/public/blockchain/blockchain)

[PersonalWebSite-Videos-Solidity](https://armanriazi.github.io/site/public/blockchain/Solidity/)
---


#### Author of armanriazi-solidity: armanriazi.blockchain@gmail.com

#### I Made it with ❤️ for you
