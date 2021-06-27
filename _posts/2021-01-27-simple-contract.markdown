---
layout: post
title:  "Simple Solidity Contract"
date:   2021-06-27 09:04:30 +0300
categories: jekyll update
---

Hello pals. Welcome to my blog once again. 
Lets do some simple smart contract in solidity. 
The smart contract will enable us store and retrieve a number from the blockchain.

<mark>pragma</mark> specifies the compiler version of Solidity.

	// SPDX-License-Identifier: GPL-3.0

	pragma solidity ^0.5.0;

	/**
	 * @title Storage
	 * @dev Store & retrieve value in a variable
	 */
	contract Storage {

	    uint256 number;

	    /**
	     * @dev Store value in variable
	     * @param num value to store
	     */
	    function store(uint256 num) public {
	        number = num;
	    }

	    /**
	     * @dev Return value 
	     * @return value of 'number'
	     */
	    function retrieve() public view returns (uint256){
	        return number;
	    }
	}

You can try it on [remix]("https://remix.ethereum.org/").
Make sure you have added metamask extension to your brwoser and created an account. Connect your metamask and deploy your contract to the blockchain. 

You can then interact with your contract. 

Yeyy! 

Its that simple noobs.