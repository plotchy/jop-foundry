# Solving ParadigmCTF's JOP in Foundry

This repo hosts the solution I created to solve ParadigmCTF 2021's JOP. Full writeup of this code and its uses available at https://plotchy.substack.com/


## Why JOP?
 JOP poses a unique challenge in that you don't have the source code available! Poking holes in a program that you can't read is something I wanted to try. As an aspiring security auditor, I'm trying to round out my skillset and JOP requires deep understanding of bytecode & managing the EVM stack.


## Why Foundry?
 Foundry separates itself from the pack with the combination of EVM cheatcodes and a kickass debugger. Being able to use prank() to change msg.sender, deal() to change balances, and especially load() and store() to adjust storage slot values promotes quickly testing new ideas and speeds up the exploratory programming phase.

 The only reason I use tools apart from Foundry is due to there being no storage change log. The record() and accesses() cheat codes are great, but they do not compare to Remix Desktop's ability to show storage location changes (slot & value) during debugging. Having the storage locations visibly available during debugging is fantastic for the massive several-step exploit functions that CTFs cater to.