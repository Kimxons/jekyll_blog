---
layout: post
title:  "Simple Token"
date:   2021-07-06 00:26:19 +0300
categories: jekyll update
---

## Not perfect yet

    // SPDX-License-Identifier: MIT

    pragma solidity ^0.8.0;

    import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

    contract MyToken is ERC20 {
        address payable public owner;
        
        constructor() ERC20("MyToken", "MYT") {
            _mint(msg.sender, 1e26);
        }
        function destroy() public {
            require(msg.sender == owner, "only owner");
            selfdestruct(owner);
        }
    }