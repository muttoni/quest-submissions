# Chapter 1 - Day 1

- Explain what the Blockchain is in your own words. You can read this to help you, but you don't have to: https://www.investopedia.com/terms/b/blockchain.asp
The blockchain is an immutable ledger that everyone can read from and write to (as long as there is consesus).

- Explain what a Smart Contract is. You can read this to help you, but you don't have to: https://www.ibm.com/topics/smart-contracts
A smart contract is a block of code that lives in the blockchain. It benefits from the self-immutability and public availability by living on the blockchain itself, while having infinite use-cases thanks to being able to mutate the blockchain programmatically. In other words, programming logic can be executed completely decentralized and autonomously.

- Explain the difference between a script and a transaction.
A script queries the blockchain, a transaction mutates the blockchain (therefore involves consensus and usually tx fees)

# Chapter 1 - Day 2

- What are the 5 Cadence Programming Language Pillars?
1. resource oriented programming
1. safety and security
1. clarity and readability
1. approachability
1. developer ergonomics (aka experience)

- In your opinion, even without knowing anything about the Blockchain or coding, why could the 5 Pillars be useful (you don't have to answer this for #5)?
Due to the nature of smart contracts, this is code that executes autonomously , meaning a lingering bug can cause devastating effects (think of all the solidity hacks that caused hundreds of millions of dollars to be siphoned off). Readability, approachability makes it easier to spot bugs, safety and security (and resource oriented programming) makes it easier to avoid bugs/leaks and developer ergonomics just provides a joyful experience.

# Chapter 2 - Day 1

For todays quest, please load up a new Flow playground by going to https://play.onflow.org just like we did in this lesson. You will use that for writing your code.

Deploy a contract to account 0x03 called "JacobTucker". Inside that contract, declare a constant variable named is, and make it have type String. Initialize it to "the best" when your contract gets deployed.
[https://play.onflow.org/f8b36bd1-7571-4bf6-97d0-1c49a0ed8e79](https://play.onflow.org/f8b36bd1-7571-4bf6-97d0-1c49a0ed8e79)

Check that your variable is actually equals "the best" by executing a script to read that variable. Include a screenshot of the output.
![image](https://user-images.githubusercontent.com/27052451/188642459-c8d07cdb-854c-488c-8ab0-f5938caf584f.png)

# Chapter 2 - Day 2

1. Explain why we wouldn't call `changeGreeting` in a script.

Because to mutate the blockchain we need a transaction, signed by someone who was access to that resource/contract.

2. What does the `AuthAccount` mean in the `prepare` phase of the transaction?

It contains our account information so the transaction can read from it and use that info to sign the transaction

3. What is the difference between the `prepare` phase and the `execute` phase in the transaction?

The prepare phase can read information in the account, whereas the execute phase can only call specific functions that mutate the blockchain

4. This is the hardest quest so far, so if it takes you some time, do not worry! I can help you in the Discord if you have questions.

- Add two new things inside your contract:
    - A variable named `myNumber` that has type `Int` (set it to 0 when the contract is deployed)
    - A function named `updateMyNumber` that takes in a new number named `newNumber` as a parameter that has type `Int` and updates `myNumber` to be `newNumber`

- Add a script that reads `myNumber` from the contract

- Add a transaction that takes in a parameter named `myNewNumber` and passes it into the `updateMyNumber` function. Verify that your number changed by running the script again.

Playground: https://play.onflow.org/0f73a9c4-3a9c-45bf-94b5-6b23541b95cf?type=script&id=39e37123-3439-4215-bd89-be76eb9af591&storage=none
