## Ganache
Ganache allows you to create a private Ethereum blockchain for you to run tests, execute commands, and inspect state while controlling how the chain operates. It gives you the ability to perform all actions you would on the main chain without the cost. 

## Truffle
Truffle is a developer environment, testing framework and asset pipeline for blockchains. It allows developers to spin up a smart contract project and provides you with a project structure, files, and directories that make deployment and testing much easier.

## Truffle Overview

### truffle init
- Type `truffle init` in the terminal to setup a truffle project or `truffle unbox` to unbox the sample _metacoin_ box. The following folders and files will be added:

  ![alt text](https://user-images.githubusercontent.com/37501487/188546962-fdc06500-3a78-436b-a8d1-73d59647b28a.png "init response")
  
### Purpose of each folder
  
1. __contracts__: contains the __.sol__ smart contracts. The __Migrations.sol__ contract is given by Truffle and it handles the migration history.
