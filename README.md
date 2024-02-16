# MyToken

This Solidity program is a simple ERC20 token contract that demonstrates the basic syntax and functionality of the Solidity programming language . The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program is a contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has functions for minting, burning, and transferring tokens. This program serves as a simple and straightforward introduction to Solidity programming and can be used as a stepping stone for more complex projects in the future. It utilizes openZeppelin

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```=solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.17;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract OtaikiToken is ERC20, Ownable {
    constructor(uint256 initialSupply) ERC20("OtaikiToken", "OTAIKI") Ownable(msg.sender){
        _mint(msg.sender, initialSupply);
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }
}


```

To compile the code, click on the “Solidity Compiler” tab in the left-hand sidebar. Make sure the “Compiler” option is set to “0.8.17” (or another compatible version), and then click on the “Compile Token.sol” button.

Once the code is compiled, you can deploy the contract by clicking on the “Deploy & Run Transactions” tab in the left-hand sidebar. Select the “MyToken” contract from the dropdown menu, and then click on the “Deploy” button.

Once the contract is deployed, you can interact with it by calling the mint, burn, and transfer functions. Click on the “ERC20” contract in the left-hand sidebar, and then click on the function you want to call. Finally, click on the “transact” button to execute the function.
## Authors

Otaiki Sadiq


## License

This project is licensed under the MIT License - see the LICENSE.md file for details


