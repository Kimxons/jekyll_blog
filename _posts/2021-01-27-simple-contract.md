---
title:  "Simple Solidity Contract"
layout: post
categories: post
---

Hello pals. Welcome to my blog once again. 
Lets do some simple smart contract in solidity. 

Here is a simple contract that you can store, and retrieve a number in this contract.

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

The first line in our smart contract in solidity shows the licensing of the source code. You can notice that the licensing of the source code follows the GPL version 3.0. It is important to focus on machine-readable license specifiers in an environment that allows the default publication of source code. 
There are number of <mark>licenses</mark> out there; //SPDX-License-Identifier: GPL-3.0 is one of them though. 

<mark>pragma</mark> specifies the compiler version of Solidity. This line shows that the source code is compatible with Solidity version 0.5.0 or newer versions of the language. (pragma solidity ^0.5.0)

 Solidity offers profound support for C-type and C++-type comments. Therefore, any type of text between the characters ‘/*’ and ‘*/’ is referred to as a comment which could span multiple lines. In addition, any type of text found between the ‘//’ and the end of a line is referred to as a comment, and most importantly, the Solidity compiler ignores the text. Here is an example that can outline the ideal use of comments.

### Decoding our smart contract

TODO -- 

You can try it on [remix]("https://remix.ethereum.org/").
Make sure you have added metamask extension to your brwoser and created an account. Connect your metamask and deploy your contract to the blockchain. 

You can then interact with your contract. 

Yeyy! 

Its that simple noobs.