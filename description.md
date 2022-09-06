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
2. __migrations__: The 1_initial_migration.js file deploys the Migrations.sol contract. Additionally, we can further create new .js migration files for any new contracts. It is important that they have increasing prefixes (e.g. 2_name_file.js) as Truffle will run the migration in ascending order in terms of the prefix. 

    Migrations are used for the deployment of the code. They automatically push the contracts to the blockchain, link them           together and pass any parameters the constructor requires.
3. __test__: Truffle provides an automated testing framework that allows us to test your contracts in two different ways: using Solidity or Javascript.
