## Handling the Error - Solidity Contract

This Solidity contract is designed to handle errors and enforce certain conditions on the 'money' variable. It provides three functions: 'extract', 'stake', and 'isempty' to interact with the money variable.

## Contract Details

1. Solidity version: 0.8.13
2. License: MIT
   
## Functions

1. extract
   
solidity

function extract(uint price) public

The 'extract' function allows extracting a specified amount of money from the contract. It uses a 'require' statement to check if the contract has enough money to extract. If the condition is not met, it will revert with the error message "I does not have enough money."

3. stake
   
solidity

function stake(uint price) public

The 'stake' function allows staking a specified amount of money to the contract. After staking, it checks if the total money exceeds 100. If it does, the function will revert with the error message "my money cannot have more than 100."

4. isempty
   
solidity

function isempty() public view returns (string memory)

The 'isempty' function checks if the money variable has a value of 0. It uses an 'assert' statement to verify this condition. If the assertion fails, it will throw an exception. If the money variable is indeed 0, it returns the string message "Yes, I has no money."

### detailed explanation

1. extract(uint price)
   
This function is used to extract money from the contract's balance. It ensures that the requested amount is not greater than the available balance (money). If the balance is sufficient, the requested amount is subtracted from the balance. Otherwise, it throws an error with the message "I does not have enough money".

2. stake(uint price)
   
The stake function is used to add money to the contract's balance. It adds the specified amount to the money variable. However, if the resulting balance exceeds 100, the function reverts the transaction and throws an error with the message "my money cannot have more than 100".

3. isempty()
   
This function checks if the money variable has a value of 0. It uses the assert statement to verify that the balance is indeed 0. If the assertion fails, indicating that the balance is not 0, it will result in an error.

## Author

SATYA PRAKASH

## Licence

This contract is licensed under the MIT License.





