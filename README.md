# Ethereum Full Stack Development

A full-stack application for interacting with the Ethereum blockchain. 

## Components and Architecture
### Smart Contracts

1. A contract for creating and updating a message on the Ethereum blockchain
1. A contract for minting tokens, which allows the owner of the contract to send tokens to others and to read the token balances, and lets owners of the new tokens also send them to others

### User-Facing Application

1.Read the greeting from the contract deployed to the blockchain
1.Update the greeting
1.Send the newly minted tokens from their address to another address
1. Once someone has received tokens, allow them to also send their tokens to someone else
1. Read the token balance from the contract deployed to the blockchain

## Testing

The easiest way to test this is to use a test ETH network: this project is configured to work with Ropsten. You will also need an Infura project ID to interface with the ETH blockchain.

1. Create an account with [Infura.io](https://infura.io) if you don't already have one
1. Create an API project on the Ethereum network
1. Under "Keys" copy your project ID and put in your `.env` file under the `INFURA_PROJECT_ID` variable
1. Add your wallet address to the "Allowlist Etherum Addresses"
1. Update the `WALLET_PRIVATE_KEY` environment variable with your wallet's key (the same one used in the last step)
1. Run `npx hardhat run scripts/deploy.js --network ropsten` to deploy your smart contract. Take note of the contract address and save it to the `REACT_APP_SMART_CONTRACT_ADDRESS` environment variable.

You should now be able to see your smart contract on the  [Etherscan Ropsten Testnet Explorer](https://ropsten.etherscan.io) by searching for the contract address.

Run `yarn start` to interact with the contract from the React application. 

---

Originally based on [The Complete Guide to Full Stack Ethereum Development](https://www.freecodecamp.org/news/full-stack-ethereum-development/) tutorial by Nader Dabit.