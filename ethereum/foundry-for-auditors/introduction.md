# Introduction

For those who are not familiar with Foundry, after finish the installation you will get three tools: **`anvil`**, **`cast`** and **`forge`**.&#x20;

* **anvil** - runs a local node, similar to ganache.&#x20;
* **cast** - is like the _netcat_ for Foundry. You can interact with the blockchain without code, convert data types, read storage from the blockchain.&#x20;
* **forge** - initiates, manage your project, deploy and test your contracts.&#x20;

Foundry uses Solidity language for everything that we will perform. This is good because we don't need to pick a language like Python or Javascript to have a professional development  and testing environment. So if you know Solidity, you're good to go!&#x20;

Let's create a demo project.&#x20;

```bash
forge init foundry_demo
```

Look at the project structure.

```
foundry_demo/
├─ lib/
├─ script/
├─ src/
├─ test/
├─ foundry.toml
```

#### Lib folder

This is where all your dependencies of your project will be. e.g. OpenZeppelin libraries.

#### Script folder

This is where the code that will interact with contracts that are on-chain, like testnets or/and mainnets will be. e.g. final exploit codes. The files ends with the extension ".s.sol".

#### Src folder

This is where the contracts will be. e.g. vulnerable contracts. The files ends with the extension ".sol".

#### Test folder

This is where the code for interact with the contracts off-chain will be, to perform some type of tests like fuzzing or for validate the existence of any possible flaws. e.g. initial step to understand the vulnerability and how to exploit. The files ends with the extension ".t.sol".

#### _foundry.toml_ file

Configuration file of the project. For more information, [click here](https://book.getfoundry.sh/config/).



