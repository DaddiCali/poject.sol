# DADDICALI's TOKEN

Solidity is a programming language used to write smart contracts on the Ethereum blockchain. A token is a digital asset that is created and traded on a 
blockchain. Solidity tokens are digital assets created using the Solidity programming language and deployed on the Ethereum blockchain as smart contracts.


## Description

Solidity tokens can be used for a variety of purposes, including as a means of payment, for governance, or as a reward mechanism within a decentralized 
application (dApp). They can be traded on decentralized exchanges (DEXs) and can have a variety of different properties and functionalities depending on 
how they are programmed.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18(
or another compatible version), and then click on the "Compile token" button.

code blocks for commands

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "DaddiCali";
    string public tokenAbbrv = "Cali";
    uint public TotalSupply= 0;
   
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
       TotalSupply+= _value;
       balances[_address] += _value;
    }
    // burn function
    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
       TotalSupply-= _value;
       balances[_address] -= _value;
       }
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18(
or another compatible version), and then click on the "Compile project.sol" button.

After compiling the code, you can deploy the contract by selecting the "Deploy & Run Transactions" tab in the left-hand sidebar. Click the "Deploy" button.

after i deploy it im going to deployed contracts then copy the ACCOUNT 

*click down the mint tab then paste the account and i put my desired token ammount(20000)then click transact to confirm the token amount that i 
inserted i click the totalsupply below of TokenName

to test the burn function
*click down the burn tab then paste the account and i put my desire amount that will be burn (10000) then click transact to confirm it again how much
token i had left i click the totalsupply.

last to check if the IF STATEMENT i made is working im going to put 15000 for the amount to be burn then testing if it will burn the token more than i have
as u expected nothings happen bacause my system cannot burn token more than i have

## Authors

carlsly june d butt     
@carls lee


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
