# Aave Flashloan Example

## What is a Flashloan?
- A flashloan is a special type of loan where a user can borrow an asset as long as the return the borrowed amount and some interest all before the end of a transaction.  Since the borrowed amount is returned, with interest during the execution of a single method or transaction, then there is no possibility for someone to take all of the borrowed money. If the loan is not repaid within the transaction, then the transaction fails and everything is reverted.


## Flashloan Applications
- Flashloans are used to aid in arbitrage between assets, to trigger liquidations in DeFi lending protocols, aid in DeFi hacks, and are used in other creative ways.

- This example is a simple flashloan that borrows a single asset, but there are alternative ways to borrow multiple assets.  Learn about other types of flashloan by reading the [Aave documentation](https://docs.aave.com/developers/guides/flash-loans).
