# Error Handling
## FIRST MODULE
## FINAL PROJECT

There are three Error Handling methods in Solidity whose implementation and explanation is shown below through line by line code and it explanation.
1. require
2. assert
3. revert

## Code Explanation

// SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;

contract DivideByZero  {

function divide(uint256 numerator, uint256 denomenator) public pure returns (uint256){

    require(denominator !=0, "Division by zero is not allowed");
    
    return numerator / denominator;
}

function divideWithAssert(uint256 numerator, uint256 denominator) public pure returns (uint256){  

    assert(denominator !=0);    
    
    return numerator/ denomenator;
}
function divideWithRevert(uint256 numerator, uint256 denominator) public pure returns (uint256){

    if (denominator ==0){
    
      revert("Division by zero is not allowed");
    }
    return numerator / denominator;
} 

### DivideByZero

DideByZero contract is a simple Solidity contract that provides three functions to perform division operations between two numbers. It includes error handling mechanisms to prevent division by zero.

## Functions

1. divide(uint256 numerator, uint256 denominator) → uint256
This function performs the division operation between the numerator and denominator parameters and returns the result as an unsigned integer. It includes a require statement to check if the denominator is not zero. If the division by zero is attempted, the function reverts with an error message.

2. divideWithAssert(uint256 numerator, uint256 denominator) → uint256
Similar to the divide function, this function performs the division operation between the numerator and denominator parameters. It uses an assert statement to validate that the denominator is not zero. If the denominator is zero, the assertion fails, and the function execution reverts.

3. divideWithRevert(uint256 numerator, uint256 denominator) → uint256
This function also performs the division operation between the numerator and denominator parameters. It uses an if statement to check if the denominator is zero. If it is zero, the function execution reverts with an error message. Otherwise, it returns the result of the division.

## Author

SATYA PRAKASH

## Licence

This contract is licensed under the MIT License.





