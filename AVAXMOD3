// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract RewardToken {
    string public tokenName;
    string public tokenSymbol;
    uint public totalSupply;
    address public creator;
    mapping(address => uint) public balances;

    constructor(string memory _name, string memory _symbol, uint _initialSupply) {
        tokenName = _name;
        tokenSymbol = _symbol;
        totalSupply = _initialSupply;
        creator = msg.sender;
        balances[msg.sender] = _initialSupply;
    }

    modifier onlyCreator() {
        require(msg.sender == creator, "Restricted: Only creator");
        _;
    }

    function sendReward(address recipient, uint amount) public {
        require(balances[msg.sender] >= amount, "Insufficient balance");
        balances[msg.sender] -= amount;
        balances[recipient] += amount;
    }

    function burnTokens(uint amount) public {
        require(balances[msg.sender] >= amount, "Insufficient balance");
        balances[msg.sender] -= amount;
        totalSupply -= amount;
    }

    function mintRewardTokens(address to, uint amount) public onlyCreator {
        balances[to] += amount;
        totalSupply += amount;
    }
}
