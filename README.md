# METACRAFTERS
##CREATING A TOKEN

This Solidity program demonstrates fundamental syntax and functionality in the process of creating a token. It serves as an initial reference for individuals new to Solidity, aiding in their comprehension of its operations. The objective of this program is to generate tokens and foster acquaintance with the Solidity programming language.

#Understanding

"This Solidity code serves as the primary contract designed for smart contracts on the Ethereum blockchain. It includes elements like 'public' and 'mapping' variables, along with 'creation' and 'destruction' functions. This code offers a superb initiation to Solidity coding and imparts a straightforward grasp of the language structure. It acts as a stepping stone for newcomers, offering them a groundwork for approaching more intricate endeavors ahead."

#Getting Started

To execute the Program Use Remix, an online Integrated Development Environment (IDE) for Solidity, kindly proceed to the official Remix website at https://remix.ethereum.org/. Utilize this platform to initiate the program's execution.

Upon accessing the Remix website, kindly initiate the creation of a new file by selecting the "+" icon located on the left-hand sidebar. It is recommended to save the file with a .sol extension, for instance, MyToken.sol. Subsequently, kindly proceed to copy and paste the code provided below into the newly created file.

//SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

// public variables here
string public tokenname = "ABHI";
string public tokenabbrv = "ABI";
uint public totalsupply = 0;

// mapping variable here
mapping(address => uint) public balances;

// mint function
function mint (address _address, uint _value) public {
    totalsupply += _value;
    balances[_address] += _value;
}

// burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value) {
    totalsupply -= _value;
    balances[_address] -= _value;
    }
}
}

To compile the code, kindly navigate to the "Solidity Compiler" tab located on the left-hand sidebar. Ensure that the "Compiler" option is appropriately configured to "0.8.4" or any other compatible version, and subsequently click on the "Compile MyToken.sol" button.

After compiling the code, the contract can be deployed by accessing the "Deploy & Run Transactions" tab located in the left-hand sidebar. From the dropdown menu, choose the "MyToken" contract and proceed by clicking the "Deploy" button.

Once the contract is deployed, you can engage with it by utilizing the Mint and Burn functions. Select the "MyToken" contract in the left sidebar, then choose options like token name, tokenabbrv, and totelsupply. Afterward, tap the "create" button to initiate a transaction. Lastly, click the "Transaction" button. Execute the function by selecting the appropriate button to mint new coins. Similarly, click the "eliminate" button to reduce the coin supply.

#License

This project is licensed under SPDX-License-Identifier: MIT
