# Testing a contract

In this example, let's use the [second challenge](https://ethernaut.openzeppelin.com/level/0x9CB391dbcD447E645D6Cb55dE6ca23164130D008) by [Ethernaut](https://ethernaut.openzeppelin.com/) to write our tests. Next page we will be writing our final script to submit the instance. Quick reminder: this section have the purpose to explain how to use Foundry and not explain how to solve this challenge. Case you need more information to comprehend the solution, check the references in the end of the page.

Assuming that your environment is ready to go, just follow the steps bellow.

### 1. Setting up the project

After creating the project **foundry\_demo**, let's remove the files: _Counter.sol_, _Counter.t.sol_ and _Counter.s.sol_. And then copy the second challenge code to a new file named as _Fallback.sol_ in the **src** folder.

### 2. Compile the contract

However, if we try to compile this contract, an error of dependency will be returned. Because in this contract, it is using the Open Zeppelin library SafeMath.

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-10 at 23.04.31.png" alt=""><figcaption><p>Dependency error</p></figcaption></figure>

To fix this error, let's install this dependency using the `forge` command and then add to a file _remappings.txt_ in the root folder of the project.

```bash
forge install openzeppelin/openzeppelin-contracts@v3.2.0 --no-commit
forge remappings > remappings.txt
```

Inside the _remappings.txt_ file, rename _openzeppelin-contracts_ to _@openzeppelin,_ and remove the last child directory_._ The third line should look like this.

```
@openzeppelin/=lib/openzeppelin-contracts/
```

To compile the contract, type `forge build` in your terminal.

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-10 at 23.22.38.png" alt=""><figcaption><p>Successful compilation</p></figcaption></figure>

### 2. Writing Tests

soon...

