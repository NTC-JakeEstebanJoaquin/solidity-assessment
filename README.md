# SOLIDITY ASSESSMENT

This contract provides a basic implementation of a token with minting and burning capabilities, following the provided requirements.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.

## Getting Started

### Installing

* To get started, go to the Remix website at https://remix.ethereum.org/.
  
### Executing program

* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
* Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract MyToken {

    // public variables here
    string public tokenName = "BREAD";
    string public tokenAbbrv = "BIX";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
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

* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the "Compile myToken.sol" button.

* Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" 

* Once the contract is deployed, you can interact with it by "Solidity Compiler"


## Authors


[NTC] Jake Esteban Joaquin

## License

This project is licensed under the [Jake Esteban Joaquin] License - see the LICENSE.md file for details
