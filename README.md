# nft-poc

A small proof of concept on creating a smart contract that can mint NFT's

Based off of [this post](https://medium.com/pinata/how-to-build-erc-721-nfts-with-ipfs-e76a21d8f914)

## Requirements
* [Node](https://nodejs.org/en/)
* [ipfs](https://docs.ipfs.io/how-to/command-line-quick-start/)
* [Ganache](https://www.trufflesuite.com/ganache)
* [Truffle](https://www.trufflesuite.com/truffle)
* [Pinata Account](https://www.pinata.cloud/)

## Running

1. Make sure Ganache is up and running. Connect the truffle-config.js file through the contracts tab.
2. Run truffle compile to compile UniqueAsset.sol
3. Run truffle migrate to transact the smart contract
4. Start the debug console with `truffle console`
5. Instantiate a contract variable with `const instance = await UniqueAsset.deployed();`
6. Call the mint function with `instance.awardItem("{address}","{hash}","ipfs://{metahash}")` replacing address, hash, and metahash with appropriate values
