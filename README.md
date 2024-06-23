# Wallet connection with Frontend

This project is a tutorial for learning to create a frontend for our smart contract and connect to our Metamask wallet in our browser through the frontend.

## Description

The smart contract works on EVM, and the frontend is made using react. We use Hardhat to compile and run our local EVM and perform operations, i.e. the functions we created in our smart contract.

[Assesment.sol](contracts/Assesment.sol) contains the smart contract with functions `getBalance()`, `deposit()` and `withdraw()` which are later imported into [index.js](pages/index.js) to extend to the frontend. Two buttons are present in the frontend that executes these functions and they also handle exceptions in this file.

## Execution

These are the steps to run the project in your local system.

- Open three terminals in this directory.
- In the first one, type `npm i`. This will install all dependencies npm will need.
- In the second one, type `npx hardhat node`. This will setup the EVM in your local machine.
- In the third one, type `npx hardhat run --network localhost scripts/deploy.js`. This will compile the project.
- Now back in the first terminal, type `npm run dev`. This will run the project and you can access the frontend in https://localhost:3000.

## Configuration
Now you can access the frontend, but before trying the project there are a few things you should do:
- You need to add a network in your metamask wallet.

  Go to `Settings -> Networks -> Add a network` and fill up the form.
	- **RPC url** is the link present at the starting of the output of the second terminal
	- **Chain ID** is `31337`
	- **Currency Symbol** is `ETH`.
- You need to be the owner of the smart contract that you are running in your browser. To do that, you need to add your local account address to metamask.
  - Go to metamask and into adding another account
  - Then click on `Import Account`
  - Go to your second terminal, at the starting of the accounts list copy the **Private Key** of **Account 0**. That is the owner of the contract.
  - Paste it in the input field in metamask.
  - (Optional) Name the account you added for easier usage.

## Usage

Now that we have everything set up, you can open the localhost and try out the project. Connect the wallet to the newly added account, and transact!