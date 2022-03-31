# Solving ParadigmCTF's JOP in Foundry

This repo hosts the solution I created to solve ParadigmCTF 2021's JOP. Full writeup of this code and its uses available at https://plotchy.substack.com/


## Why JOP?
JOP poses a unique challenge in that you don't have the source code available! Poking holes in a program that you can't read is something I’ve wanted to try and would advocate others to try as well. Approaching problems through first-principles is a great guiding force, and learning the barebones bytecode will round out your skillset alongside Solidity.

Also, it currently does not have a hosted write-up explaining its intricacies and I wanted to fill this void.


## Why Foundry?
Foundry separates itself from the pack with the combination of providing EVM cheatcodes and a kickass debugger. Being able to use prank() to change msg.sender, deal() to change balances, and especially load() & store() to read & alter storage slot values promotes quickly testing new ideas and speeds up the exploratory programming phase.

Foundry also is designed to have the user writing only Solidity. It’s a very enjoyable experience to stay in Solidity-mode rather than context switching between JS/Python for deployment and testing your ideas. 

From a CTF-solver standpoint I only wish there were a storage change log. The record() and accesses() cheat codes are great, but it’s so useful to view storage location changes (slot & value) during debugging — especially so for the massive multi-step exploit functions that CTFs cater to. Nonetheless, I am quickly becoming a Foundry-main and only go to other debuggers like Remix for storage-related problems.