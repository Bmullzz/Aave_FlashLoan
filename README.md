# Aave Flashloan Example

## What is a Flashloan?
- A flashloan is a special type of loan where a user can borrow an asset as long as the return the borrowed amount and some interest all before the end of a transaction.  Since the borrowed amount is returned, with interest during the execution of a single method or transaction, then there is no possibility for someone to take all of the borrowed money. If the loan is not repaid within the transaction, then the transaction fails and everything is reverted.


## Flashloan Applications
- Flashloans are used to aid in arbitrage between assets, to trigger liquidations in DeFi lending protocols, aid in DeFi hacks, and are used in other creative ways.

- This example is a simple flashloan that borrows a single asset, but there are alternative ways to borrow multiple assets.  Learn about other types of flashloan by reading the [Aave documentation](https://docs.aave.com/developers/guides/flash-loans).

- One use case for flashloans is Arbitrage. Imagine there are 2 exchanges, A and B. Exchange A is selling a token, `LW3`, for a lower price than exchange B. An Arbitrageur can make a profit by buying `LW3` from echange A for DAI, then selling it on exchange B for more DAI than they initially started with.

## How do Flashloans work?
- There are 4 basic steps to any flashloan. To execute a flashloan, you need to write a smart contract that contains a method which uses a flashloan.  Assume this method is called `createFlashLoan()`.  The following 4 steps happen in this order when you call that function:
    -  The contract calls a function on a Flashloan provider, like Aave, indicating which asset you want to and how much to borrow.
    - The Flashloan provider sends the assets to your contract, and calls back into your contract for a different function, `executeOperation()`.
    - `executeOperation()` is all custom code that you have written. At the end, you grant approval to the Flash Loan Provider to withdraw the borrowed assets from the contract plus a premium.
    - The Flash Loan provider then takes back the assets it gave you, plus the premium for lending you the assets.

    

