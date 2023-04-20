# NTC Token

NTC Token was created to exhibit the lessons we have learned from this coourse. This Token will be our first sample token where we applied the basics of Cryptograpy, Blockchain and Solidity. Lastly, this will serve as my stepping stone as an aspiring Web3 Developer.

## Description

NTC Token is a sample smart contract using Solidity for evaluation purposes. This smart contract will execute the basic functions of this token including, mapping function (the checking of balance), minting function (the adding of the amount to the total supply) and the burning function (the removal of token from the total supply). NTC Token will be our first project that will serve as our first stage of achieving that Web3 ambition.

## Getting Started

Like other smart contracts on the blockchain. NTC Token will be ran at Remix or Remix IDE (https://remix.ethereum.org/) - is a no-setup tool with a GUI for developing smart contracts. To run this code the user must input the license identifer to be followed by the IDE's version:

    // SPDX-License-Identifier: MIT
         pragma solidity 0.8.19;
         
And to be followed by the token's characters together with its functions:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.19;

contract NTCToken {
    
    string public TokenName = "NTC Token";
    string public TokenSymbol = "NTC";
    uint public totalSupply = 0;
    
    mapping(address => uint) public balances;

    function mint(address _address, uint _amount) public {
        totalSupply += _amount;
        balances[_address] += _amount;
    }

    function burn(address _address, uint _amount) public {
        if(balances[_address] >= _amount) {
            totalSupply -= _amount;
            balances[_address] -= _amount;
        }
    }
    }
## Help

If issues occur, please execute diagnostics and check the past lessons from the module regarding the issue. For further, assistance kindly reach out to the author.



## Authors

Gamalliel N. Tamaca

Email: 8213858@ntc.edu.ph

Discord: gammmy #5689

## License

This project is licensed under the MIT License.
