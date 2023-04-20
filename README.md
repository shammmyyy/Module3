# MODULE THREE

This "module 3" demonstrates the deployment of Smart Contracts' basic fundamental syntax and operation.


## Description

With the help of this software, users can deploy contracts, determine their value, and perform mint, burn, and balance transactions.
In order to deploy and test smart contracts, which are almost exclusively written in Solidity, Ethereum Remix IDE is used.

## Getting Started

### Executing program

* We could use an solidity compiler IDE, but we execute this project solidity program using Remix IDE.
* Make a new file in the Remix ethereum IDE (https://remix.ethereum.org) 
```
//SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract ModuleThree {

    // public variables here
    string public tokenName = "Guitar";
    string public tokenAbbrv = "Hero";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```
* The smart contract's legal usage restrictions are specified by the SPDX License Identifier, which is also visible to the compiler, developer, and anyone else viewing it. In the field of software development, there are many distinct licenses.

* After coding your code, you will click the Solidity Compiler at the left-side of IDE, after that, you'll also click the Deploy under the Solidity Compiler.

* You will paste the address at Mint, Burn, and Balances after you have copied it.

* You must first transact with the mint before burn and obtain the balances.

* The uint value or total supply will then be displayed.

 
## Authors
Sham Sham

https://www.facebook.com/siyammmii


## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
