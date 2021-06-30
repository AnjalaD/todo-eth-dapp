# DApp with Web3 and ReactJs

Eth dapp using `web3.js` and `reactJs` with `Metamask browser extension`.

[web3.js](https://web3js.readthedocs.io/en/v1.3.4/)

[Metamask](https://metamask.io/)

## Devtools

Ganache - Ethereum blockchain that can be run on your pc. This can be used for testing.

## Setup for test run (using Ganache)

1. Download Ganche from [here](https://www.trufflesuite.com/ganache).
2. Run Ganache.
3. Install Metamask extension.
4. `Metamask > settings > networks` add network\
   Network name: `Ganache`
   New RPC URL: `RPC of Ganache(can be viewed in Ganache app), usually http://localhost:7545`
   Chain ID: `1337`
   Currency: `Eth`
5. Connect to Ganache from extension
6. In extension `create acount > import account`, using account private key from Ganache Accounts.
7. Install packages in both root and truffle directories.
8. Run following commands to deploy smart contract
   ```bash
   cd truffle
   ```
   Go to the `truffle-config.js` and update Ganache configuration if needed.
   ```
   yarn truffle migrate
   # or try "yarn truffle migrate --reset"
   ```
   Copy the `contract address` from the output.
9. Go to `src/config.js`, replace `TODO_LIST_ADDRESS` value with copyied address.
10. `yarn start` the root project
11. Due to new Metamask update, Metamask will not automatically connect to `localhost:3000`.
    Use extention options to add it manually.
