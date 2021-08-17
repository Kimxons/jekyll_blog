---
layout: post
title: "Inheritance in Solidity"
date: 2021-07-24 15:45:25 +0300
categories: jekyll update
---

Inheritance consists of the word “Inherit”, which means “To Derive”. 

So, Inheritance is defined as one class’s tendency to derive properties and characteristics from other classes. 

It provides additional functionalities to extract features from the base class and imply it into other derived classes significantly.

Inheritance is an eminent concept in Object Oriented Programming (OOP) Paradigm. 
It provides aj mechanism to establish relationships and build hierarchies of class
im object composition. 

Practically, The functions and methods defined in one class may be used in manipulating other data members of the class.


Contracts easily inherit other contracts by using the <mark>is</mark> keyword. 

Function that is going to be overriden by the child contract must be declared as <mark>virtual</mark>

The function that is going to override the parent function must therefore use the keyword <mark>override</mark>

NB: The order of inheritance is very important.
    The parent contracts must be listed in the order "most base-like" to "most derived".  


#### Basic Graph of inheritance

        A
       / \
      B   C
     / \ /
    F  D,E

Remember to include License and solidity versions used

    contract A {
        function foo() public pure virtual returns (string memory) {
            return "A";
        }
    }

Contracts inherit other contracts by using the keyword 'is'. See below code. 
    
    contract B is A {
        // Override A.foo()
        function foo() public pure virtual override returns (string memory) {
            return "B";
        }
    }

    contract C is A {
        // Override A.foo()
        function foo() public pure virtual override returns (string memory) {
            return "C";
        }
    }

Solidity supports multiple inheritance, i.e Contracts can inherit from multiple parent contracts.

When a function is called that is defined multiple times in different contracts, parent contracts are searched from
right to left, and in depth-first (DFS) manner.

#### Example of multiple inheritance

    contract D is B, C {
        // D.foo() returns "C"
        // since C is the right most parent contract with function foo()
        function foo() public pure override(B, C) returns (string memory) {
            return super.foo();
        }
    }

    contract E is C, B {
        // E.foo() returns "B"
        // since B is the right most parent contract with function foo()
        function foo() public pure override(C, B) returns (string memory) {
            return super.foo();
        }
    }


Inheritance must be ordered from “most base-like” to “most derived”.

Swapping the order of A and B will throw a compilation error.

### Example
   
    contract F is A, B {
        function foo() public pure override(A, B) returns (string memory) {
            return super.foo();
        }
    }

Happy coding n00bs <(..)>