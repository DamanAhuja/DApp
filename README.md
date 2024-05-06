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

Now we go to the accounts section and click on 
