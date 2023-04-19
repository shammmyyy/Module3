# MODULE THREE

This "module 3" shows the fundamental syntax and operation of how to mint an NFT, to deployed Contracts.

## Description

This software demonstrates basic minting, mint transactions, burn transactions, and balance transactions.

## Getting Started

### Executing program

* We may execute this Solidity program using Remix IDE.
* Make a new file in the Remix ethereum IDE (https://remix.ethereum.org) and save it as a .sol file.
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

* You will paste the address at Mint Burn and Balances after you have copied it.

* You must first transact with the mint before burn and obtain the balances.

* The uint value or total supply will then be displayed.

 
## Authors
Sham Sham

https://www.facebook.com/siyammmii


## License

This project is licensed under the [SHAMSHAM] License - see the LICENSE.md file for details
