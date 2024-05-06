# Dapp
## Prerequisits
- Node Js
- Github
- git
## Main aim
![image](https://github.com/DamanAhuja/DApp/assets/142963733/70520772-a64c-4974-8bb1-6b69b3d94952)
## Tools Used
HardHat
MetaMask
## Getting Started
```
# install yarn
npm install --global yarn
# clone the example code repo
git clone https://github.com/ChainShot/hardhat-ethers-react-ts-starter.git
cd hardhat-ethers-react-ts-starter
# install the project's dependencies
yarn && cd frontend && yarn && cd ..
# compile the smart contracts
yarn hardhat compile
# start your local Ethereum blockchain
yarn hardhat node
```
The final yarn hardhat node step is important to do now, as it is necessary to have a local Hardhat network running before installing and configuring the MetaMask browser extension for Hardhat!

Once you have Hardhat network running you’ll see output in your terminal similar to:
![image](https://github.com/DamanAhuja/DApp/assets/142963733/23543ccd-1d51-4df5-b3a3-e48f74ae1a6e)

Now we have a directory named hardhat-ethers-react-ts-starter

Enter command 
``` cd hardhat-ethers-react-ts-starter ```
And then enter 
``` ls ```
![image](https://github.com/DamanAhuja/DApp/assets/142963733/467ada03-943d-4de1-8f29-620c747c3cfb)
The Contracts directory contains the MYContract file

The frontend file contains the react js script which designs the frontent

## Installing MetaMask
Follow the official steps to install metamask 
![image](https://github.com/DamanAhuja/DApp/assets/142963733/7d1a9cbb-c504-4d50-b366-da7c7b75c626)

Now we hsve to make a few changes in the settings

First go to settings > advanced and turn on the 'Show Tet Networks' and 'Customize transaction nonce'

Then go to networks
![image](https://github.com/DamanAhuja/DApp/assets/142963733/82f5e03f-473d-46a4-b7d8-b7b5a3ed04bd)

We change the Chain ID of Loacal Host to 31337.

Now we go to the accounts section and click on Import Account 
![image](https://github.com/DamanAhuja/DApp/assets/142963733/5e2c8535-f1bc-49d6-933f-0561e6220608)

Remember, earlier we saved a private key?

Now enter that key here and import the account
![image](https://github.com/DamanAhuja/DApp/assets/142963733/1a8aa5d2-bb94-4132-92e8-0d21b9a39989)

Now you will be able to see 1000 ETH in your account (Unfortunately there are test tokens)
![image](https://github.com/DamanAhuja/DApp/assets/142963733/a128dc66-09ad-4282-bb33-60b7dde70c6b)

## The Greeter Dapp
The contracts file for the Dapp is
```
//SPDX-License-Identifier: Unlicense
pragma solidity ^0.8.0;
import "hardhat/console.sol";
contract Greeter {
  string private greeting;
  constructor(string memory _greeting) {
    console.log("Deploying a Greeter with greeting:", _greeting);
    greeting = _greeting;
  }
  function greet() public view returns (string memory) {
    return greeting;
  }
  function setGreeting(string memory _greeting) public {
    console.log("Changing greeting from '%s' to '%s'", greeting, _greeting);
    greeting = _greeting;
  }
}
```
### Starting our Dapp
```
cd frontend
yarn start
```
A browser window will open 
![image](https://github.com/DamanAhuja/DApp/assets/142963733/25cbb7f2-2247-44f1-ac21-62886c9edb46)

### Connecting MetaMask
Here you can see your MetaMask wallet is not yet connected to your Dapp, so you can’t yet interact with it. Go ahead and click on the Connect button and select Account 2 (the account you imported into earlier) from MetaMask’s dialog box.

![image](https://github.com/DamanAhuja/DApp/assets/142963733/19839f95-a8a6-45e6-9edd-0f89f151634b)

In the MetaMask dialog window click ‘Next’, and then click ‘Connect’. This will connect your MetaMask wallet to your Greeter Dapp frontend, which will communicate with the Greeter.solsmart contract.

![image](https://github.com/DamanAhuja/DApp/assets/142963733/6aa68689-3dac-4eed-b3b4-a5c646cd1a69)

You can see information about your locally running blockchain and your MetaMask account, including which chain id your account/wallet is connected to, the current block number, the address of the connected account, the account balance, and the account’s next nonce. You can also see there is no deployed Greeter.sol smart contract (yet! — we’re getting there).

