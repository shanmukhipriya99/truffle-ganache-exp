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
4. __build__: After compiling the contracts, a build folder will be automatically created. The files in this folder contain important low-level information such as the __ABI__ and __bytecode__ of the smart contracts. The __address__ of the contract can also be found in these files.
5. __truffle-config.js__: This file sets up the project's configurations. The most important elements here are __network__ and __compilers__. You can set any network like ropsten, Ganache local blockchain or even the mainnet. The network can be selected at the time of deploying: `truffle deploy --network yourNetwork`. The __solc__ compiler configurations can be modified if needed.

### truffle compile
- Type `truffle compile` in the terminal to compile the smart contracts in the contracts folder.

<img width="812" alt="truffle compile" src="https://user-images.githubusercontent.com/37501487/188782275-dafdcaf0-0d55-47a4-bfcc-be105cf0b1f1.png">


- This compiles the original code into __Ethereum bytecode__.
- Upon successful completion, a __.json__ file under __build/contracts__ folder is created.

<img width="316" alt="build folder" src="https://user-images.githubusercontent.com/37501487/188782089-5d96b71e-8970-4641-b0ea-a0d2e010e3b0.png">

### truffle migrate
- Type `truffle migrate` to deploy to the network.

<img width="728" alt="truffle migrate" src="https://user-images.githubusercontent.com/37501487/188783630-74b55937-70e3-48e8-a4ed-5ff052928cc7.png">

### truffle test
- Type `truffle test` to test the cases defined for the given smart contract.

<img width="871" alt="truffle test" src="https://user-images.githubusercontent.com/37501487/188785185-a28a9c7a-c41d-4564-9ea6-de1ae8c1c9a5.png">


