---
layout: post
title:  "Sample Token"
categories: post
---

	pragma solidity ^0.7.0;

	import 'https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v3.2.0-solc-0.7/contracts/token/ERC20/ERC20.sol';

	// This ERC-20 contract mints the specified amount of tokens to the contract creator.
	contract FunToken is ERC20 {
	  constructor(uint256 initialSupply) ERC20("FunToken", "FUT") {
	    _mint(msg.sender, initialSupply);
	  }
	}

This is a simple ERC-20 contract based on the current Open Zeppelin ERC-20 template. It creates FunToken with symbol FUT and mints the entirety of the initial supply to the creator of the contract.